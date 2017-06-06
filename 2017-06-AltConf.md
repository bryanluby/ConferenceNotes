# AltConf 2017 Notes

<http://altconf.com>

## Table of Contents

- [Keynote](#keynote)
- [Platforms State Of The Union](#platforms-state-of-the-union)

## Keynote

### 6 Important Announcements

1. tvOS - Amazon prime video coming to Apple TV.
2. Apple Watch
    - watchOS 4
    - Siri watch face with custom information displayed for the user
    - Kaleidoscope face
    - Toy story watch faces
    - Activity notifications get more personal. Monthly challenges.
    - Workout app has new easier to use UI. High intensity interval training workout type added. Gym equipment integration with Apple Watch starting in Fall.
    - Music - Redesigned UI better - Improved AirPod experience.
3. Mac (High Sierra)
    - Safari
        - Performance improvements
        - Autoplay blocking!
        - Intelligent tracking prevention
    - Mail
        - Improved search
        - Split view
        - Improved storage 
    - Photos
        - New UI and organization
        - Faces improvement
        - Improved photo editing and interaction with other photo apps
    - Data
        - Apple File System will be the default file system
    - Video
        - H.265 HEVC software and hardware support
    - Graphics
        - Metal 2 - Mac window server built on Metal 2
        - Metal for VR - Steam VR with Unity and Unreal
        - External GPUs
    - iMacs
        - Improved iMac display specs
        - Latest Intel chips
        - More memory
        - Standard fusion drives
        - Improved gpus
    - Refreshed specs on all laptops
    - iMac Pro
        - The most powerful mac ever made
        - Up to 18 core Xeon processor
        - Radeon Vega graphics
        - Up to 128 gb of memory
        - Up to 4tb ssd
        - Drive multiple external displays
        - Starts at $4999 available in Dec.
4. iOS 11
    - Messages
        - Redesigned app drawer
        - Messages in iCloud (better syncing for all devices)
    - Apple Pay
        - Person to person payments
        - Built into messages as an iMessage app
    - Siri
        - Better machine learning
        - Translation support
        - Expanded SiriKit support
        - Siri understands better what you want next
    - Camera
        - HEVC capmera capture videos (less storage spece)
        - HEIF image format up to 2x better compression
        - Portrait mode depth API
        - Enhanced Live photo editing
        - Redesigned control center and unified lock screen
        - New photo effects
    - Maps
        - Detailed floor plans of malls (multiple floor support)
        - Airport support
        - Navigation improvements to speed limits and lane guidance
        - Do not disturb while driving - Use bluetooth + wifi to detect
    - HomeKit
        - Speaker support - Airplay 2 - multi-room audio
        - Airplay 2 audio API
    - Apple Music
        - See what your friends are listening to
        - MusicKit API for Apple Music
    - App Store
        - Phased releases
        - Complete redesign
        - Today tab
        - Games tab
        - Apps tab - In app purchase in the store
        - Redesigned product detail page
    - Machine Learning
        - Core ML
        - Vision API
        - Natural Language API
    - AR
        - ARKit!
5. iPad
    - iPad Pro
        - 10.5 inch display
        - Reduced bezel
        - 1 pound
        - Improved display
        - ProMotion - 120Hz refresh rate - Also makes Apple Pencil more responsive (20ms latency)
        - Performance - A10X fusion
        - 10hr battery
        - Improved cameras
        - Start with 64gb
    - iPad + iOS
        - The dock!
        - Multitasking - pull app from the dock
        - New app switcher
        - Drag and drop!
        - Quick type
        - Files app - filesystem for iPad
        - Apple Pencil
            - Instant Markup integrated in iOS
            - Instant notes
            - Searchable handwriting
            - Inline drowing within typed notes
        - Notes built in document scanner
        - Create pdf action
6. Music
    - Reinvent home music
    - Breakthrough home speaker
    - HomePod
    - Spatial awareness
    - Works with Apple Music in the cloud-
    - Responds to hey sir
    - Also can act as a home assistant for other tasks
    - $349 available December

## Platforms State Of The Union

### Swift Playgrounds

- Connect to bluetooth robots, drones, and devices
- Swift Playgrounds 2 in fall
    - Playground feeds

### Xcode 9

- Source Editor
    - Re-written in Swift
    - Integrated markdown editor
    - Improved performance
    - Source highlighting with transformations
    - Brand new refactoring system (works with all languages)
    - Open source Transformation engine
- Swift 4
    - Improved String API
        - Easier to use
        - Multi-line string literals
        - Better string slicing
        - Better unicode support
        - Speed improvements
    - Codable
        - Easy encoding/decoding
    - Easy to Adopt
        - Swift language version choice
        - Mix and match 3.2 and 4.0 targets (ex app and framework)
        - 3.2 can't use swift 4 improvements for existing apis
    - Building large projects
        - 40% faster mixed objc and swift projects
        - 2x build time for projects with whole module optimization
- Core Technologies
    - Indexer
        - Rebuilt architecture
        - Performance improvements for Open quickly and searching
        - Indexing while building
    - Build system
        - New build system (written in Swift)
        - 2.5x faster build operations
    - Source Control
        - Github integrated with Xcode 9
        - New open in xcode button on github website
    - Debugging
        - View controllers in the view debugger
        - SpriteKit and SceneKit scenes in view debugger
        - Runtime sanitizers
            - Undefined behavior
            - Main thread API checker
    - Testing and CI
        - Xcode server is built in to xcode (don't need to install macos server)
        - UI testing multiple applications
        - UI testing query performance improvements
        - Parallel device and simulator testing
        - Simulator supports multiple bootable devices
- Wireless development
    - works on all platforms

### New APIs

- Drag and drop
    - Easy to adopt
    - Flexible and customizable
    - Automatic for standard text and web
    - Tableview and collectionview delegate method support
    - Works with custom data types
    - Reordering support
    - In-app and system-wide multi-touch
    - Secure delivery
    - Example shows adobe dragging layers between multiple adobe apps!
- New Large Title navigation style
- UITableView dynamic type support by default
- Files
    - File browser can be brought up in 3rd party apps
    - Can customize appearance
- Multitasking adoption
    - Size classes
    - Auto layout
    - Default storyboards
- Vector assets i
- Custom fonts and dynamic type
- iMessage
    - App strip
    - Direct send api
- SiriKit
    - Payment accounts
    - Lists
    - QR codes
- MusicKit
    - Play songs and playlists and radio stations
- Photo APIs
    - Photos project extensions for the mac version of Photos
    - Camera detects QR codes - likn into apps with Universal links
    - HEVC and HEIF (compound container format)
    - Depth API - can use custom filters - Can also use with streaming API
- Vision
    - Face, landmark, shap, text, barcode, object tracking
- Metal 2
    - GPU-driven rendering
    - Platform feature alignment (unified API)
    - Machine learning acceleration
    - VR - Steam VR
    - External GPU support
    - Advanced Optimization Tools
- ARKit
    - iPhone 6s and later - iPad Pro and later
    - Visual-Inertial Odometry
    - Scene understanding
    - ARSession
    - Can use SceneKit and SpriteKit to work with ARKit - Can also use Metal 2
