# FVCustomAlertView-Swift

Custom AlertView for iOS SDK. Port from [FVCustomAlertView](https://github.com/thegameg/FVCustomAlertView)

## Usage

To run the example project, clone the repo, open `FVCustomAlertView-Swift.xcworkspace`

## Requirements

* iOS7+ project
* ARC project

## Difference from FVCustomAlertView

* Remove blur to support iOS7, you can use the objective version to get that
* Add a thread-safe share singleton
* Add alertView to view's window to get fullscreen effect

## How to install FVCustomAlertView

Not have enough time, so only manual way now.

Copy the source file and resource images to your project

* FVCustomAlertView.swift
* FVCustomAlertViewResources/

## How to use FVCustomAlertView

Use `FVCustomAlertView.shareInstance`, it's a thread-saft singleton.

It comes with 4 default modes and a cutom mode.

The default modes are : (make sure you try them in the example app)

* Loading

![Loading](./Screenshots/loading.png)

```swift
FVCustomAlertView.shareInstance.showDefaultLoadingAlertOnView(self.view, withTitle: "Loading...")
```

* Done

![done](./Screenshots/done.png)

```swift
FVCustomAlertView.shareInstance.showDefaultDoneAlertOnView(self.view, withTitle: "Done")
```

* Error

![error](./Screenshots/error.png)

```swift
FVCustomAlertView.shareInstance.showDefaultErrorAlertOnView(self.view, withTitle: "Error", withSize: CGSizeMake(width: 200, height: 100))
```

* Warning

![warning](./Screenshots/warning.png)

```swift
FVCustomAlertView.shareInstance.showDefaultWarningAlertOnView(self.view, withTitle: "Be careful")
```

* Custom


![custom](./Screenshots/custom.png)

Let's add a `UISwitch`:

```swift
let sw = UISwitch()
sw.on = true
FVCustomAlertView.shareInstance.showAlertOnView(self.view, withTitle: "1 + 1 = 2 ?", titleColor: UIColor.blackColor(), width: 200, height: 150, backgroundImage: nil, backgroundColor: UIColor.orangeColor(), cornerRadius: 5, shadowAlpha: 0.1, alpha: 0.9, contentView: sw, type: .Custom)
```

## Resources

The resources (checkmark, cross, warning sign) comes from [http://www.iconfont.cn/](http://www.iconfont.cn/)

## Author

Garnel Mao (maogm12@gmail.com)

[http://maogm.com](http://maogm.com)

## License

This code is distributed under the terms and conditions of the [MIT license](LICENSE).
