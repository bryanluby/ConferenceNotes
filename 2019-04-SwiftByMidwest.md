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
- Use Xcode custom quicklook inspector - `debugQuickLookObject`
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
- settings > developer has Siri debugging options
- https://github.com/jacobvanorder/SwiftByMidwest2019_SiriKit

## Generic Swift - It Isn’t Supposed To Hurt - Rob Napier @cocoaphony

- https://github.com/rnapier/generics
- Don’t *always* start with a protocol
- It’s all about extensions - How does a protocol allow me to write a generic algorithm
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

- Mostly code samples and crowd participation

## Tool Builders For Life - Jaimee Newberry @jaimeejaimee

- The process of discovery is more important than the solution.
- Breakdown occurs when clarity of vision is lacking.
- Create a “What’s important to me” list.
- jaimeejaimee.com/speaking - Speaking tips
- Iterate to improve
- picturethisclothing storytelling
- Steve jobs video on poking life and making tools that other people can use
- Why - what - work - iterate
