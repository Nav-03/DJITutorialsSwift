# iOS-ImportAndActivateSDKInXcode-Swift

## Introduction

This demo is designed for you to learn how to import and activate DJI SDK in your Xcode project using Swift.

## Requirements

 - iOS 9.0+
 - Xcode 8.0+
 - DJI iOS SDK 4.16

## SDK Installation with CocoaPods

Since this project has been integrated with [DJI iOS SDK CocoaPods](https://cocoapods.org/pods/DJI-SDK-iOS) now, please check the following steps to install **DJISDK.framework** using CocoaPods after you downloading this project:

**1.** Install CocoaPods

Open Terminal and change to the download project's directory, enter the following command to install it:

~~~
sudo gem install cocoapods
~~~

The process may take a long time, please wait. For further installation instructions, please check [this guide](https://guides.cocoapods.org/using/getting-started.html#getting-started).

**2.** Install SDK with CocoaPods in the Project

Run the following command in the project's path:

~~~
pod install
~~~

If you install it successfully, you should get the messages similar to the following:

~~~
Analyzing dependencies
Downloading dependencies
Installing DJI-SDK-iOS (4.16)
Generating Pods project
Integrating client project

[!] Please close any current Xcode sessions and use `ImportSDKDemo.xcworkspace` for this project from now on.
Pod installation complete! There is 1 dependency from the Podfile and 1 total pod
installed.
~~~

> **Note**: If you saw "Unable to satisfy the following requirements" issue during pod install, please run the following commands to update your pod repo and install the pod again:
>
> ~~~
> pod repo update
> pod install
> ~~~

**3.** Header Search Paths Settings

Please delete all the paths in **Header Search Paths** except `$(PODS_ROOT)/Headers/Public` in **Build Settings** to help fix the Swift compiler error: **Inclue of non-modular header inside framework module 'DJISDK'**.

## Tutorial

For this demo's Objective C tutorial: **Integrate SDK into Application**, please refer to <https://developer.dji.com/mobile-sdk/documentation/application-development-workflow/workflow-integrate.html>.

## Feedback

We’d love to hear your feedback on this demo and tutorial.

Please use **DJI Developer Forum** [dji-forum](https://forum.dji.com/forum-139-1.html?from=developer) or **email** [dev@dji.com](dev@dji.com) when you meet any problems of using this demo. At a minimum please let us know:

* Which DJI Product you are using?
* Which iOS Device and iOS version you are using?
* A short description of your problem includes debugging logs or screenshots.
* Any bugs or typos you come across.

## License

iOS-ImportAndActivateSDKInXcode-Swift is available under the MIT license. Please see the LICENSE file for more info.

## Join Us

DJI is looking for all kinds of Software Engineers to continue building the Future of Possible. Available positions in Shenzhen, China and around the world. If you are interested, please send your resume to <software-sz@dji.com>. For more details, and list of all our global offices, please check <https://we.dji.com/jobs_en.html>.

DJI 招软件工程师啦，based在深圳，如果你想和我们一起把DJI产品做得更好，请发送简历到 <software-sz@dji.com>.  详情请浏览 <https://we.dji.com/zh-CN/recruitment>.
