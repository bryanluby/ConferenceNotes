# CocoaConf Chicago 2014 Notes

# AVFoundation Film School - Chris Adamson

- AVFoundation Tightly coupled with core graphics and core animation
- AVAsset top level asset for time based files
- AVURLAsset for remote
- Capturing doesn't store
- Recording mean capturing and storing

# MVVM and Reactive Cocoa for the Haters - Danny Greg

## MVC

- Massive View Controller: too many resposibilities

## MVVM

- View Model - two roles: value converter, mediator
- specialization of mvc. 
- Benefits: testing. Flow of data through app is cleaner than mvc
- View models are platform independent. iPhone/iPad/Mac.
- Serializable: State restoration of a view to disk

## But Cocoa is all MVC?

- ViewController is part of the view.
- You could use mvvm as you go. You don't have to rewrite your entire app.

## RAC: Reactive Cocoa

### Signal

- Time varying value. A new model for thinking about what a variable is. Look at a variable not as a snapshot of what it currently is.
- Operator: modify a value coming down the pipe. Also can be used to merge several values into one.
- NSValueTransformer: Similar to RAC. Bind values with a transformer in the middle.

- This is how our brains work. Inputs and outputs.
- Why simulate this with state?  Reduced if statements. Less housekeeping and glue code.

## Next Steps
- blog.maybeapps.com input and output post - josh abernathy
- RAC repo on github
- Ash Furrow book: functional reactive programming

## Epilogue
- Cross-polination is vital to a community.

# Effective Networking - Ben Schierman

## Problems

- Too many apps do network programming wrong.
- Too much work on the main thread.
- Perpetual loading. No caching.
- Loading too much data at launch time.
- Stale activity feeds.

## iOS 7 APIs - NSURLSession

- NSURLSession will eventually replace NSURLConnection
- Configuration, cache, options, delegate.
- Typically 1 session per api.
- Download task for pausing and resuming. Crash safe.
- Easy callbacks. Caste response to HTTPResponse to get a status code.
- You can also use delegate if you choose not to use block callbacks.
- ephemeralSessionConfiguration: Returns a session configuration that uses no persistent storage for caches, cookies, or credentials.
- test for status code 200
- sessionWithConfiguration:delegate:delegateQueue: - specify the queue for the delegate callbacks
- NSURLSessionDataTask: get, put, post, delete
- Use Charles http://charlesproxy.com to inspect network requests

## AFNetworking 2.0

- Based off of NSObject rather than NSOperation. 
- AFJSONResponseSerializer: handles json decoding. Also plist, xml, custom serializers.
- Base url support
- setAnimatingWithStateOfTask: - convenience category method for activity indicator

## HTTP Caching
- Header data: Etag. Cache-Control. Date.
- Extremely fast and lightweight to look at the header data before downloading data.
- Reverse proxy cache : varnish squid linx
- Cons of cache control: clients may render stale data
- NSURLSession does this automatically. NSURLCache default settings are low.
- Reason about the lifecycle of your data.
- Send os version, app version, and device name as headers.
- Take care when user-specific data
- Turn on gzip compression
- Measure api response times
- slides speakerdeck/subdigital - code on github

# Take your automated testing to the next level - Brand Heintz -  ymedialabs.com

- Defects are cheaper to fix when caught early.
- Skip testing boilerplate. Only test non-trivial parts of your code.
- Don't test third party code.
- Triangulation: using external test data. A second set of test data can expose weaknesses. Boundary conditions. 
- Write new tests when handed legacy code with no tests.
- A stub is a dummy object with an interface like some external object and feeds specified data to your code. Ex. network calls.
- Mocks are fake objects that measure behavior.
- Integration testing is hard. Use unit tests for individual components, then use UI Testing for your integration tests.
- UI Testing - What to test? Where does the user spend most of their time. Empty states. Error states. Authentication tests.
- Write tests that teach you about the system.
- Mocks and stubs decouple tests.
- Test data should be under your control.
- You will spend the most of your time in the Refactor mode of tdd.

# Advanced Core Data - Aaron Douglas

## Concurrency

- Stuttering
- Asynchronous operations
- Batch operations
- NSManagedObjects belong to a single context and thread
- Do not share between threads/contexts
- Pass around threads by NSManagedObjectID
- isTemporaryID

### In the background

- thread containment: each thread gets its own context. Manually manage contexts and merging.
- Queues: initWithConcurrencyType:. PrivateQueue anything not on the UI. performBlock, performBlockAndWait. Main thread can still execute directly.
- Multiple contexts with a single persistent store coordinator: Parent context
- When dealing with multiple contexts, listen for mange object context save notification
- main contexts with worker contexts for the background work.
- Save in one spot
- Merge policy: research NSMergeByPropertyStoreTrumpMergePolicy
- NSErrorMergePolicy - NSError userInfo[@"conflictList"]

## Caching

- Fetched Results Controller: listens for context changes. Cache name and deleteCacheWithName:
- background fetch to warm up the cache: set resultType to NSManagedObjectIDResultType. 

## Migrating Schemas

- Version number is a hint. Hash modifier tells if the model is different.
- Class name, transient proerties, user info, validation predicates, default values will NOT trigger a migration.
- Download previous app store version to test migration.
- Automatic migration.
- Heavyweight migration. Manually map and manipulate data. Every object loaded into memory for checking default values against another value.
- Infer mapping model. Not as magical as it seems. Model upgrades can skip versions. 
- Manual mapping. More complex scenarios. Code is needed for sequential migrations.
- AL Iterator class for sequential mapping
- Test migrations with unit tests.
- Don't assume user is using the current version only

## Undo Management

- NSUndoManager. It is nil by default on iOS. Built-in support for NSManagedObjectContext.

## Performance

- com.apple.CoreData.sqldebug 1
- Base.app for opening sqlite file directly
- predicates: contains, endswith are slow.
- Use autoreleasepools for large batch operations
- use reset when you want to flush everything out of the context
- refreshObject:mergeChanges:
- Updates the persistent properties of a managed object to use the latest values from the persistent store.
- Use abnormally large test datasets.
- github.com/astralbodies

# Stupid Video Tricks - Chris Adamson

- AVFoundation for working with time base media
- Replacement for Quicktime for Mac : deprecated as of Mavericks
- AVAssetReader: lets you read raw samples.
- AVAssetWriter: lets you write raw samples.
- AVCaptureSessionDataOutput : callbacks
- AVPlayerLayer - subclass of calayer
- AVFoundation is built on top of Core Media
- CMTime and CMTimeRange in fraction of a second
- Types to represent media samples. sample buffers and block buffers.
- CMSampleBuffer. keep track of timing. contains either: cvimagebuffer or cmblockbuffer
- research AVAssetWriterInputPixelBufferAdaptor
- CMSampleBufferGetSampleAttachmentsArray
- kCMSampleBufferAttachmentKey_PostNotificationWhenConsumed
- Look at CMSampleBuffer.h
- AVAssetWriter: expectsMediaDataInRealTime
- CVImageBuffer - CVPixelBufferGetBaseAddress to work with bitmaps - wrap with lock and unlock
- CMSampleBuffer - Core Image Open GL- Core Audio
- Bob McCune: Learning AV Foundation
- QuickTime File Format Specification
- devforums good source of avfoundation info
- GPUImage is hardware optimized for 5S.

# Tips and Tricks of Effective iOS Developers - Ben Schierman

## General Tips

- Effective developers ship better software
- Always use braces for conditionals
- Use class extensions for private properties
- Use intention revealing method names
- Name single parameter bool arguments ex. showPanelAnimated
- Add comment documentation to public methods - use structured comment syntax - xcode will pick it up
- Lazily initialize properties - leads to a cleaner viewDidLoad - can also set to nil in didRecieveMemoryWarning
- Use refactor method judiciosly - cellForRowAtIndexPath usual place - Understand dependencies
- objc-dependency-visualizier tool
- Reduce dependencies: loose coupling, programming to interfaces, dependency inversion, reduce god objects, reduce singletons
- With less dependencies you can more easily refactor and change your code, change implementation, add features.
- Slim down your classes - Try to impose limits on lines of code for methods, classes.

## Xcode Tips

- Label your views in IB - Subject label, Timestamp label etc.
- keyboard shortcuts: command shift j, y, c  - command control j then command control left arrow to go back - control i to reindent - deliberately practice them - don't use cheatsheets, practice them
- snippets - propstr, propint,  mark prag snippet, tvds table view data source, swf - string with format

## Source Control

- use the command line - leverage guis for specific tasks : gitx
- commits should be a logical chunk - write a good commit message - github enforces 50 character commit subject limit
- branches are basically free in git
- Learn to rebase - git pull --rebase, you can make that setting a default setting in gitconfig for all - never rebase public branches
- git bisect - find when bugs were introduced in git history
- git reflog for fixing mistakes
- branch per feature - keep master releasable - don't veer too far from working software - try to break down your tasks so you are able to make a commit every hour

## Effective Habits

- keep an improvement list of things to work on
- have a side project - allow you to explore and do stupid things
- read other peoples code
- learn how to ask for help - don't ask five questions at once - reduce variables - don't send a help email to 5 different people
- program in other languages - learn from other communities
- write more tests
- go forth and be effective - share what you learn with others

# View Controller Transitions - Jonathan Blocksom

## Basic Architecture 

- break it down  - nav controller - add a navigation delegate - 
- implement UIViewControllerAnimatedTransitioning protocol
- use from and to view controllers
- you are given a container view to do the animation in
- apple provides the transition context and container view
- snapshotViewAfterScreenUpdates
- make sure to call completeTransition after animating

## Animation Methods

- uiview animations: bounce, keyframe - keyframe animation blocks can get messy since they are nested
- resizableSnapshotViewFromRect:afterScreenUpdates:withCapInsets: 
- high performance cache view - special layer.contents that can't be modified

## Other Contexts

- tab bar controller is similar - different delegate method, same object
- modal controllers - needs to be able to dismiss - animation controllers are reusable - UIModalPresentationCustom
- your own custom container controllers

## Interactive Transitions

- navigationController:interactionControllerForAnimationController:
- startInteractiveTransition
- UIPercentDrivenInteractiveTransition
- updateInteractiveTransition
- could cause viewWillAppear to be called but not viewDidAppear if you cancel - UIViewControllerTransitionCoordinator can aid with this situation
- animateAlongsideTransition:completion: help for progress animations

## CollectionView Transitions

- useLayoutToLayoutNavigationTransitions

# Parallel Computing with OpenCL - Personal, Heterogeneous, Parallel Computing - Jeff Biggus

- We still have vast untapped power on the desktop
- transistor count on chips still going up
- power and heat severly limits performance
- multicore movement in design
- problem: we are not parallel programmers - there are no good general parallel programming tools
- parallel is starting to come into its own
- SIMD - Single instruction, multiple data
- not all macs support cuda and glsl - opencl runs on all macs, supported graphics chips on iphones
- bottleneck is getting data to the graphics card
- work groups have 1 2 or 3 dimensions
- 1 - audio
- 2 - video
- 3 - 3d data
- buffers and images - two different kinds of data that opencl recognizes
- text search, financial data
- opencl can be called from different languages
- opencl C - vector data types - vector functions - math and geometric functions - data transfer functions, image and sampler functions
- gcl.h gcd + opencl
- pyopencl 

# Physics and the User Interface - UIKit Dynamics - Jonathan Penn - rubbercitywizard.com/stuff

## Dynamic Animations

- uikdy uses core animation - transformation, color
- animation curves - linear: moves at a constant rate - eased: mimic a swell or bell curve - bounce
- has a physics engine built-in tied to core animation
- approximate simulation of bodies moving around in the real world
- this is performance intensive so use judiciously and use only for subtlety
- reference view- items - items should be direct subviews of the reference view - dynamic animator- behaviors
- translatesReferenceBoundsIntoBoundary
- uidynamicbehavior action property
- objcio issue 5 - collectionviews and uikit dynamics
- dynamics catalog
- DMDynamicWaterfall
