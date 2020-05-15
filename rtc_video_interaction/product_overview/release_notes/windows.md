# Release Note Log

This section provides release update description to the audio/video SDK product.

## Overview

Version of the latest audio/video SDK product running on Windows is v2.7.0.

Two service product types are available. For their key features and charging rules, click the following links:

- [Real-time audio interaction](/en/product_category/rtc_service/rt_audio_interaction/product_overview/product/product.md)
- [Real-time video interaction](/en/product_category/rtc_service/rt_video_interaction/product_overview/product/product.md)

We offer complete user access documents for your quick access to audio/video capabilities. To know detailed integration methods, interface descriptions, and related scenario demos, click the following links:

- SDK integration to App: [SDK Integration Methods](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=DEPLOYMENT&title=Windows&version=blank&parentId=761)

- API Development Manual:  [Windows API](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows)

- Downloading related demos: [SDK and Demo downloading](http://resource.sunclouds.com/SunClouds_ThunderBoltSdk_PC_v2.5.4_20200210110521.zip)

## v2.7.0

### Version Overview

This version is released on March 19, 2020.

In this version, usability of publishing interfaces are improved to optimize the publishing procedure. Major interfaces for audio/video publishing have been adjusted and optimized, and publishing behaviors on mainstream platforms (android, iOS, and windows) are unified. 
In addition, to facilitate monitoring on the running status of audio/video services, callback information related to audio/video streams and equipment is added, allowing more transparent and detailed information to be transmitted to services. 
The issue of SDK power consumption in case of multiple people connected on microphone on mobile clients has been improved. Multi-person microphone connection view has been added. Specifically, downlink streams share a rendering window and one rendering manager manages rendering centrally.

**Precautions**

> - Though this version (2.7.0) is compatible with the previous version (2.5.+), behaviors of some publishing interfaces in this version have changed. Therefore, it is recommended that new interface callback methods are used. Customers that have accessed the earlier version need to read the release note first and then determine whether to perform an upgrade.

### New Features

- 1. SDK publishing mode

Add the SDK mode setting. The SDK mode can be set either to audio/video mode or audio-only mode.

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [setMediaMode](#setMediaMode) | Set media mode |

- 2. SDK room mode

Add the room mode setting. The room mode can be set to live streaming, communication, and audio room modes.

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [setRoomMode](#setRoomMode) | Set room mode |

- 3. Audio publishing mode

Add the publishing mode setting. Users can select required audio uplink mode, for example, whether accompaniment is carried.

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [setAudioSourceType](#setAudioSourceType) | Set publishing mode |

- 4. Volume adjustment

Add the support for volume collection through microphone and volume adjustment during local play of subscribed remote users

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [setPlayVolume](#setPlayVolume) | Sets the local play volume of a remote user |
| [adjustRecordingSignalVolume](#adjustRecordingSignalVolume) | Set microphone volume |

- 5. Graphic card collection

After graphic card collection is enabled, the sound played by the graphic card will be integrated to local audio stream and then sent to the remote end

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [enableLoopbackRecording](#enableLoopbackRecording) | Enable/Disable graphic card capture. |

- 6. Audio player control

Play control on local or online audio files is implemented by audio player. Effects such as accompaniment and special effects are available

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [createThunderAudioPlayer](#createThunderAudioPlayer) | Create file play object [IThunderAudioPlayer](#IThunderAudioPlayer) |
| [destroyThunderAudioPlayer](#destroyThunderAudioPlayer) | Create file destroying object [IThunderAudioPlayer](#IThunderAudioPlayer) |

- 7. Local audio recording on client

Audio files can be recorded locally on client to satisfy customers’ local recording requirements

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [startAudioRecording](#startAudioRecording) | Start audio recording |
| [stopAudioRecording](#stopAudioRecording) | Stop audio recording |

- 8. Automatic gain

Added volume automatic gain switch for convenient use

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [enableAGC](#enableAGC) | Enable/Disable Automatic Gain Control (AGC) |

- 9. Media supplementary information

Add the support of carrying media supplementary information through SEI/DSE. This allows users to determine whether system information or service customization information is carried in audio/video frames in anchor network or in video mixing and stream publishing

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [registerMediaExtraInfoObserver](#registerMediaExtraInfoObserver) | Register observer object of media extra information |
| [sendMediaExtraInfo](#sendMediaExtraInfo) | Send media extra information |
| [enableMixVideoExtraInfo](#enableMixVideoExtraInfo) | Enable video mixing with media extra information |
| [IThunderMediaExtraInfoObserver.onSendMediaExtraInfoFailedStatus](#onSendMediaExtraInfoFailedStatus) | Callback on failure in sending secondary media information |
| [IThunderMediaExtraInfoObserver.onRecvMediaExtraInfo](#onRecvMediaExtraInfo) | Receive media extra information |
| [IThunderMediaExtraInfoObserver.onRecvMixAudioInfo](#onRecvMixAudioInfo) | Extra information of mixed audio stream received |
| [IThunderMediaExtraInfoObserver.onRecvMixVideoInfo](#onRecvMixVideoInfo) | Extra information of mixed video stream received |

- 10. User-defined messages

Added support for releasing customized messages by anchor through broadcast channels so as to synchronize related information to broadcast network

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [sendUserAppMsgData](#sendUserAppMsgData) | Send custom broadcast message of service |
| [onRecvUserAppMsgData](#onRecvUserAppMsgData) | Notification of receiving service customized broadcast messages |
| [onSendAppMsgDataFailedStatus](#onSendAppMsgDataFailedStatus) | Notification of failure in sending service customized broadcast messages |

- 11. Callback on change in audio/video device status

Statistical collection and callback are performed for audio/video streams released locally through audio/video SDK and subscribed remote audio/video streams.

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [onAudioCaptureStatus](#onAudioCaptureStatus) | Notification of change in audio device capture status |
| [onVideoCaptureStatus](#onVideoCaptureStatus) | Notification of change in camera capture status |

- 12. Statistics callback for local and remote audio/video streams

Statistical collection and callback are performed for audio/video streams released locally through audio/video SDK and subscribed remote audio/video streams.

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [onLocalVideoStats](#onLocalVideoStats) | Callback on local video stream statistics |
| [onLocalAudioStats](#onLocalAudioStats) | Callback on local audio streams statistics |
| [onRemoteVideoStatsOfUid](#onRemoteVideoStatsOfUid) | Statistics callback for remote video streams |

- 13. Log Management

Provide log setting interface to facilitate users to manage logs

| Method | Function |
| ----------------------------------------------------------- | -------------------------------- |
| [setLogFilePath](#setLogFilePath) | Setting directory for SDK to output log files |
| [setLogLevel](#setLogLevel) | Setting log levels |


### Optimization and Improvement

- 1. Optimization for starting/stopping audio/video publishing

To optimize the publishing procedure and improve usability of publishing interfaces, this version has adjusted and optimized major interfaces, and unified publishing behaviors on mainstream platforms (android, iOS, and windows).

| Earlier Procedure | New Procedure |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Procedures used in earlier audio streams: **<br/>1. createEngine <br/>2. initialize<br/>3.setRoomConfig<br/>4. joinRoom<br/>5.enableAudioEngine<br/>6.disableAudioEngine<br/>7.leaveRoom | **Procedures used in new audio streams:**<br/>1. createEngine <br/>2. initialize<br/>3. setRoomMode<br/>4. joinRoom<br/>5. stopLocalAudioStream(false)<br/>6. stopLocalAudioStream(true)<br/>7. leaveRoom |
| **Procedures used in earlier video streams: **<br/>1.createEngine <br/>2.initialize<br/>3.setRoomConfig<br/>4.joinRoom<br/>5.startVideoPreview<br/>6.enableVideoEngine<br/>7.disableVideoEngine<br/>8.stopVideoPreview<br/>9.leaveRoom | **Procedures used in new video streams: **<br/>1. createEngine <br/>2. initialize<br/>3. setRoomMode<br/>4. joinRoom<br/>5. enumVideoDevices<br/>6. setVideoEncoderConfig<br/>7. startVideoDeviceCapture<br/>8. setLocalVideocanvas<br/>9. startVideoPreview<br/>10. stopLocalVideoStream(false)<br/>11. stopLocalVideoStream(true)<br/>12. stopVideoPreview<br/>13. stopVideoDeviceCapture<br/>14. leaveRoom |

### Interface Changes

- 1. Modification to volume interfaces

| Function | Old Interface | New Interface |
| -------------------------------- | ------------------------------------------- | ------------------------------------- |
| Sets the local play volume of a remote user | ThunderAudioFilePlayer.setPlayVolume | [setPlayVolume](#setPlayVolume) |
| Set the volume of the current playback device | [setOutputtingVolume](#setOutputtingVolume) | [setOuttingVolume](#setOuttingVolume) |
| Get the volume of the current playback device | [getOutputtingVolume](#getOutputtingVolume) | [getOuttingVolume](#getOuttingVolume) |

- 2. Deprecation of some interfaces

Some interfaces have been changed to be deprecated with interface behaviors remaining the same, thus usage of existing users is not affected. However, we will not recommend usage of such interfaces any more nor will we maintain them

| Method | Function |
| --- | --- |
| [setRoomConfig](#setRoomConfig) | Marked as @Deprecated with interface behaviors remaining the same |
| [enableAudioEngine](#enableAudioEngine) | Marked as @Deprecated with interface behaviors remaining the same |
| [disableAudioEngine](#disableAudioEngine) | Marked as @Deprecated with interface behaviors remaining the same |
| [enableVideoEngine](#enableVideoEngine) | Marked as @Deprecated with interface behaviors directly returned. No processing is performed internally |
| [disableVideoEngine](#disableVideoEngine) | Marked as @Deprecated with interface behaviors directly returned. No processing is performed internally |

- 3. Interface Behavior Changes

| Interface | Change |
| --- | --- |
| [setRemoteVideoCanvas](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.7.0#setRemoteVideoCanvas) | Set rendering view of remote video: thunderbolt-sdk automatically subscribes audio/video streams in the channel. After uid and view of a remote anchor are configured, sdk will save the binding relationship between uid and view and render the view. If the app destroys the view, this interface must be called to set the uid and view=null to unbind the view internally. Otherwise, the sdk is directed to the wild pointer of the view during automatic subscription when the remote anchor re-publishes, resulting in crash. |
| [startVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.7.0#startVideoPreview) / [stopVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.7.0#stopVideoPreview) | Unbinding of video capture and preview from room: Video preview ([startVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.7.0#startVideoPreview)) starts upon room entry and does not stop proactively upon room exit. To stop preview, call the [stopVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.7.0#stopVideoPreview) interface. |

### Problem Fixing

N/A

### Others

- 1. Error codes are returned in a unified manner.
- 2. All interfaces are standardized with life cycle, calling, and reset time specified. (The return values must be processed).

## v2.5.4

This version is released on February 10, 2020.

Repair the known online issues and crash.


## v2.5.2

This version is released on November 12, 2019.

Repair the bugs found during online operation.


## v2.5.1

This version is released on October 31, 2019.

### New Interfaces

| Method | Function |
| ------------------------------------------------------------ | -------------- |
| [enableMicEnhancement](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.5.1#enableMicEnhancement) | Start microphone enhancement |
| [enableMicDenoise](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.5.1#enableMicDenoise) | Start microphone noise reduction |
| [enableAEC](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.5.1#enableAEC) | Start echo mitigation |

### Modified Interfaces

| Method | Modification |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [setLocalCanvasScaleMode](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.5.1#setLocalCanvasScaleMode) | Implementation of YR_RENDER_MODE_FILL in the previous version is inconsistent with description, which has been rectified. Implementation of YR_RENDER_MODE_FILL and YR_RENDER_MODE_CLIP_TO_BOUNDS in the previous version have been unified as clipping. |
| [setRemoteCanvasScaleMode](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.5.1#setRemoteCanvasScaleMode) | Implementation of YR_RENDER_MODE_FILL in the previous version is inconsistent with description, which has been rectified. Implementation of YR_RENDER_MODE_FILL and YR_RENDER_MODE_CLIP_TO_BOUNDS in the previous version have been unified as clipping. |

## v2.4.0

This version is released on October 15, 2019.

- 1. Optimize the screen sharing function. Screen capturing by area in a window, resolution adaption during screen capturing, and suspending or recovering screen capturing are supported
- 2. Add and improve interfaces for collecting and rendering video streams, which are connected to special effect libraries such as beautification library.

## Earlier Versions

### v2.3.0
#### New Interfaces
- 1. Add the screen sharing function. Currently, full screen sharing, regional sharing (screen), window sharing, and sound sharing are supported.
- 2. Add H265-based microphone connection, which provides an encoding/decoding protocol for video microphone connection that outperforms the H.264 protocol.
- 3. Change UID type to String. For example, the API joinRoom() allows app to specify account ID to join the channel. Callback interfaces with UIDs, including onJoinRoomSuccess and onUserJoined, use string-type UIDs.

#### Modified Interfaces

| Before Modification | After Modification | Function |
| -------------- | ------------------------------------------------------------ | -------------------- |
| onJoinedOfUid | [onUserJoined](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.3.0#onUserJoined) | Callback on user joining a current room |
| onOfflineOfUid | [onUserOffline](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.3.0#onUserOffline) | Callback on user leaving a current room |
- 5. Management method for changing two video devices:<br>

Before Change

| Method | Function |
| --------- | ---------------- |
| setDevice | Set video device |
| getDevice | Get current video device |

After Change

| Method | Function |
| ------------------------------------------------------------ | ---------------- |
| [startVideoDeviceCapture](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.3.0#startVideoDeviceCapture) | Start video device |
| [stopVideoDeviceCapture](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Windows&version=2.3.0#stopVideoDeviceCapture) | Stop current video device |

### v2.2.1
- 1. Add interfaces that accommodate with and interconnect with Web SDK.
- 2. Add camera preview and mirror setting for stream publishing
- 3. Add multiple SDK event callback interfaces to satisfy various service requirements
- 4. Further optimize SDK performance items.

### v2.1.2
- 1. Modify the names of some SDK interfaces

### v2.1.1
- 1. Modify audio/video subscription logic. Added blacklist and whitelist mechanism so that audio/video streams can be shielded or subscribed as required. [Click to know more](/en/cloud/v2/developer/doc.htm?serviceId=108&typeCode=API_DOC&title=媒体黑白名单功能&version=).


### v2.1.0:
- 1. Add the cross-channel subscription function. Audio/video streams of other channels can be subscribed to implement cross-channel microphone connection.
- 2. Add the interface for automatic audio capture
- 3. Add the interface for automatic video capture
- 4. Add interface for mixing streams and CDN stream publishing to implement video mixing and stream publishing to CDN at server.
- 5. Add the watermark function for local video. A PNG picture can be added to local video as watermark and the watermarked video can be released through SUNCLOUADS interaction network.
### V2.0.1
Add watermarks by local SDK importing