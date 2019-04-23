# Swift by Midwest 2019

## Thoughts on Debugging - Mark Dalrymple @borkware

- Questions. Why? Bifurcation points in a problem space. How can you split a problem space in half?
- Questioning Modes
    - Solo questions. Build your own mental model of the system.
    - Pair debugging. Things asked to another programmer. Collaboratively build a mental model of the the system. This can make you *really* valuable to an organization. Applied socratic method.
- The 5Ws - who, what, when, where, why, ...... how? 
- 3Ws What, when, why
    - *What* is happening here?
    - *When* is something happening?
    - *Why* is something happening?
- Look for articulation points. Points where you can remove a node from a graph and cause it to become disconnected. Allows you to safely ignore parts of the problem space.
- Keep a log of what you have done and what you have found. Helpful for yourself and your colleagues in the future.
- Use Xcode custom Quick Look inspector - `debugQuickLookObject`
- Swift 5 interpolation for better print debugging
- Command-Shift-D reveal into view debugger inspector

## I’m a Coder: Codable & NSCoding - Liz Marley @Adana

- gist.github.com/emarley
- https://developer.apple.com/documentation/swift/decodingerror
- Move decodable *struct* conformances to extensions. Also gives you back the default initializer!
- Try having separate bare-bones structs for api responses
- Use the NSSecureCoding versions of archiving/unarchiving
- NSCoding and Codable can be used *together* when using `encodeEncodable` and `decodeDecodable` methods.
- https://github.com/emarley/Codable
- https://github.com/emarley/ColorContrast

## Hey Siri, How do I Implement You - Jacob Van Order

- Leverage NSUserActivity
- Intents framework
- Make sure it is eligible for prediction and invocation phrase
- Make sure to localize your suggested phrase
- Setup entitlements
- INShortcut 
- Intents extension
- Intent is like a question from the user to Siri
- Can use parameters in intents definition file
- Only add eligible for prediction if it is relevant to your app
- Think about functionality that is deep in your app workflow but is still used
- Keep asynchronous calls as short as possible
- Make sure the shortcut actually benefits the user
- bit.ly/sirikitapps
- iOS Settings > Developer has Siri debugging options
- https://github.com/jacobvanorder/SwiftByMidwest2019_SiriKit

## Generic Swift - It Isn’t Supposed To Hurt - Rob Napier @cocoaphony

- https://github.com/rnapier/generics
- Don’t *always* start with a protocol
- It’s all about extensions
- How does a protocol allow me to write a generic algorithm
- Write concrete code *first*. *Then* work out generics when you find you need abstraction.
- Swift protocols (except Error) do not conform to themselves
- Mocks are a terrible way to design protocols
- Generalized existentials are more relevant to the standard library
- Don’t use a type eraser to get rid of a PAT (protocol with associated type)
- If something will need to go in an array a PAT will not work
- Equality implies substitutability
- Protocols are for algorithms

## Swift as Light - Jon - Tait Beason @bugkrusha

- Mostly visual demo + example code about 3D laser printer experiences

## Living the Monadstic Life - Daniel Steinberg

- Mostly code samples and crowd participation going over functional programming concepts

## Tool Builders For Life - Jaimee Newberry @jaimeejaimee

- "The process of discovery is more important than the solution"
- Breakdown occurs when clarity of vision is lacking.
- Create a “What’s important to me” list.
- jaimeejaimee.com/speaking - Speaking tips
- Iterate to improve
- picturethisclothing storytelling
- Steve jobs video on poking life and making tools that other people can use
- Why - what - work - iterate

## Crows Can Understand Symbols, Can Apple’s Vision Framework - Jen Kelley @thehulkstoy

- Vision framework to use image recognition on a knitting chart
- Image orientation is important for accurate processing
- CoreML with Vision announced at WWDC 2018
- CreateML for easy model creation
- CreateMLUI framework can show live view in Swift Playgrounds
- Consider consulting with a data scientist before training your model to remove any potential bias
- https://github.com/jenkelley/TextPlay

## Wh@t is th@t - Mark Dalrymple @borkware

- Attributes: examples @IBOutlet @UIApplicationMain @testable
- Language feature: @discardableResult, @escaping, @noreturn, @autoclosure, @dynamic
- Interoperability: @objc, @objc(methodName), @objcMembers, @convention
- Fine Control: @_semantics, @transparent, @unsafe_no_objc_tagged_pointer
- Platform Peculiarities: @IBOutlet, @IBAction, @available, @UIApplicationMain
- How does it work? Source Code -> Abstract Syntax Tree -> Object Code
    - SIL: Source Code -> AST -> LLMV IR -> Object Code
    - apple/swift/docs directory for compiler docs: https://github.com/apple/swift/tree/master/docs
    - find unix command: change to your directory - “find . -type f -exec grep Something {}\; -print” search current directory for files, for the file execute the grep command using the file path, printing the filename. Faster alternatives: ack, ag, rg
    - Can be helpful to use a text editor with a built-in shell

## A Promise for a Better Future - Ben Scheirman @subdigital

- Promises
    - PromiseKit examples
    - https://github.com/mxcl/PromiseKit
    - Chaining support, Collecting values, concurrent promises, timing delay, error recovery, retry support
- Futures
    - Frequently seen in Vapor and Swift NIO 
    - A future is a read-only container for a value that has not arrived yet
    - Your code will typically make promises but return futures
- Async / Await
    - Part of the current swift concurrency manifesto
    - https://gist.github.com/lattner/429b9070918248274f25b714dcfc7619
    - Probably not part of Swift 6

# The Swift Name Game - James Dempsey @jamesdempsey

- Audience participation trivia game going over Swift API naming guidelines
- https://swift.org/documentation/api-design-guidelines/
