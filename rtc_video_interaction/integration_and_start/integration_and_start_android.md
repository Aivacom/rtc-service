# Real-Time Video Call

This section describes how to use basic functions of Thunder video SDK to implement video call. To have deeper understanding of the functions, refer to information about advanced functions or turn to access personnel for help.

## 1. Demo Experience

Click [Download Demo Experience](http://resource.sunclouds.com/JLYMeet-2.8.0-1293-SNAPSHOT-5-official.apk)

## 2. Prerequisites

Before you start, ensure that the following are available:

- Android Studio 3.0 or higher
- Android SDK API 16 or higher
- Mobile device running Android 4.1 or higher
- Valid AIVACOM account (valid APPID and APPSECRET). Please contact technical support for details 

## 3. Preparing the Development Environment

After the preceding prerequisites are met, SDK development can be started.

### 3.1 Creating a Project

1. Start **Android Studio**. Click **Start a new Android Studio project**.   
2. On the **Choose your project** window, choose **Phone and Tablet** > **Empty Activity**. Then click **Next**.   
3. On the **Configure your project** window, specify the following fields:
- **Name**: Fill in the Android project name, for example, mouselive-android
- **Package name**: Fill in the package name of the project, for example, com.aivacom.mouselive
- **Project location**: Fill in the project storage path
- **Language**: Select the programing language, for example, Java
- **Minimum API level**: Select the lowest API level

4. click **Finish**. Install required plug-ins as prompted and wait for project synchronization completion

### 3.2 Integrating SDK

1. Locate build.gradle from the root directory of the project, open it, and add maven source:

```js
buildscript {
    repositories {
        maven { url "http://nexus.sunclouds.com:8081/nexus/content/groups/public/" }
        ......
    }
}

allprojects {
    repositories {
        ......
        maven { url "http://nexus.sunclouds.com:8081/nexus/content/groups/public/" }
        ......
    }
}
```

2. Add dependencies to modules that will use SDK:

```js
dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    //Add ThunderBolt sdk here
    api "com.rtc.thunder:thunderbolt:${thunder_version}"
    .....
}
```

3. Add permissions required by SDK to modules that will use SDK:

```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.xxx.xxxx">
    .....
    //Add permission
    <uses-permission android:name="android.permission.BLUETOOTH" />
    <uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
    <uses-permission android:name="android.permission.RECORD_AUDIO" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.WAKE_LOCK" />
    <uses-permission android:name="android.permission.CAMERA" />

    //Add software features
    <uses-feature android:name="android.hardware.audio.low_latency" />
    <uses-feature android:name="android.hardware.audio.pro" />
    <uses-feature android:name="android.hardware.microphone" android:required="true" />
    <uses-feature android:name="android.hardware.camera.autofocus" />
    <uses-feature android:name="android.hardware.camera" android:required="true" />
    <uses-feature android:name="android.hardware.camera.front" android:required="true" />
</manifest>
```

4. Anti-proguard codes:

If proguard has been enabled during app compilation, anti-proguard measures must be taken. Specifically, add the following information to the rule file proguard-rules.pro (/app/proguard-rules.pro) to prevent mixing public names in the library:

```js
-keep class com.rtc.thunder.** { *; }
-keep class org.webrtc.audioengine.** { *; }
-keep class com.yy.yyvideolib.** { *; }
-keep class com.yy.yyvideoplayer.** { *; }
-keep class com.yy.android.medialibrary.audiocodec.** { *; }
```

5. Click Sync to synchronize the project. The integration is completed.

## 4. Real-Time Video Call

After SDK integration, real-time video call can be implemented by SDK. The following figure shows the time sequence of API calling during a video call:

![Time sequence of real-time video call](/rt_video_interaction/resources/sequence.png)

### 4.1 Dynamic Permission Application

Call `checkSelfPermission`. When enabling Activity, check and obtain camera and microphone permissions of the mobile device.

```java
private static final String[] REQUEST_PERMISSIONS = new String[]{
        Manifest.permission.CAMERA,
        Manifest.permission.WRITE_EXTERNAL_STORAGE,
        Manifest.permission.READ_EXTERNAL_STORAGE,
        Manifest.permission.INTERNET,
        Manifest.permission.ACCESS_NETWORK_STATE,
        Manifest.permission.RECORD_AUDIO,
        Manifest.permission.MODIFY_AUDIO_SETTINGS,
        Manifest.permission.BLUETOOTH,
        Manifest.permission.BLUETOOTH_ADMIN
};

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_video_chat_view);


    if (checkSelfPermission(REQUESTED_PERMISSIONS[0], PERMISSION_REQ_ID) &&
        checkSelfPermission(REQUESTED_PERMISSIONS[1], PERMISSION_REQ_ID) &&
        checkSelfPermission(REQUESTED_PERMISSIONS[2], PERMISSION_REQ_ID)) {
      // TODO:
      // After obtaining permission, initialize SDK and join channel.
    }
}

private boolean checkSelfPermission(String permission, int requestCode) {
    if (ContextCompat.checkSelfPermission(this, permission) !=
            PackageManager.PERMISSION_GRANTED) {
        ActivityCompat.requestPermissions(this, REQUESTED_PERMISSIONS, requestCode);
        return false;
    }

    return true;
}
```

### 4.2 Creating ThunderEngine

Before calling other Thunder APIs, create and initialize the ThunderEngine object.

```java
ThunderEngine.createEngine(Context context,String appId,long sceneId,ThunderEventHandler handler);
ThunderEngine.setArea(isChina ?
                ThunderRtcConstant.AreaType.THUNDER_AREA_DEFAULT :
                ThunderRtcConstant.AreaType.THUNDER_AREA_FOREIGN);
```

For detailed information, see descriptions about [createEngine](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginecreateengine), [createWithLoop](/rtc_video_interaction/api/Android/v2.7.0/function.md#thunderenginecreatewithloop), and [setArea](/rtc_video_interaction/api/Android/v2.7.0/function.md#thunderenginesetarea).

When creating ThunderEngine, you need to monitor SDK events and status callback through [ThunderEventHandler](/rtc_video_interaction/api/Android/v2.7.0/notification.md#thundereventhandler) as required by the scenario. For example:

- Token status: [onTokenWillExpire](/rtc_video_interaction/api/Android/v2.7.0/notification.md#thundereventhandlerontokenwillexpire):

```java
public void onTokenWillExpire() {}
```

- Network status: [onConnectionStatus](/rtc_video_interaction/api/Android/v2.7.0/notification.md#thundereventhandleronconnectionstatus):

```java
public void onConnectionStatus(){}
```

- Publishing callback for remote users: [onRemoteVideoStopped](/rtc_video_interaction/api/Android/v2.7.0/notification.md#thundereventhandleronremotevideostopped)

```java
public void onRemoteVideoStopped(String uid, boolean stop) {}
```

You can process callback interfaces in ThunderEventHandler based on scenario requirements. For details, see [API Document](/rtc_video_interaction/api/Android/v2.7.0/category.md).

### 4.3 Setting Room Attribute and Joining a Room

Before joining a room, set room attribute to obtain better user experience.

**Note**: When joining a room, provide Token. For how to obtain Token parameters, see [Generating Token](../token_generator/token_generator.md).

```java
ThunderEngine.setMediaMode(isAudio ?
                ThunderRtcConstant.ThunderRtcProfile.THUNDER_PROFILE_ONLY_AUDIO :
                ThunderRtcConstant.ThunderRtcProfile.THUNDER_PROFILE_NORMAL);
ThunderEngine.setRoomMode(int mode);
ThunderEngine.setAudioConfig(int profile,int commutMode,int scenarioMode);
ThunderEngine.joinRoom(byte[] token, String roomName, String uid);
```

For detailed information, see descriptions about [setMediaMode](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetmediamode), [setRoomMode](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetroommode), and [joinRoom](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginejoinroom) in API Document.

### 4.4 Enabling Local Preview and Publishing

1. Enable local preview video:

```java
ThunderVideoCanvas canvas = new ThunderVideoCanvas(ThunderPreviewView view, scaleMode, uid);
ThunderEngine.setLocalCanvasScaleMode(scaleMode);
ThunderEngine.setLocalVideoCanvas(canvas);
ThunderEngine.startVideoPreview();
```

For detailed information, see descriptions about [setLocalVideoCanvas](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetlocalvideocanvas) and [startVideoPreview](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestartvideopreview) in API Document.

2. Publish local video:

```java
ThunderEngine.stopLocalVideoStream(false);
```

For detailed information, see descriptions about [stopLocalVideoStream](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestoplocalvideostream) in API Document.StopLocalVideoStream can only be called after receiving the callback of onJoinRoomSuccess.

3. Stop publishing local video:

```java
ThunderEngine.stopLocalVideoStream(true);
ThunderEngine.stopVideoPreview();
```

For detailed information, see descriptions about [stopLocalVideoStream](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestoplocalvideostream) and [stopVideoPreview](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestopvideopreview) in API Document.

During local publishing, users can set publishing parameters:

```java
ThunderEngine.setVideoEncoderConfig(ThunderVideoEncoderConfiguration yyVideoConfig);
```

For detailed information, see descriptions about [setVideoEncoderConfig](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetvideoencoderconfig) in API Document.

### 4.5 Receiving and Displaying Remote Video

If another user is publishing in the room where the local user resides, the local user will receive event callback of [onRemoteVideoStopped](/rtc_video_interaction/api/Android/v2.7.0/notification.html#thundereventhandleronremotevideostopped) in the callback of ThunderEventHandler:

```java

public void onRemoteVideoStopped(String uid, boolean stop) {}
```

After receiving the preceding event, the video of the remote user needs to be rendered:

```java
ThunderVideoCanvas canvas = new ThunderVideoCanvas(ThunderPlayerView view, int renderMode, String uid);
ThunderEngine.setRemoteVideoCanvas(canvas);
```

For detailed information, see descriptions about [setRemoteVideoCanvas](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetremotevideocanvas) in API Document.

### 4.6 Leaving the Channel

To stop a call, disable the app, or switch the app to the background, and call [leaveRoom](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderengineleaveroom) to leave the current call channel.

```java
int ret = mThunderEngine.leaveRoom();
For detailed description, refer to description of API Manual on [leaveRoom](/en/product_category/rtc_service/rt_audio_interaction/api/Android/v2.7.0/function.html#thunderengineleaveroom).
```

## 5. API Reference

- [createEngine](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginecreateengine)
- [createWithLoop](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginecreatewithloop)
- [joinRoom](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginejoinroom)
- [setArea](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetarea)
- [setSceneId](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetsceneid)
- [setMediaMode](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetmediamode)
- [setRoomMode](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetroommode)
- [setLocalVideoCanvas](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetlocalvideocanvas)
- [setVideoEncoderConfig](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetvideoencoderconfig)
- [startVideoPreview](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestartvideopreview)
- [stopVideoPreview](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginestopvideopreview)
- [setRemoteVideoCanvas](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginesetremotevideocanvas)
- [leaveRoom](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderengineleaveroom)
- [destroyEngine](/rtc_video_interaction/api/Android/v2.7.0/function.html#thunderenginedestroyengine)

## 6. Precautions

Pay attention to the following during integration

- If no Looper is specified for callback, SDK callback will be implemented in the thread where SDK is created.
- Returned value of the interface: 0: calling success, < 0: calling failure
