# Mobile App - Technical Constraints & Architecture

## Platform Architecture Overview

### Separate Native Applications
**Android App**:
- **Technology**: Native Android (Kotlin/Java)
- **Developer Team**: 1 Senior Android Developer
- **Minimum SDK**: Android 8.0 (API level 26) - supports 85% of Croatian market
- **Target SDK**: Android 14 (API level 34)
- **IDE**: Android Studio
- **Build System**: Gradle with modular architecture

**iOS App**:
- **Technology**: Native iOS (Swift)
- **Developer Team**: 1 Senior iOS Developer  
- **Minimum iOS**: iOS 13.0 - supports 90% of Croatian iPhone users
- **Target iOS**: iOS 17.0
- **IDE**: Xcode
- **Build System**: Swift Package Manager + CocoaPods

### Shared Backend Infrastructure
**API Layer**:
- **Technology**: Node.js + Express.js
- **Database**: PostgreSQL (user data, workouts, progress)
- **Authentication**: JWT tokens with refresh mechanism
- **Rate Limiting**: Platform-specific limits (Android: more conservative due to performance)

**Content Delivery**:
- **Video Hosting**: Vimeo Pro (external dependency)
- **Image Storage**: AWS S3 with CloudFront CDN
- **Content Management**: Custom CMS for workout library
- **Localization**: Croatian/Bosnian content management system

## External Dependencies & Integration Points

### Critical External Services

**Vimeo Integration**:
- **Purpose**: Video hosting and streaming for workout content
- **API**: Vimeo API v3.4
- **Constraints**: 
  - Rate limits: 1000 requests/hour per app
  - Video quality options limited by user's Croatian internet speeds
  - Download capabilities restricted by Vimeo Pro plan
- **Risk Assessment**: Single point of failure for core feature
- **Mitigation**: Video caching strategy, fallback to lower quality streams

**ejabberd Chat System**:
- **Purpose**: Real-time chat between users and 30 expert agents
- **Protocol**: XMPP with custom extensions
- **Constraints**:
  - Legacy system not optimized for mobile push notifications
  - Connection stability issues during Android battery optimization
  - Limited message history retrieval on mobile clients
- **Performance Impact**: Affects chat response time metrics
- **Upgrade Path**: Considering migration to modern chat infrastructure

### Platform-Specific Integrations

**Android-Specific Dependencies**:
- **Google Play Services**: Location, Analytics, Push Notifications
- **Firebase**: Crashlytics, Remote Config, Cloud Messaging
- **Room Database**: Local data persistence and offline support
- **ExoPlayer**: Video playback with adaptive streaming
- **WorkManager**: Background sync and download management

**iOS-Specific Dependencies**:
- **HealthKit**: Integration for health data (heart rate, workouts, nutrition)
- **WatchKit**: Apple Watch companion app development
- **Core Data**: Local data persistence and sync
- **AVFoundation**: Video playback and media management
- **Background App Refresh**: Workout data sync and notifications

## Performance Constraints & Optimization

### Android Performance Challenges

**Device Fragmentation**:
- **Screen Sizes**: 4.5" to 7" displays require responsive video player
- **RAM Variations**: 4GB (30%), 6GB (45%), 8GB+ (25%) affects video caching
- **Processor Range**: Snapdragon 660 to 8 Gen 2 creates performance gaps
- **Storage**: 64GB devices (40% of users) limit offline video downloads

**Battery Optimization Impact**:
- **Doze Mode**: Affects background sync and chat notifications
- **Battery Saver**: Reduces video quality and disables auto-downloads
- **Background App Limits**: OEM-specific restrictions (Samsung, Xiaomi, etc.)
- **Mitigation Strategy**: Adaptive performance based on device capabilities

**Network Performance**:
- **Croatian Internet**: Average 25 Mbps, but rural areas struggle with video
- **Data Cost Sensitivity**: 60% of users prefer WiFi-only video downloads
- **Peak Hour Congestion**: 7-10pm performance degrades 35%
- **Optimization**: Multiple video quality tiers, aggressive caching

### iOS Performance Considerations

**Memory Management**:
- **Video Caching**: Intelligent cache management for seamless playback
- **HealthKit Data**: Efficient sync without draining battery
- **Watch Connectivity**: Maintain connection without impacting phone performance
- **Background Processing**: Optimize workout data sync during background refresh

**Integration Complexity**:
- **HealthKit Setup**: Complex permission flow affects onboarding conversion
- **Watch App**: Standalone functionality requires careful data synchronization
- **AirPlay Support**: Video streaming to Apple TV requires additional testing
- **Siri Integration**: Voice shortcuts implementation for quick workout access

## Development & Release Constraints

### Android Development Limitations

**Team Capacity**:
- **Single Developer**: Limits parallel feature development
- **Code Review**: Relies on iOS developer for cross-platform patterns
- **Testing Coverage**: Manual testing on limited device set
- **Release Management**: Google Play Store review process (2-3 days)

**Technical Debt**:
- **Legacy Code**: Some modules from pre-Kotlin era need refactoring
- **Architecture**: Monolithic structure makes feature isolation difficult
- **Testing**: Limited unit test coverage (currently 45%, target 80%)
- **Documentation**: API integration documentation needs updating

### iOS Development Limitations

**Team Capacity**:
- **Single Developer**: Feature development bottleneck
- **Apple Ecosystem**: Requires expertise in Watch, HealthKit, multiple frameworks
- **Device Testing**: Need physical devices for Watch integration testing
- **Release Management**: App Store review process (1-7 days, strict guidelines)

**Apple-Specific Constraints**:
- **App Store Guidelines**: Strict review process affects feature release timing
- **iOS Version Support**: Balancing new features vs backward compatibility
- **HealthKit Permissions**: Complex privacy requirements affect user onboarding
- **Watch App**: Additional complexity for standalone functionality

## Security & Privacy Constraints

### Data Protection Requirements

**GDPR Compliance** (Croatian/EU users):
- **Data Minimization**: Collect only essential user data
- **Consent Management**: Granular permissions for health data, analytics
- **Data Portability**: User data export functionality required
- **Right to Deletion**: Complete user data removal capabilities

**Health Data Sensitivity**:
- **Progress Photos**: Encrypted storage, user-controlled sharing
- **Health Metrics**: HealthKit integration requires special privacy handling
- **Chat Messages**: End-to-end encryption for expert consultations
- **Payment Data**: PCI compliance for subscription processing

### Platform Security Requirements

**Android Security**:
- **Certificate Pinning**: Protect API communication
- **ProGuard/R8**: Code obfuscation for release builds
- **Biometric Authentication**: Fingerprint/face unlock for sensitive data
- **Network Security**: Protection against man-in-the-middle attacks

**iOS Security**:
- **Keychain Services**: Secure storage for authentication tokens
- **App Transport Security**: HTTPS enforcement for all network calls
- **Biometric Authentication**: Touch ID/Face ID for app access
- **Code Signing**: Distribution certificate management

## Scalability & Infrastructure Constraints

### Current System Limitations

**Backend Scaling** (15k → 25k users):
- **Database Performance**: PostgreSQL optimization needed for peak hours
- **API Rate Limits**: Current limits may not support 67% user growth
- **Video Streaming**: Vimeo bandwidth costs increase linearly with users
- **Chat Infrastructure**: ejabberd may need clustering for 30+ agents

**Mobile App Scaling**:
- **Download Management**: Offline content storage strategy needs optimization
- **Push Notifications**: Firebase/APNs scaling for increased message volume
- **Analytics**: Event volume will increase 67% with user growth
- **Support Burden**: App store reviews and user support scaling

### Technical Debt Impact

**Priority Technical Debt** (affects feature velocity):
1. **Android Architecture**: Monolithic structure slows feature development
2. **Chat Integration**: Legacy ejabberd integration creates maintenance overhead
3. **Video Player**: Custom implementation needs modernization
4. **Testing Infrastructure**: Low test coverage increases bug risk
5. **Documentation**: Poor API documentation slows development

**Debt Mitigation Strategy**:
- **Quarterly Refactoring Sprints**: 20% of development time
- **Architecture Migration**: Gradual modularization of Android app
- **Chat System Evaluation**: Research modern alternatives to ejabberd
- **Testing Improvement**: Increase coverage by 10% per quarter

## Development Workflow & Tools

### Cross-Platform Coordination

**Shared Components**:
- **API Specifications**: OpenAPI documentation for consistent implementation
- **Design System**: Shared UI components adapted for platform conventions
- **Content Management**: Synchronized workout library and Croatian translations
- **Analytics**: Consistent event tracking across platforms

**Version Alignment**:
- **Feature Parity**: Major features released on both platforms simultaneously
- **Release Schedule**: Bi-weekly releases coordinated between platforms
- **Bug Fix Priority**: Critical issues addressed on both platforms
- **Performance Benchmarks**: Shared targets adapted for platform capabilities

### Quality Assurance Process

**Testing Strategy**:
- **Unit Testing**: Platform-specific test suites (target 80% coverage)
- **Integration Testing**: API contract testing for backend changes
- **Manual Testing**: Device-specific testing on Croatian market devices
- **Performance Testing**: Load testing during Croatian peak hours (7-10pm)

**Release Process**:
- **Staging Environment**: Pre-production testing with subset of real data
- **Gradual Rollout**: 10% → 50% → 100% user rollout over 48 hours
- **Rollback Strategy**: Immediate rollback capability for critical issues
- **Monitoring**: Real-time crash and performance monitoring post-release

## Future Architecture Considerations

### Technology Evolution Path

**Android Modernization**:
- **Jetpack Compose**: UI framework migration for better performance
- **Kotlin Multiplatform**: Shared business logic with iOS
- **Architecture Components**: MVVM pattern implementation
- **Modularization**: Feature-based module structure

**iOS Enhancement**:
- **SwiftUI**: Modern UI framework adoption
- **Combine Framework**: Reactive programming for better data flow
- **iOS 17+ Features**: Latest platform capabilities utilization
- **Watch App Independence**: Standalone functionality improvement

### Infrastructure Scaling Preparation

**Backend Optimization** (for 25k+ users):
- **Microservices Migration**: Gradual decomposition of monolithic backend
- **Caching Strategy**: Redis implementation for frequently accessed data
- **CDN Optimization**: Global content delivery for diaspora users
- **Database Sharding**: Preparation for horizontal scaling

**Chat System Modernization**:
- **WebSocket Implementation**: Replace ejabberd with modern chat infrastructure
- **Real-time Scaling**: Support for increased agent-user conversations
- **Mobile Push Optimization**: Better notification delivery and reliability
- **Integration Simplification**: Reduce maintenance overhead

---

*Technical Owner*: Mobile Development Team (Android + iOS developers)  
*Architecture Review*: Quarterly assessment with backend team  
*Last Updated*: [Current Date]  
*Next Review*: Technical debt impact assessment