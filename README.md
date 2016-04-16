# AELog
**Simple, lightweight and flexible debug logging framework written in Swift**

[![Language Swift 2.2](https://img.shields.io/badge/Language-Swift%202.2-orange.svg?style=flat)](https://swift.org)
[![Platforms iOS | watchOS | tvOS | OSX](https://img.shields.io/badge/Platforms-iOS%20%7C%20watchOS%20%7C%20tvOS%20%7C%20OS%20X-lightgray.svg?style=flat)](http://www.apple.com)
[![License MIT](https://img.shields.io/badge/License-MIT-lightgrey.svg?style=flat)](https://github.com/tadija/AELog/blob/master/LICENSE)

[![CocoaPods Version](https://img.shields.io/cocoapods/v/AELog.svg?style=flat)](https://cocoapods.org/pods/AELog)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-brightgreen.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Swift Package Manager compatible](https://img.shields.io/badge/Swift%20Package%20Manager-compatible-brightgreen.svg)](https://github.com/apple/swift-package-manager)

If you find yourself in upcoming statements, then you probably want to use **AELog**:  
> - I just want to log anything to console while working on a project, then turn it off when going live.  
> - I'd like to enable / disable logging on a file level, and also to format log lines just the way I like.  
> - I don't want to have anything other then that, I just want to be up and running in no time.

## Index
- [Features](#features)
- [Usage](#usage)
	- [One more thing](#one-more-thing)
- [Requirements](#requirements)
- [Installation](#installation)
- [License](#license)

## Features
- **Top level logging** which can be disabled when needed
- Enable or disable logging **on a file level**
- **Customizable format and verbosity** of log lines
- Covered with **unit tests**
- Covered with [docs](http://cocoadocs.org/docsets/AELog)

## Usage

Still there? All right, this is how you would use it:

```swift
aelog("hi there")
```

For example, if you added this on line 21 in `viewDidLoad` of your `ViewController`, this is how your output might look:

```
2016-04-03 21:08:00.123 -- [Main] ViewController (21) -> viewDidLoad() > hi there
```

Ok, now for the pro-users which might want to disable logging when going live, choose between files that are making the output and ones that don't, or maybe customize format and verbosity of the log lines, this is how you can **configure AELog**:

1. Create `AELog.plist` file and add it to your target (you can also drag one from the **AELogDemo** example project).
2. Configure any possible settings the way you want:

	Key | Type | Description
	------------ | ------------- | -------------
	Enabled | Boolean | Logging enabled flag. (defaults to `YES`)
	Files | Dictionary | Key: file name, Value: Boolean (defaults to empty - all files log enabled)
	DateFormat | String | Date format which will be used in log lines. (defaults to `yyyy-MM-dd HH:mm:ss.SSS`)
	Template | String | Log lines template. (defaults to `{date} -- [{thread}] {file} ({line}) -> {function} > {message}`)
	
That's all there is. You're the master of `AELog` now. Happy coding!

### One more thing

Have you ever wanted to see the output of your app while you're not at your computer, like in real time directly on your iOS device? Yeah, me neither, but just in case you change your mind (I did), check out [AEConsole](https://github.com/tadija/AEConsole) - **customizable console UI overlay with debug log on top of your iOS app**. After all, `AELog` was made just to complement `AEConsole`. :)
	
## Requirements
- Xcode 7.3+
- iOS 8.0 | watchOS 2.0 | tvOS 9.0 | OSX 10.10

## Installation

- [CocoaPods](http://cocoapods.org/):

	```ruby
	pod 'AELog'
	```
  
- [Carthage](https://github.com/Carthage/Carthage):

	```ogdl
	github "tadija/AELog"
	```

- Manually:

  Just drag **AELog.swift** into your project and start using it.

## License
AELog is released under the MIT license. See [LICENSE](LICENSE) for details.