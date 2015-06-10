# AltConf Notes

## Misc

- github.com/flexmonkey

## Keynote panel discussion - iMore

- WatchKit - watchOS
- iPad split screen
- Wider adoption of Metal
- Apple music
- Split screen window management
- No Siri on the mac???
- Siri deep linking
- Safari view controller
- News - Flipboard got sherlocked
- Vastly improved 3rd party watch support
- Shift key fixed on ios keyboard
- ipad trackpad keyboard
- command tab app switching on ios
- Swift open source - linux (share client and server classes!!!)
- iOS low power mode switch
- watch complications

## Platforms state of the union

- Free native dev - only need appleid
- Single paid dev program!!!!!!
- 1.3 free space needed to install ios 9
- Hopes for faster ios adoption
- app thinning - 

## How indoor location will change your user experience - Scott Brewer @goawaygeek

- Various location aware museum app demos - users felt closer to the works in the museum that they saw - Bluetooth beacons - Core bluetooth
- EnsoLocate: location platform - simplifies the management of the objects in the museum space - public beta open now - "Indoor Location Made Easy" - ensolocate.com
- Their client needed a specific problem solved and not just a generic location platform solution
- They used almost 200 beacons that worked off a triangulation algorithm

## The Stylish Objective-C Developers Guide to Swift - Jaim Zuber @jaimzuber

- Swift is ready for prime time
- Careful with implicitly unwrapped optionals and nibs - Will crash in Swift and not objc if an outlet is nil
- let > var
- Non-optional > ? > !
- Use optionals only when they make sense
- heavy use of var and optionals is like writing objective-c in swift and getting the worst of both
- use small focused structs using all lets
- New patterns - Safety first - optional binding with if let - Networking, AlamoFire, SwiftyJSON - "if let all the things"
- Dependency management - carthage

## Design is Not for Designers - Joe Cieplinski

- Design is problem solving - asking the right questions is more important than anything
- we are more similar to architechts
- for whom do we design? Not designers but everyday people - they just want the app to work
- dribbble should not be just a portfolio page
- designers tend not to be as colloborative as developers - no equivalent to github and stack overflow - 
- read marc edwards blog for example of a designer sharing info
- wants to see designers share more info!
- Questions to ask: What does it do??? Is that something we should build??
- Use your talents to build something worthwhile
- Can we learn form the past without fetishizing it?
- Examples
    - Good - quotebook started with an empty data set, they wanted to make the entry point easier - make adding quotes easy
    - Not good - Flash over substance - video on websites - suprise but no delight - mac pro website messes with the typical scrolling experience - "highjacked scrolling" - rate my app
- Why does it matter? Make sure products succeed, help, and make users happy.
- We have been building throwaway apps

## Objective-C++: What could possibly go wrong? - Peter Steinberger

- every malloc is a mistake - segfaults everywhere
- What about Swift? Does not work directly with C++.
- binary compatibility for frameworks
- C++ - actively improved, geat tooling, cross-platform, fast!, powerful standard library, many 3rd-party libraries
- no Cocoapods compatibility
- auto and range-based for loops, shared_ptr, weak, labmdas, move semantics
- std::vector<CGPoint>
- initializer lists
- smart pointer - unique_ptr
- book on starting C++ - effective modern c++
- Objective-C++ - freely mix C++ and Objcs
- enable by renaming files to .hpp and .mm
- gotchas: compile time can be slow, stricter compiler, properties: use ivars and write accessors manually
- projects in objc++ - objc runtime, webkit, realm, pop, componentKit, djinni
- type safety with objective c generics
- effeciency - c++ is alot faster
- nil safety - vector allows nullptr
- inline blocks - auto handler for type inference with inline block variables
- Good lldb debugging support

## Designing for Fun - Sarah Allen @mightyverse

### Meaning

- Connect to personal goals and passions
- What is your epic win?

### Autonomy

- Freedom: the ability to curiosly explore opportunity
- play should be voluntary
- learning is our brains primary function - how can we design software so it is effortless learning to use it
- let people do things they already know how to do

### Mastery

- "Fun is just another word for learning under optimal conditions" - Ralph Koster
- relaxed alertness - the more you are stressed , the less you learn - moderate to high challenge - sense of well-being
- the compulsion loop - Stephanie Morgan - kill monsters -> Win gold -> Buy stuff -> repeat - content creation feedback loop

### Fun

- create a paper prototype
- play test and iterate - don't stop iterating until it is actually fun
- give someone your app, shut up and watch them use it - resist providing answers - ask questions instead: did you have fun, did you learn anything?
- build small things
- design in collaboration with your users

## Choose your character - Brianna Wu

- Nine ways to start helping and stop hurting women in tech "follow up" from last years talk
- Gamergate hate group aftermath
- Common senses of frustration for women - not enough lead positinos - not enough female protagonists in games
- women have exploded into the gaming industry
- she would rather be talking about game dev rather than all energy talking about women in tech
- Where did gamergate start? When anita sarkeesian started feminist frequency - let to negative response from gamers
- zoe quinn - depression quest
- men need to communicate with other men to raise conciousness about this issue
- @freebsdgirl
- men tend to go with a technical fix to a human problem - systems set up for men, by men
- no visibility in the media for women who play games

## Successful Test Driven Development on iOS Paul Zabelin, Glen Tregoning

- tests become executable docs that don't get out of date
- tdd produces great test coverage
- reduce manual testing time
- pair programming ping pong
- start where testing is easy
- don't test everything
- start with user acceptance tests
- acceptance tests - test happy path user scenarios and error cases
- prefer testing to public interface rather than testing private methods
- avoid complex mocking - if tests get too complex, consider moving your test to another level - unit -> integration -> accptance
- indigogo/simulatorsetup github repo

## Overloading Comparison - Ray Wenderlich

- Twitter success parade
- comparison robs of achievement
- feelings of comparison never went away - still to this day
- take daily stock of what is going right in your own life
- all of us have our own unique strengths and weaknesses - we are each on a unique track
- play to your strengths
- alot of success ends up being accidental
- overload the comparison operatior
- we are here to learn
- don't compare, learn from others

## Making users smile, laugh, and cry - Maxim Cramer

- meaning - people want a sense of direction in their life
- engagement - get lost in your work - flow
- pleasure - problem is adapting to the situation
- positive design - design to be a morally good person - pleasure - personal significance
- enhance how you feel about your self
- allow you to connect to others in a meaningful way
- visceral, behavioral, reflective
- visceral - gut instinct to things

## An OSS Education - Samuel Giddins

- amazed at a powerful tool like RestKit was free to use
- in open source, you don't need a set of prerequisites to contribute
- open source was the way he introduced himself as a developer to the community
- loves open source but loves where it took him: both as a dev and as a human being

## The Social Coding Contract - Justin Searls

- Open source is good right?

### Dependencies

- industrialization of open source
- open sources progress - jar files led to smaller focused dependencies which brought on the need dependency managers
- npm package manager - recursive dependecies
- long term fragility
- its always easy to start an app now, but fragile in the long run due to updating dependecies
- easy to start, but not simple
- risk of deep dependencies and version conflicts

### What it is like as a maintainer

- maintainers are just extra early adopters
- late adopters tend to have a sense of entitlement
- trolls - asymmetric power - trolls may be dominating the communicationn

### Trust

- how do we get people to trust us? Marketing!
- but large companies are spending  big mony on marketing
- recognize when projects are being marketed to you

### Future

- How we communicate - we are mostly just text on a screen
- better communication is also a troll repellant
- we need more live chant, live examples and pairing setssions
- most open source tools are a product of web development - not ideal for ios philosophy

## 7 ways to Enrich the Tech Industry - Aleen Simms

- not alot of women or diversity in the industry
- 15% of techical rolse are women
- 56% of women leave the industry
- 2% of tech workers are black
- 3% are latino
- less than or equal podcast

### Tips

0. recognize that its not about you - not everyone has the same experiences
1. listen to and believe us - women face criticism when they speak up
2. expand your network - seek out people from different backgrounds - don't argue with them - just listen and learn
3. amplify our voices - retweet them - link to them - give credit to them but don't speak for them
4. pass opportunities on to us - it costs little to pass these to underrepresented groups
5. pay attention to your language - alternative words lame: slow, crazy:unrealistic, turn a blind eye: they wer ignorant
6. be our ambassador - there are people who will listen only to you but not people from underrepresented groups - stand up with your support - add your voice
7. dont' hestitate to apologize - a sincire apology is to take responsibiity for your actions

## Swift Thinking - Natasha Murashev

### Learning

- Learning Swift can be challenging! - rewiring your brain
- Work with others - pair programming at her company was extremely helpful to her
- Teach - gives you a deeper level of learning - solidify knowledge - as fast as you learn it, teach it right away! That will be the most helpful to other people
- Put your stuff out there - it does not have to be perfect - gets feedback from other people
- Expose yourself to advanced topics
- Celebrate breakthroughs in your own learning - reward yourself while you can
- never put yourself in a position where youl be treated as foolish for learning

### Swift things

- value types
- optionals
- can use view models for handling mutable state
- new swift error handling
- testing - functional style can make things easier to test - @testable keyword - Quick testing framework

## Lessons in app PR: How to launch - Matt Ronge

- Launch starts at day 0
- how is what you are doing better or different than what is already out there
- book recomendation: the 22 immutable laws of marketing
- app website can be helpful
- polished video for astropad!
- put together a press kit - icons, logos, screenshots, product shots, team pictures, guide & quotes
- make a big press list - sites you want to be covered on - niche sites can often be better than general tech sites
- pick a launch date - ideally in the middle of the week
- Send individual emails and not mass emails to all contacts - make the email short! the contact can follow up for more details later if necessary
- book rec: the burned out bloggers guide to PR

## Imagine a fully diverse & inclusive world - Melinda Briana Epler @changecatalysts

- What happened to women in computer science?
- What could go wrong when we don't have diverse teams? Products built by men can be poorly designed when used by women.
- What is diversity? Inviting people to the table.
- What is inclusion? Inviting people to speak, participate and lead.
- What could go right? Numerous examples shown on slide of successful women-run companies.

## What Haskell Teaches Me About Swift - Amizer Nasir @abizern

- Why Haskell? Learning haskell will make you a better swift programmer!
- Type inference
- Favor immutable state over mutating values - valued don't change under you- esaier to maintian - more likely to be thread safe
- prefer structs over classes
- avoid mutating structs
- lists - don't iterate over a list - use higher order functions instead (map, filter, reduce)
- reduce is often enough rather than map - be careful though for sacrificing readability
- monads - is sort of like a burrito - a value in a context - optional is a context that contains a value or doesnt have a value - Result is the context that has  value or an error in getting that value
- The type system is your friend - strong types can fix a whole class of bugs - If it compiles, your moset of the way to solving your problem
- typealias is useful for making code clearer - it can also make higer order function dclarations easier to read.
- just looking at the types can make it easyer to reason about your problems
- keep code with side effeccs in one place
- functions all the way down - easier to test - very small functions can be easier to read
- higher order functions can reduce duplication in code
- map on optionals - applicative on optionals (optional functions) - bind on optinoals (flatmap)
- do we still need OOP? Sometimes need to deal with existing Cocoa apis that are more OOP.
- you you have pur funtions, is it worth worring about their access modifiers? Can you make thime bare functions instead?
- group together functions into a protocol
- Books: learn you a haskell for great good - real world haskell - Functional programming in swift - Maybe Haskell by Pat Brisbin
- With Cocoa now, we have the choice of two different approaches to the same problem space 
- Don't confuse complexity for unfamiliarity!

## Building in Success with Market First Development - Charles Perry @DazeEnd


