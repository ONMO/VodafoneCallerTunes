![Onmobile: Logo](http://t0.gstatic.com/images?q=tbn:ANd9GcQ7a6C5baa2f_3KA2zVpouH29tMGgRfcCn1PGuubySgbFbKuMxg)

# Vodafone Callertunes SDK

- [Introduction](#introduction)
  - [Purpose](#purpose)
- [SDK Integration Steps](#sdk-integration-steps)
  - [CocoaPods](#cocoapods)
  - [Project settings](#project-settings)
  - [Initialize and Run Vodafone Callertunes SDK](#initialize-and-run-vodafone-callertunes-sdk)
- [Copy Right](#copy-right)

## Introduction

  ### Purpose

  This document describes systematic guidelines in integrating Vodafone Callertunes SDK framework along with its dependent libraries/frameworks.This document provides complete guidelines tointegrateVodafone Callertunes Framework in iOS project.

## SDK Integration Steps

  ### CocoaPods

  Vodafone SDK can be integrated to any iOS project through CocoaPods. You can refer [Cocoapods](https://guides.cocoapods.org/using/getting-started.html#getting-started) for more details.

  Command to install CocoaPods (If it is not already installed on your OS X)

```bash
$ sudo gem install cocoapods
```

  To integrate Vodafone Callertunes SDK into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '9.0'
use_frameworks!

target '<Your Target Name>' do
pod 'VodafoneCallerTunes', '~> 1.0.0'
end
```

  Then, run the following command on your project path:

```bash
$ pod install
```

  ### Project settings

  Post installing Vodafone Callertunes SDK to your project, please update the project settings by following below steps

  #### 1. Navigate to Project Target Info Tab

![Step1](https://github.com/ONMO/VodafoneCallerTunes/blob/master/Navigate%20to%20Project%20Target%20Info%20Tab.png)

  #### 2. Add following Properties in Custom iOS Target Properties list

![Step2](https://github.com/ONMO/VodafoneCallerTunes/blob/master/Add%20following%20Properties%20in%20Custom%20iOS%20Target%20Properties%20list.png)

  ### Initialize and Run Vodafone Callertunes SDK

  Use the following code to initialize and to run the Vodafone Callertunes SDK by passing the valid `MSISDN` number and valid `Key`

```swift
import VodafoneCallerTunesSDK

VodafoneCallerTunesConnector.initialize(withAuthenticationKey: <key>, forPhoneNumber: <phoneNumber>, controller: self, animated: true) { (error) in
// Write error handling code here
}
```

## Copy Right

### ©2018 OnMobile Global Limited All Rights Reserved.
