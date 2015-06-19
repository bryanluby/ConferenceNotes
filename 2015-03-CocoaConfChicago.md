# CocoaConf Chicago 2015 Notes

## Links

- http://t.co/Vd2OieNz3d - midi demo

## Extensions Programming Workshop - Chris Adamson

- Separate processes
- Today extension autolayout differences:  return size or push out your container
- Custom keyboards must provide `advanceToNextInputMode`
- `NSExtensionMainStoryboard`

## Core Bluetooth - Will LaFrance

### Bluetooth classic

- IOBluetooth
- IOBluetoothdeviceinquiry
- External accessary framework
- MFi program

### Bluetooth Low Energy (BLE)

- Low bandwidth, low energy, low cost
- ISM band - same band as wifi and microwave
- 40 channels
- roles: central(master) - peripheral (slave) - ibeacons are peripheral
- attribute protocol
- characteristic: smallest peice of data
- profile - a use case or application - example: heart rate profile

### Core Bluetooth

- CBCentralManager - wait for .PoweredOn
- Scan for peripherals with services
- keep strong ref to peripheral
- CBPeripheralDelegate for discovering services
- discover characteristics 
- write a new value
- subscribe to notification - notification vs indication
- further reading - bluetooth low energy: the developers handbook - bluetooth for developers(apple)
- beware of targeting 8.0-8.1 for core bluetooth - very buggy - improved in latest betas
- LightBlue app on appstore for peripheral discovery

## Modern Table Views in iOS 8 - James Dempsey

### interactive transition animation

- animateAlongsideTransition

### dynamic table views

- dynamic type size setting in settings app
- table cell automatic sizing - set `estimatedRowHeight`, `rowHeight = UITableViewAutomaticDimension` - the tableview will use auto layout to calculate height
- `preferredContentSizeCategory`
- make sure to set minimum cell height
- semantic text styles - `preferredFontForTextStyle` - get automatic support for any future changes of default system font.

### UISearchController

## Speaking in Types: How I learned to Stop Worrying and love the type system - TJ Usiyan @griotspeak

- What is a type: How we *describe* our data that our system works with.
- Result, Either - "make illegal states unrepresentable"
- Can use an enum with no cases as a namespace for static methods or type properties
- algebraic data types -
- Functions are maps
- parametric polymorphism, trait polymorphism
- no support for higher kinded types

## Solving problems with Auto Layout - Jack Cox

- scrollviews don't have an instrinsic size
- Create category on uiview with IBInspectable properties that act as a proxy property

## Hands on With Adaptive Layout

## Playing and Learning in Playgrounds - Daniel Steinberg

## 3D Math Primer - Janie Clayton

- Normalized coordinate systems - percentage between 0.0 - 1.0 - (0,0) - (1,1) - colors work similarly 100/255 rgb values

- Algorithm rosetta stone - math,logic,code
- trig - triangles foundation of 3d graphics
- linear algebra - perform an acton on many values at the same time - must be consistent across all values - optimized for prallel math 
- vector data types vec2, vec3 etc - matrix data types
- `CGAffineTransform` - alter size, position or rotation
- open gl need to include precision variable qualifiers `highp float ...`
- books - 3d math primer for graphics and game development - 3d math primer for graphics and game developmnent, khan academy - the nature of code - tho computational beauty of nature - fermat's enigma

## Who are you calling polymorphic - TJ Usiyan

### Parametric Polymorphism

- enforced ignorance
- its "parametric" because another type is the parameter
- Use assoctiated types when dealing with protocols - typealias

### Trait polymorphism

- deliberately limited knowledge - ex. a generic type that conforms to a protocol

### Ad-hoc polymorphism (function overloading)

- example `numericCast`
- generics as a means for liberating ignorance
- Be careful of getting generic too soon!
