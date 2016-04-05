+++
date = "2014-07-12T14:00:00+01:00"
draft = true
title = "Evolution of iOS"

+++

It's important to know when a specific feature was introduced in which iOS, especially when there are some backwards compatibility issues, that's the reason behind this article. I tried to make the descriptions of new features as short as possible, to give only a general idea.

## iOS 4.0

###  Multitasking

Apps go into background mode when user presses home button. Previous versions of iOS terminated the app. Most of the apps after going to background mode are being suspended but there are some exceptions:

* An application can request a finite amount of time to complete some important task.
* An application can declare itself as supporting specific services that require regular background execution time.
* An application can use local notifications to generate user alerts at designated times, whether or not the application is running.

The app which is in background mode can still be terminated due to some conditions for example low memory, therefore the applications must be ready to exit at any time.

### Blocks

Really great feature making source code cleaner and developer's live a lot easier. Block are segments of code that can be passed to methods and functions, get invoked, assigned to properties.

### GCD

Thread programming is hard, no question about it, how about making a simpler alternative which is really easy to use? That's where GCD (Grand Central Dispatch) comes in. No more blocking of main thread, apps are now more responsive (if written right)!

### Local Notifications
The app can issue a local notification, which will inform a user about an important event. Mostly used when the app is in the background mode.

### Event Kit
Provides an interface for accessing calendar events on a user’s device. You can use this framework to get existing events and add new events to the user’s calendar.
### Core Motion
How about getting info about iPhone state form motion-based sensors, and using it to build a game where you can manipulate a ball through rotating the device? Sounds great? You can do it with the use of Core Motion framework.

### Data Protection
Build in encryption can now be used when working with sensitive user data.
>When your application designates a particular file as protected, the system stores that file on-disk in an encrypted format. While the device is locked, the contents of the file are inaccessible to both your application and to any potential intruders. However, when the device is unlocked by the user, a decryption key is created to allow your application to access the file.

>Implementing data protection requires you to be considerate in how you create and manage the data you want to protect. Applications must themselves be designed to secure the data at creation time and to be prepared for changes in access to that data when the user locks and unlocks the device.

### Core Telephony
This framework provides interfaces for interacting with phone-based information on devices that have a cellular radio. Apps can get information about a user’s cellular service provider and be notified when call events occur.

### iAd
Advertisements framework allows a developer to monetize an app in different way.
Why would anyone spoil the app with ads?

### QuickLook Framework
The Quick Look framework for iOS, allows to preview the contents of files an app does not support directly.

### AV Foundation
That's the bomb! Very powerful framework which allows developers to do a ton of crazy stuff. Playing audio, video, recording and so on. You should definitely check it out!

### Asset Library
A framework which provide interface for retrieving a user’s photos and videos. Using this framework, you can access the same assets that are managed by the Photos application.

### Image I/O
Importing and exporting image data and image metadata.
>This framework is built on top of the Core Graphics data types and functions and supports all of the standard image types available in iOS.

### Core Media
Even more powerful than AV Foundation which is build on top of it. Check it out if you are interested in more low-level stuff.

### Cored Video
Funny apple description, they make it sound as some scary black magic is going on inside this framework. More reasons to check it out!
>The Core Video framework (CoreVideo.framework) provides buffer and buffer pool support for Core Media. Most applications should never need to use this framework directly.

## iOS 4.1
### Game Center
Games becoming more social with use of this framework. User can create it's own profile which will be universal. Leaderboards, matchmaking and achievements mean users will gets more fun interacting with each other.

## iOS 4.2
### Printing
iOS now incorporates support for wireless printing from iPhone and iPad applications.

### Air Play
Audio streaming to Apple TV and to third-party AirPlay speakers and receivers.

### Core MIDI
Provides a standard way to communicate with MIDI devices, including hardware keyboards and synthesisers.

### Weak Linking Support
System frameworks now tag their classes with availability information that the compiler can use to link weakly to those classes as needed. It is easer to check if the class is available at the runtime. Previously, you needed to use the NSClassFromString function to determine whether a class was present, now you can simply check for the existence the class directly with the use of *class* method. Generally speaking these feature makes life easier.

## iOS 4.3
### Air Play Video Support
Previous version added support for audio streaming, this allows streaming of video.

## iOS 5.0
### iCloud Storage
Really great feature build for easy access of your data by the NSA in mind. You will have an option to store all your data in a central location, where Apple will keep it 'secure'. Complete erosion of privacy... nah just kidding (or am I?).

### iCloud Backup
Easier restoration of apps through cloud backup, space is limited so send **only** the most important ones...

### Automatic Reference Counting
Memory management in Objective-C is based on retain count of objects, if retain count is greater than zero object resides in memory, when it gets down to zero the object gets dealloceted. It was developer responsibility to manage the retain count, with the introduction of ARC it is compiler responsibility.

### Storyboard
Previously if you didn't wanted create the controllers views programatically you could do it using nib files. Each controller had its own nib, storyboard captures your entire user interface in one place.

### Newsstand Support
Newsstand provides a central place for users to read magazines and newspapers.

### New Frameworks
#### GLKit Framework
Utility classes that simplify the effort required to create an OpenGL ES 2.0 app.

#### Core Image Framework
Really fast way to apply filters to images and video, uses CPU and GPU processing power. Really powerful.


#### Twitter Framework
Provides support for sending Twitter requests on behalf of the user and for composing and sending tweets. For requests, the framework handles the user authentication part of the request for you and provides a template for creating the HTTP portion of the request.


#### Accounts Framework
Provides system wide sign-on model for certain user accounts. Single sign-on improves the user experience, because apps no longer need to prompt a user separately for login information related to an account.


#### Generic Security Services Framework
Security related services to iOS apps. Very little info about this one in Apple's developer library, [rfc-2743](http://www.ietf.org/rfc/rfc2743.txt), [rfc-4401](http://tools.ietf.org/html/rfc4401)

#### Core Bluetooth
Framework allows developers to interact specifically with Bluetooth accessories.


## iOS 5.1
### Dictation support
>On supported devices, iOS automatically inserts recognised phrases into the current text view when the user has chosen dictation input. The new UIDictationPhrase class (declared in UITextInput.h) provides you with a string representing a phrase that a user has dictated. In the case of ambiguous dictation results, the new class provides an array containing alternative strings. New methods in the UITextInput protocol allow your app to respond to the completion of dictation.

## iOS 6.0
### Maps
Apple introduces it's own Map framework to challenge Google.Apps that do not incorporate their own map support now have an easier way to launch the Maps app and display points of interest or directions.

### Social Frameworks
Ever tired of having separate frameworks for Twitter, Facebook or Sina's Weibo?  Managing their versions and keeping everything up to date? Apple response is a framework which unifies all those services.

### Pass Kit
>Pass Kit is a new technology that uses web services, a new file format, and an Objective-C framework (PassKit.framework) to implement support for downloadable passes. Companies can create passes to represent items such as coupons, boarding passes, event tickets, and discount cards for businesses. Instead of carrying a physical representation of these items, users can now store them on their iOS device and use them the same way as before.

### Reminders
In previous version Event Kit allowed creation, deletion - general management of calendar events. Since iOS6 it will allow to use reminders.

### In-App Purchases
Introduction of freemium model and slow death of paid apps. User can now purchase additional content inside the app.

### Collection Views
Really great addition, it's worth to set deployment target to iOS6 (not iOS5) solely for this collection views. Easy way to create more robust user interface.

### UI State Preservation
Even when an app gets terminated by the operating system, its now possible to restore user interface to the state when it was last used.


### Auto Layout
More robust system than previously used "springs and struts" for laying out user interface elements.

### Data Privacy
In addition to location data, the system now asks the user’s permission before allowing third-party apps to access certain user data, including:

* Contacts
* Calendars
* Reminders
* Photo Library

## iOS 6.1
### Map Kit Searches
Developer is able to programmatically search for map-based addresses and points of interest.

## iOS 7.0
### User Interface Changes
#### UI Redesign
The iOS 7 user interface has been completely redesigned.Newly introduced flat design focuses on functionality and on the user’s content informs every aspect of design.


#### Dynamic Behaviours for Views
Introduction of physics based animation engine into iOS, more possibilities for creating crazy looking animations.


#### Text Kit
New version of iOS focuses more on content, Text Kit framework allows better management of text and typography.

### 64-Bit Support
When compiled for the 64-bit runtime, apps may run faster because of the availability of extra processor resources in 64-bit mode, they will also use more memory.

### Multitasking Enhancements
Apps can now fetch new content, after receiving silent push notification from a server. When fetching is complete, it can inform user about new podcast, tv show, podcast - all process done without user interaction.

### Games
#### Sprite Kit Framework
Games are big on App Store, till now there has been no Apple frameworks for creating them, only open source like [cocos2d](http://cocos2d.org).
In fact if you know cocos2d you will adapt the Sprite Kit very quickly.


#### Game Controller Framework
This framework standardises the use of third party game controller hardware.
>Game controllers can be devices connected physically to an iOS device or connected wirelessly over Bluetooth. The Game Controller framework notifies your app when controllers become available and lets you specify which controller inputs are relevant to your app.


#### Game Center Improvements
Exchanges which lets you create simultaneous turns, player chats, increased size of leaderboards or conditions in challenges.

### AirDrop
Sharing photos, document, URLs and other kinds of data with nearby iPhones, iPads or Macs.

### Inter-App Audio
>The Audio Unit framework (AudioUnit.framework) adds support for Inter-App Audio, which enables the ability to send MIDI commands and stream audio between apps on the same device. For example, you might use this feature to record music from an app acting as an instrument or use it to send audio to another app for processing. To vend your app’s audio data, publish a I/O audio unit (AURemoteIO) that is visible to other processes. To use audio features from another app, use the audio component discovery interfaces in iOS 7.

### Peer-to-Peer Connectivity
Framework for network peer-to-peer interaction between devices.

## iOS 7.1
### Support for External Media Players
>Apps can now receive and respond to events sent by an external media player. This process lets users interact solely with the external media player, removing the need to interact directly with an iOS device.


### OpenGL ES
Multithreading support added to OpenGL ES.

## iOS 8.0
### Swift
Introduction of new language called Swift, which is designed to be as productive as Ruby and as fast as Ansi C, Objective-C and C++. There are many features which will make this language great

* Clean syntax
* No headers and semicolons
* Multiple return values
* Generics
* Closures and much much more.

### App Extensions
Extensions allows custom functionality within a context of a user task. For example if user plays with Apple's photos app and want to share cool picture by your social app called Momo he simply can do it by an extension which you provided from photos app. No need to go to Momo specifically import image and than share it!

### Touch ID Authentication
More secure access to content inside an app, you can require a user to authenticated before proceeding.

### Photos
#### Photos Framework
Provides new APIs for working with photo and video assets, including iCloud Photos assets, that are managed by the Photos app. This framework is a more capable alternative to the Assets Library framework.

#### Manual Camera Controls
Long awaited feature, AV Foundation now allows for direct control of the camera focus, white balance and exposure settings!

### Games
Technology improvements in iOS 8 make it easier than ever to implement your game’s graphics and audio features. Some of the new additions are Metal (access to high performance A7 GPU), improvements in Scene Kit and Sprite Kit.

### Health Kit Framework
>Health Kit makes it easy for apps to share health-related information, whether that information comes from devices connected to an iOS device or is entered manually by the user. The user’s health information is stored in a centralised and secure location. The user can then see all of that data displayed in the Health app.


### Home Kit Framework
Framework for communicating with devices in a user's home. Easy way to discover devices and configure them.

### iCloud
#### Document-Related Data Migration
When users logs in to iCloud through device running iOS8 all the documents get migrated to a new version of the app's container directory. Devices running older operating systems will continue to have access to the original container, but changes made in that container will not appear in the new container and vice versa.

#### Cloud Kit
New great way to store users data without the need to setting up your own server, you have access to 1PB of disc space for free. Cloud Kit gives you control over when transfers occur. You can use Cloud Kit to manage all types of data.

#### Document Picker
>The document picker view controller grants users access to files outside your application’s sandbox. It is a simple mechanism for sharing documents between apps. It also enables more complex workflows, because users can edit a single document with multiple apps.


### Handoff
Handoff enables users to begin an activity on one device, then switch to another device and resume the same activity on the other device. For example, a user who is writing a document moves to an iOS device that's signed into the same Apple ID, and the same document automatically opens on iOS.

### Unified Storyboards for Universal Apps
One storyboard to rule them all, you no longer need to use separate storyboards for iPhone and iPad, also with adaptive controllers writing multi device apps will be easier than before.

There you have it, general evolution of iOS since version 4.0 to 8.0. Guys at Apple are working hard and I love how the iOS keeps getting better and better. I can't wait to see what the next version will bring!
