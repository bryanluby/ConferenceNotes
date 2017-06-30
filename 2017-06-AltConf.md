# AltConf 2017 Notes

<http://altconf.com>

## Table of Contents

- [Keynote](#keynote)
- [Platforms State Of The Union](#platforms-state-of-the-union)
- [How I Became A Developer At 51](#how-i-became-a-developer-at-51)
- [Mastering Mobile SEO for Your Native App and Website](#mastering-mobile-seo-for-your-native-app-and-website)
- [The Reality of Indie Life](#the-reality-of-indie-life)
- [Kickstarting your app with user feedback](#kickstarting-your-app-with-user-feedback)
- [Challenging Your Assumptions](#challenging-your-assumptions)
- [Finally Automation Magic for both iOS and macOS](#finally-automation-magic-for-boths-ios-and-macos)
- [The Secret Life of Types in Swift](#the-secret-life-of-types-in-swift)
- [Swift Things Programming the Internet of Things with Swift](#swift-things-programming-the-internet-of-things-with-swift)
- [What the Swiftly Func](#what-the-swiftly-func)
- [Helping Users Create Good Habits](#helping-users-create-good-habits)
- [Bringing Machine Learning to your iOS Apps](#bringing-machine-learning-to-your-ios-apps)
- [Misc WWDC Video Notes](#misc-wwdc-video-notes)

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

## How I Became A Developer At 51

Alicia Carr

- She developed the Purple PocketBook; an app to help women get out of domestic violent relationships
- She attended WWDC 2015 and was featured on Apple's website about her app
- Was also later featured in a WWDC Keynote video

## Mastering Mobile SEO for Your Native App and Website

Mada Seghete @mada299 

- Websites and apps can comingle within the same search results
- Voice search
- Search results can differ depending on the type of mobile device
- App users spend 20x time than mobile web visitors
- Apps convert 3x compared to mobile websites
- App transactions are 55% of all mCommerce transactions
- App content is trapped
- The newly designed App Store may actually make discovery even harder
- Make your app content discoverable
    - Google app indexing - Actual organic search results are ranked lower (google results are ranked higher)
    - You still need a website to take of google indexing
    - App content sitemaps with AMP Deepviews for search
    - Ranking still mostly basend an traditional non-app signals
- Tips
    - Targeted web to app flows
    - Pass google mobile friendly test bit.ly/mobilefriendlytest
    - Improve mobile usability (ex, tou flash, use viewports, legible fonts,)
    - Mobile performance matters (visitors will abandon if site takes longer than 3 seconds)
        - Webpagetest.org
        - Chrome dev tools
    - Caveats of AMP (Accelerated Mobile Pages)
        - When a webpage has both AMP and deeplink, Google serves AMP
        - Difficult to get users out of AMP pages

## The Reality of Indie Life

Stephen Hackett

- "Dont half-ass two things. Whole-ass one thing" - Ron Swanson
- Stress in indy life and corporate life a very similar

## Kickstarting your app with user feedback

Leah Culver - Breaker

- Find a large highly fragmented industry
- Low NPS (net promoter score) (low customer loyalty)
- Vertically integrate a solution to simplify value product
- Customer interviews (what do you want)
- Used TestFlight in early stages
- Buglife (In-app user feedback) - Users love it
- Does this feature benefit our ideal user?
- They use mixpanel for analytics - Figure out what is your key metric for the app and try to improve on it over time.
    - They also used Mixpanel funnels and AB testing (link about "Hooked" by Prerna Gupta)
- Inspiration, then data (use data to back up inspirational ideas)

## Challenging Your Assumptions

Kristina Thai @kristinathai

- Assumptions
    - Most users will have the latest feature on their iphone
        - Features may be turned off
        - Network speed may be bad (global differences)
        - We can control battery, performance, and backwards compatibility
        - Repeating functionality (dont be afraid to do this)
    - Users will eventually learn how to do things
        - *Clear* iconography is important
        - Don't deprioritize bugs that have known workarounds
    - People with disabilities don't use our app
        - Impairment is much more common that you think
        - Desiging for permanent impairment can also benefit partially impaired
- Avoiding the assumption mindset
    - Beta test with your entire team
    - Develop with accessibility in mind from the beginning
    - Get in the mind of your users - What people say they do and actually do is usually different
- Assumptions we make on our own team
    - Someone is the expert on that feature - give the work to them. Leads to lack of flexibility on a team and also career stagnation. Allow work to be rotated.
    - If someone does not say things during a meeting means they don't have an opinion. Don't rule out introverts. Meetings may not be ideal for some. One on ones or written communication may be better.
    - Someone asked alot of questions, so they must not know what they are doing.
    - Observe your own team and say something - projectinclude.org/recommendations

## Finally Automation Magic for both iOS and macOS

Sal Soghoian

- OmniAutomation (omni-automation.com)
    - Javascript objects similar to webkit dom
    - Library - can have multiple javascript functions in one file
    - Plugin - can have libraries and actions and other resources
    - Can encode automation scripts into URLs - Then they can be used inter-app
    - Can blend with HTML elements
    - HTML data transfer
    - Works with Workflow app
    - Works app to app

## The Secret Life of Types in Swift

Manu Rink

- No type root
- Protocols instead of inheritecnce
- Super loose coupling
- Good separation of concerns
- Clean architecture
- Two types of types
    - Named types
        - Class, structs, enums, protocols, etc (they have names)
    - Compound Types
        - Tuples (technically you can give them a name with typealias)
        - Functions

## Swift Things Programming the Internet of Things with Swift

Steven Gray & Laurie Hannon SoftSource Consulting

- What if you could write apps in Swift for IoT?
- Why do this?
    - Power - Moores law
    - Money - Huge Opportunity
    - Popularity - Heavy support from Apple
    - Safety - Significant safety improvement over C
- What does it take?
    - Use Swift compiler out of the box
    - Target a low-level IoT chip (Texas Instruments SensorTag)
        - blink LEDs
        - Sound the buzzer
        - Get diagnostics from sensors
        - Respond to button presses
        - Network with other things
- What do you need?
    - A mac with Xcode (or not)
    - Or windows or linux with Swift command line tools
    - A means to flash binaries to your Thing
- What you don't need?
    - A custom build of swift
    - A need to care much about the OS running on the device
- The compiler generates intermedaite language code - once in IR we can combine with code from other languages
- `swiftc -emit-ir hello.swift > hello.ll`
- Contiki open source IoT OS with good support for the SensorTag
- MicroStdlib boilerplate code starting point - Custom "standard" library for IoT
- www.sftsrc.com - they are going to open source their custom IoT library

## What the Swiftly Func

James Majors

- bit.ly/AltConf2017 - slides + code
- Simple Definitions
    - Functional programming is just *one* tool you can use from your toolbox
        - Not always the best approach for UI heavy apps
    - Side effect free
    - Stateless
    - Immutable data
    - Functions are the basic building block
    - Functions as first class citizens
    - Currying is like initializing a function 

## Helping Users Create Good Habits

Sally Shepard @mostgood

- Basics of habits
    - Hooked book
    - Why build habits?
        - Downloads do not equal users
        - What makes the top grossing apps successful? They create habits with users.
        - Behavior: Trigger, motivation, action. Repeating this behaviour creates a habit.
        - Trigger - Get someones attention.
            - External - What brings users to your app *visually* (ex a badge)
            - Internal - When your *brain* commands you to do things
        - Action - The thing a user needs to do
            - Action <-> Ability
            - Increase a products ease of use
            - List every step then remove as many as possible (example remove steps to open the camera app)
        - Reward - Immediate gratification
            - Unlock in-app content
            - Award
            - Sense of completion
            - Status
            - Variability
        - Investment
            - Ask them to give something back to you
                - Money, email, like on facebook, survey, etc.
            - Investment should work towards improving the users experience
- Implementing habits
    - Build habits around goals
    - Start with a goal the user wants to achieve
    - List reasons *why* they want to achive that goal
    - The *why* behind the goal can be used to motivate users
    - Triggers need to include a motivation
    - Actions should be simple and easy to complete
    - The size of investment is proportional to how long they have used the app
    - Ask for investments right after rewards
    - Streaks and habits
        - Hard streak - requires completing every 24 hours - This is stressful for users - You may never get that user back. Not everyone responds to streaks.
        - Soft streak - Can complete an action in a less stressful timeframe - Soften hard streaks by decreasing the reward - Also can make hard streaks more flexible
        - People do not magically reset at midnight - Dont' be lazy about date calculation in streaks - Time zones exist and need to account for them
        - We place significance on doing something a certain number of times
    - Examples shown: Vanido app
- How to test habits (are they working)
    - Analytics are your friend - Similar to crash reports for habits
    - Track events that verify the success as well as the failure of habits
    - Define what an ideal user is, then look for patterns
    - Why are my habits failing?
        - Where in the process are users leaving? Find that and fix them. Sometimes analytics aren't enough and you need more direct contact from users.
        - Are triggers being triggered? (ex push turned off)
        - Make triggers easy to turn on and off
        - Are actions able to be completed? Time, money, effort, non-routine, etc
        - Is the reward strong enough? Is there variability?
        - Is the investment too expensive? Is the investment asked at the right time?
    - Testing habits is tricky
        - Habit time machine
            - Timescale - time intervals to test habit
            - Questions - Ask questions at each interval about the process
            - Empathy - Think about the state of the user
- Habits and Health
    - Blurry line when a habit can become an addiction
    - Have empathy
    - Don't be evil - form habits for people's good

## Bringing Machine Learning to your iOS Apps

Meghan Kane @meghafon

- Enable machines to learn without being explicitly programmed
- Siri, Camera, QuickType
- Enables a more meaningful experience - personalizaiton, identification
- Model: the system that outputs a prediction given an input
- Neural Networks: learns by itself, like a brain
- Vision, Natural Language, GamePlayKit, CoreML
- Check resources slide for this talk for all links
- tinyletter.com/letsinfer + companion podcast
- bike worshop app will use ML

## Misc WWDC Video Notes

- `CALayer` now has maskedCorners: `CACornerMask` (Also can now animate rounding of corners)
- Mail-like full swipe gesture for any table view `performsFirstActionWithFullSwipe` boolean
- Drag and drop is also available on iPhone but is restricted to within the same application
- `NSLinguisticTagger` can detect the dominant language of a given string.
- `NSJSONSerialization` supports sorted keys
- `NSArray` `NSDictionary` and `NSSet` support copy-on-write
- Block-based KVO (Swift only?)
- Drag/drop interaction objects are similar to gesture recognizers
- Enable large nav bar titles with `prefersLargeTitle`and `largeTitleDisplayMode`
- Foundation added support for achiving to json and plist
- UIScrollView `contentLayoutGuide` `frameLayoutGuide` for Auto Layout
- Can use `UIFontMetrics` to scale arbitrary layout spacing values with dynamic type
- For Auto Layout and Dynamic type can use `constraintEqualToSystemSpacing` with and `spacingUsingSystem` for `UIStackView` to let system find the ideal amount of spacing for different dynamic type sizes.
- Wide color (P3) support for app icons
- Touch Bar - Can use interface builder to build touch bar support for macOS apps - `acceptsFirstResponder` gotcha - `otherItemsProxy`for sharing touch bar items between touch bars

