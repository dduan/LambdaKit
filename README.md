# ClosureKit

Closures make code clear and readable. You can write self-contained, small snipets of code instead of having the logic spread throughout your app,  Cocoa is moving slowly to a block/closure approach but there are still a lot of Cocoa libraries (such as UIKit) that don't support Closures. ClosureKit hopes to facilitate this kind of programming by removing some of the annoying - and, in some cases, impeding - limits on coding with closures.

## Requirements

 * iOS 7.0+
 * Xcode 8.3

ClosureKit can 

## Installation

[CocoaPods](http://cocoapods.org) is a dependency manager for Cocoa projects.

CocoaPods 0.36 adds supports for Swift and embedded frameworks. You can install it with the following command:

```bash
$ gem install cocoapods
```

To integrate Alamofire into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'
use_frameworks!

pod 'Alamofire', '~> 1.1'
```

Then, run the following command:

```bash
$ pod install
```

## Usage

### UIControl

Closure control event handling for UIControl

Example:

```swift
let button = UIButton.buttonWithType(.System) as! UIButton
button.addEventHandler(forControlEvents: .TouchUpInside) { button in
    println("Button touched!!! \(button)")
}
```

### UIGestureRecognizer

Closure functionality for UIGestureRecognizer.

Example: 

```swift
let doubleTap = UITapGestureRecognizer { gesture, state in
    println("Double tap!")
}
doubleTap.numberOfTapsRequired = 2
self.addGestureRecognizer(doubleTap)
```