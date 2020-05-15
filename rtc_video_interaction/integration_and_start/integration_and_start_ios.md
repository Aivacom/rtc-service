# Real-Time Video Call

This section describes how to use basic functions of Thunder video SDK to implement video call. To access more functions, refer to information about advanced functions or turn to access personnel for help.

## 1. Demo Experience

Click [Download Demo Experience](https://apps.apple.com/cn/app/%E5%B0%9A%E4%BA%91%E4%BA%92%E5%8A%A8/id1471967129)

## 2. Prerequisites

Before you start, ensure that the following are available:

- Xcode 9.0+
- iOS 8.0+ prototype (use a prototype to run example codes. Simulators may fail to run some example codes due to incomplete functions.)
- Valid AIVACOM account (valid APPID and APPSECRET). Please contact technical support for details

## 3. Preparing the Development Environment

After the preceding prerequisites are met, SDK development can be started.

### 3.1 Creating a Project

1. Start **Xcode**. Click **Create a new Xcode project**.
2. Select **Single View App** for project type and click **Next**.
3. Fill in project information, including project name, information about the development team, organization name, and language. Then click **Next**. 
   **Note**: If no information about a development team is added before, you will see the Add account... button. Click this button and log in by using Apple ID as prompted. After login, select your account as the development team.
4. Select the project storage path and click **Create**.
5. Connect your iOS device to the computer.
6. Choose TARGETS > Project Name > General > Signing. Select Automatically manage signing. Click Enable Automatic in the displayed menu. 
   ![Configuration diagram](/rtc_video_interaction/resources/iOS1.png)

### 3.2 Integrating SDK

**Note**: `In versions later than v2.5.1`, SDK relies on the `AFNetworking` third-party library and the version is later than `3.2.0`

- For API Development Manual, visit: [iOS API](/rtc_video_interaction/api/iOS/v2.7.0/category.md)
- For Development Reference Demo, visit: [Demo Downloading](https://github.com/Aivacom/JLYMeet/tree/master/JLYMeet-ios)

Integrate ThunderBolt SDK to your project.

1. Install CocoaPods. Type the following command in the terminal:

```shell
brew install cocoapods
```

- If you have installed CocoaPods and Homebrew in the system, skip this step.
- If the terminal displays -bash: brew: command not found, you need to install Homebrew first and then type the command. For details, see [Homebrew Installation](https://brew.sh/index.html).

2. Create the Profile file.

Type the project path in the terminal and type the following command. After command execution, a Podfile text file will be displayed under the project path.

```shell
pod init
```

3. Add reference of ThunderBolt SDK.

**The latest thunder ios version is 2.7.8**

Open the Podfile file and change the file content to the following. Note: `YourApp` is your Target name and you need to add source and SDK version.

```ruby
#Uncomment the next line to define a global platform for your project
platform :ios, '9.0'

source 'https://github.com/CocoaPods/Specs.git'    #Add item
source 'https://github.com/yyqapm/specs.git'       #Add item

target 'YourApp' do
    # Uncomment the next line if you're using Swift or would     like to use dynamic frameworks
    # use_frameworks!

    # Pods for YourApp
    pod 'thunder','2.7.8' #Add item，'2.7.8' is thunderbolt sdk version number, and modified according to the version number introduced specifically
```

4. Install ThunderBolt SDK.

Type the following command in the terminal to procede with the installation:

```shell
pod update
```

- If the terminal displays Pod installation complete!, the library has been automatically added and pod will automatically configure all system libraries that the SDK relies on. Click to open the YourApp.xcworkspace file.

### 3.3 Adding app Permissions

1. To ensure normal running of SDK, authorize the microphone and camera of the device before using ThunderBolt SDK. Open info.plist and click the + icon to add permissions:

- Choose Privacy - Microphone Usage Description and fill in the purpose to use the microphone, for example, Video Chat.
- Choose Privacy - Camera Usage Description and fill in the purpose to use the camera, for example, Video Chat. 
   ![info.plist configuration](/rtc_video_interaction/resources/IOS3.png)

2. Enable background mode as required by the project. After entering background mode, the iOS device can still run related functions.

![Set background mode](/rtc_video_interaction/resources/iOS2.jpg)

## 4. Real-Time Video Interaction

After SDK integration, real-time video call can be implemented by SDK. The following figure shows the time sequence of API calling during a video call:

![Time sequence of real-time video call](/rtc_video_interaction/resources/sequence.png)

### 4.1 Creating and Initializing the ThunderEngine Instance

Before calling other SDK APIs, call [createEngine](/rtc_video_interaction/api/iOS/v2.7.0/category.md#createengine) to create and initialize the ThunderEngine object. 
Fill in the app ID of the project in this step. Refer to the following steps to create a project and obtain [App ID] in AIVACOM Control Station.

```objc
+(instancetype _Nonnull)createEngine:(NSString* _Nonnull)appId
                              sceneId:(NSInteger)sceneId
                             delegate:(id<ThunderEventDelegate> _Nullable)delegate;
```

For detailed information, see descriptions about [createEngine](/rtc_video_interaction/api/iOS/v2.7.0/category.md#createengine) in API Document.

### 4.2 Setting SDK Media Mode

```objc
- (int)setMediaMode:(ThunderRtcConfig)mode;


### 4.3 Joining room

​```objc
-(int)joinRoom:(NSString* _Nullable)token
      roomName:(NSString* _Nonnull)roomName
           uid:(NSString* _Nonnull)uid;
```

Join a room. This step allows a user to join a call room. Users in this room can communicate with each other or engage in group chat. Apps using different App IDs are not interoperable. If a call is ongoing, the user must call leaveRoom to exit the current call before joining another room.

For detailed information, see descriptions about [joinRoom](/rtc_video_interaction/api/iOS/v2.7.0/category.md#joinroom) in API Document.

### 4.4 Setting Video Encoding Attribute

```objc
- (int)setVideoEncoderConfig:(ThunderVideoEncoderConfiguration* _Nonnull)config;
```

Set video encoder’s property. 
SDK will acquire specific video encoding parameters for video encoding from the configured server in accordance with parameter configuration. If the service entails special parameter demand for video encoding, contact Technical Support for personalized configuration. 
If the video has been published, update the video encoding parameters. The updated video effect can be seen from local review and remote subscription. 
ThunderVideoEncoderConfiguration consists of two members.

For detailed information, see descriptions about [setVideoEncoderConfig](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setvideoencoderconfig) in API Document.

### 4.5 Setting Local View

```objc
- (int)setLocalVideoCanvas:(ThunderVideoCanvas* _Nullable)local;
```

You can preview and publish without setting this window. You can see locally captured pictures by setting this window.

For detailed information, see descriptions about [setLocalVideoCanvas](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setlocalvideocanvas) in API Document.

### 4.6 Enabling Video Preview

```objc
- (int)startVideoPreview;
```

Enabling preview will also enable the camera and data collection.

For detailed information, see descriptions about [startVideoPreview](/rtc_video_interaction/api/iOS/v2.7.0/category.md#startvideopreview) in API Document.

### 4.7 Enabling/Disabling Local Video Sending

```objc
- (int)stopLocalVideoStream:(BOOL)stopped;
```

Enabling local video sending means to send locally collected and encoded data to the server.

For detailed information, see descriptions about [stopLocalVideoStream](/rtc_video_interaction/api/iOS/v2.7.0/category.md#stoplocalvideostream) in API Document.StopLocalVideoStream can only be called after receiving the callback of onJoinRoomSuccess.

### 4.8 Disabling Video Preview

```objc
- (int)stopVideoPreview;
```

After video preview is disabled, video data collection will be stopped. Audience that subscribes to this anchor will fail to play video.

For detailed information, see descriptions about [stopVideoPreview](/rtc_video_interaction/api/iOS/v2.7.0/category.md#stopvideopreview) in API Document.

### 4.8 Leaving a Room

```objc
- (int)leaveRoom;
```

Leave a room. 
Leaving room indicates hang off or exiting conversation. After joinRoom is called, the user must call leaveRoom to stop the call before starting another call. No matter whether the user is idle or in a call, leaveRoom can be called without generating adverse effects. This method can release all resources related to conversation.

For detailed information, see descriptions about [leaveRoom](/rtc_video_interaction/api/iOS/v2.7.0/category.md#leaveroom) in API Document.

## 5. API Reference

- [createEngine](/rtc_video_interaction/api/iOS/v2.7.0/category.md#createengine)
- [joinRoom](/rtc_video_interaction/api/iOS/v2.7.0/category.md#joinroom)
- [setArea](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setarea)
- [setMediaMode](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setmediamode)
- [setRoomMode](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setroommode)
- [setLocalVideoCanvas](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setlocalvideocanvas)
- [setVideoEncoderConfig](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setvideoencoderconfig)
- [startVideoPreview](/rtc_video_interaction/api/iOS/v2.7.0/category.md#startvideopreview)
- [stopVideoPreview](/rtc_video_interaction/api/iOS/v2.7.0/category.md#stopvideopreview)
- [stopLocalVideoStream](/rtc_video_interaction/api/iOS/v2.7.0/category.md#stoplocalvideostream)
- [setRemoteVideoCanvas](/rtc_video_interaction/api/iOS/v2.7.0/category.md#setremotevideocanvas)
- [leaveRoom](/rtc_video_interaction/api/iOS/v2.7.0/category.md#leaveroom)
- [destroyEngine](/rtc_video_interaction/api/iOS/v2.7.0/category.md#destroyengine)

