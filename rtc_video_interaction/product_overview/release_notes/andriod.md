# Release Note Log

This section provides release update description to the audio/video SDK product.

## Overview

Version of the latest audio/video SDK product running on Android is v2.7.0.

Two service product types are available. For their key features and charging rules, click the following links:

- [Real-time audio interaction](/en/product_category/rtc_service/rt_audio_interaction/product_overview/product/product.md)
- [Real-time video interaction](/en/product_category/rtc_service/rt_video_interaction/product_overview/product/product.md)

We offer complete user access documents for your quick access to audio/video capabilities. To know detailed integration methods, interface descriptions, and related scenario demos, click the following links:

- SDK integration to App: [SDK Integration Methods](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=DEPLOYMENT&title=Android&version=blank&parentId=761)

- API Development Manual:  [Android API](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android)

- Downloading related demos: [SDK and Demo downloading](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=SDK_DOWNLOAD)

## v2.7.0

### Version Overview

This version is released on March 19, 2020.

In this version, usability of publishing interfaces are improved to optimize the publishing procedure. Major interfaces for audio/video publishing have been adjusted and optimized, and publishing behaviors on mainstream platforms (android, iOS, and windows) are unified. 
In addition, to facilitate monitoring on the running status of audio/video services, callback information related to audio/video streams and equipment is added, allowing more transparent and detailed information to be transmitted to services. 
The issue of SDK power consumption in case of multiple people connected on microphone on mobile clients has been improved. Multi-person microphone connection view has been added. Specifically, downlink streams share a rendering window and one rendering manager manages rendering centrally.

**Precautions**

> - Though this version (2.7.0) is compatible with the previous version (2.5.+), behaviors of some publishing interfaces in this version have changed. Therefore, it is recommended that new interface callback methods are used.

### New Features

- 1. Multi-person microphone connection view

In case of multiple people connected on microphone, downlink streams share a rendering window and one rendering manager manages rendering centrally.

| Interface | Function |
| --- | --- |
| [setRemotePlayType](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setRemotePlayType) | Set whether to enable multi-person microphone connection view to enter multi-person mode. This interface is called before channel entry |
| [setMultiVideoViewLayout](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setMultiVideoViewLayout) | Set layout parameters in the scenario of multiple people connected on microphone |

- 2. Callback on change in audio/video device status

Real-time callback is provided for status such as no permission or being occupied when audio/video SDK calls audio/video capture device. This facilitates service adjustment in time.

| Interface | Function |
| --- | --- |
| [onAudioCaptureStatus](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onAudioCaptureStatus) | Audio device capture status notification |
| [onVideoCaptureStatus](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onVideoCaptureStatus) | Notification of change in camera capture status |

- 3. Statistics callback for local and remote audio/video streams

Statistical collection and callback are performed for audio/video streams released locally through audio/video SDK and subscribed remote audio/video streams.

| Interface | Function |
| --- | --- |
| [onLocalVideoStats](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onLocalVideoStats) | Callback on local video stream statistics |
| [onLocalAudioStats](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onLocalAudioStats) | Callback on local audio streams statistics |
| [onRemoteVideoStatsOfUid](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onRemoteVideoStatsOfUid) | Callback on remote video stream information during the call |
| [onRemoteAudioStatsOfUid](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#onRemoteAudioStatsOfUid) | Callback on remote audio stream information during the call |

### Optimization and Improvement

- 1. Optimization for starting/stopping audio/video publishing

To optimize the publishing procedure and improve usability of publishing interfaces, this version has adjusted and optimized major interfaces, and unified publishing behaviors on mainstream platforms (android, iOS, and windows).

| Earlier Procedure | New Procedure |
| --- | --- |
| **Procedures used in earlier audio streams: **<br/>1. createEngine<br/>2. setMediaMode<br/>3. joinRoom<br/>4. enableAudioEngine<br/>5. disableAudioEngine<br/>6. leaveRoom | **Procedures used in new audio streams: **<br/>1. createEngine<br/>2. setMediaMode<br/>3. joinRoom<br/>4. stopLocalAudioStream(false)<br/>5. stopLocalAudioStream(true)<br/>6. leaveRoom |
| **Procedures used in earlier video streams: **<br/>1. createEngine<br/>2. setMediaMode<br/>3. joinRoom<br/>4. startVideoPreview<br/>5. enableVideoEngine<br/>6. disableVideoEngine<br/>7. stopVideoPreview<br/>8. leaveRoom | **Procedures used in new video streams: **<br/>1. createEngine<br/>2. setMediaMode<br/>3. joinRoom<br/>4. setVideoEncoderConfig<br/>5. setLocalVideocanvas<br/>6. startVideoPreview<br/>7. stopLocalVideoStream(false)<br/>8. stopLocalVideoStream(true)<br/>9. stopVideoPreview<br/>10. leaveRoom |


### Interface Changes

- Volume range adjustment

To satisfy developers’ requirements in different scenarios, adjustable volume range is further detailed and expanded. Specifically, the volume range has expanded from 0-100 to 0-400. Since excessively high volume may degrade the collection or play quality for different equipment, users shall adjust the range as required. The following interfaces are involved:

| Interface | New version |
| --- | --- |
| [setLoudSpeakerVolume](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setLoudSpeakerVolume) | Set loudspeaker volume. Available volume range: 0-400 |
| [setMicVolume](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setMicVolume) | Set microphone volume. Available volume range: 0-400 |
| [setRemoteAudioStreamsVolume](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setRemoteAudioStreamsVolume) | Set play volume for remote users. Available volume range: 0-400 |

- 2. Parameter simplification for the texture data collection interface

To optimize user experience of developers, parameters of the texture data monitoring and collection interface (registerVideoCaptureTextureObserver) have been adjusted and optimized

| Earlier version | New version |
| --- | --- |
| public interface IGPUProcess {<br/> void onInit(MobileFaceDetectionWrapperManager manager, int textureTarget, int outputWidth, int outputHeight, String fs);<br/> ...<br/>  void onDraw(final int textureId, final FloatBuffer cubeBuffer,final FloatBuffer textureBuffer, int textureTarget, float[] texMatrix,boolean background);<br/> ...} | public interface IGPUProcess {<br/> void onInit(int textureTarget, int outputWidth, int outputHeight);<br/>	...<br/>   void onDraw(final int textureId, final FloatBuffer cubeBuffer,final FloatBuffer textureBuffer, float[] texMatrix);<br/>	...<br/>} |

- 3. Deprecation of some interfaces

Some interfaces have been changed to be deprecated with interface behaviors remaining the same, thus usage of existing users is not affected. However, we will not recommend usage of such interfaces any more nor will we maintain them

| Interface | Change |
| --- | --- |
| [enableAudioEngine](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#enableAudioEngine) | Marked as @Deprecated with interface behaviors remaining the same |
| [disableAudioEngine](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#disableAudioEngine) | Marked as @Deprecated with interface behaviors remaining the same |
| [enableVideoEngine](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#enableVideoEngine) | Marked as @Deprecated with interface behaviors directly returned. No processing is performed internally |
| [disableVideoEngine](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#disableVideoEngine) | Marked as @Deprecated with interface behaviors directly returned. No processing is performed internally |

- 4. Interface Behavior Changes

| Interface | Change |
| --- | --- |
| [setRemoteVideoCanvas](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=iOS&version=2.7.0#setRemoteVideoCanvas) | Set rendering view of remote video: thunderbolt-sdk automatically subscribes audio/video streams in the channel. After uid and view of a remote anchor are configured, sdk will save the binding relationship between uid and view and render the view. If the app destroys the view, this interface must be called to set the uid and view=null to unbind the view internally. Otherwise, the sdk is directed to the wild pointer of the view during automatic subscription when the remote anchor re-publishes, resulting in crash. |
| [startVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#startVideoPreview) / [stopVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#stopVideoPreview) | Unbinding of video capture and preview from room: Video preview ([startVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#startVideoPreview)) starts upon room entry and does not stop proactively upon room exit. To stop preview, call the [stopVideoPreview](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#stopVideoPreview) interface. |

- 5. Modification to other interfaces

| Interface | Change |
| --- | --- |
| [setReverbExParameter](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setReverbExParameter) [setCompressorParam](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.7.0#setCompressorParam) [setLimiterParam](#setLimiterParam) | Definitions of transfer parameters of three interfaces have migrated from ThunderEngine to ThunderRtcConstant |

### Problem Fixing

N/A

### Others

- 1. Error codes are returned in a unified manner.
- 2. All interfaces are standardized with life cycle, callback, and reset time specified. Therefore, the return values must be processed.
- 3. ThunderEventHandler.java class has changed from interface modification to abstract modification.

## v2.5.3

This version is released on February 26, 2020.

Bugs found during online usage have been resolved.

## v2.5.2

This version is released on December 10, 2019.

This version contains modified and deprecated interfaces. In case of upgrade from SDK of earlier versions, interface change descriptions must be read carefully. <br>
==Special attention: Modification made in [v2.4.16](#v2.4.16) and [v2.4.20](#v2.4.20) are not included in this version and will be included in version 2.6. ==

- [v2.4.13](#v2.4.16): Contains high/low stream view features and some new callback interface
- [v2.4.20](#v2.4.20): Contains optimization on multi-person microphone connection mode and support for customized layout of multi-person microphone connection


**This version includes following changes:**
- The room configuration interface [setRoomConfig](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setRoomConfig) is deprecated (compatible with the earlier version) and is replaced with the SDK media mode configuration interface [setMediaMode](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setMediaMode) and room scenario mode configuration interface setRoomMode.](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setRoomMode)[
- Chorus accompanied by audio is supported.
- FEC package compatibility is optimized.
- Extra information [SEI] (publishing start-up, view, and video mixing) of audio/video media is supported.
- Audio file play has changed to asynchronous control.
- Add support for some new models of PC simulators: Leidian, MUMU, and Yeshen<br>

### Modified Interfaces
* Deprecated interfaces are as follows:<br>

| Method | Function |
| ------------------------------------------------------------ | ------------ |
| [setRoomConfig](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setRoomConfig) | Set room mode |
* Modified interfaces are as follows:

| Method | Function | Modification Description |
| ------------------------------------------------------------ | -------------------------- | ------------------------------------------------------------ |
| [setMediaExtraInfoCallback](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setMediaExtraInfoCallback) | Set callback and monitoring of media extra information | Modify IThunderMediaExtraInfoCallback interface class and adds callback of the onRecvMixAudioInfo and onRecvMixVideoInfo interface |
| [sendMediaExtraInfo](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#sendMediaExtraInfo) | Send media extra information | Support sending of media extra information upon publishing in audio/video mode |
| [ThunderAudioFilePlayer.open](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#ThunderAudioFilePlayer.open) | Open audio file | The return value type of ThunderAudioFilePlayer.open has changed from BOOL to void. The new return value is recommended for use in callback IThunderAudioFilePlayerCallback.onAudioFilePlayError<br/>. Whether a file is successfully opened can be determined by the return value.<br/><br/><br/> |
| [addPublishOriginStreamUrl](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#addPublishOriginStreamUrl) | Add address for bypass stream publishing of source streams | In the earlier version, multiple URLs may overwrite, which does not apply to the new version. If URLs are to be updated, call removePublishOriginStreamUrl to remove original URLs and then add target ones |
| [addPublishTranscodingStreamUrl](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#addPublishTranscodingStreamUrl) | Add address for bypass stream publishing of mixed streams | In the earlier version, multiple URLs may overwrite, which does not apply to the new version. If URLs are to be updated, call removePublishTranscodingStreamUrl to remove original URLs and then add target ones |

### New Interfaces

| Method | Function |
| ------------------------------------------------------------ | ---------------------------- |
| [setMediaMode](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setMediaMode) | Set SDK media mode |
| [setRoomMode](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setRoomMode) | Set room scenario mode |
| [IThunderMediaExtraInfoCallback.onRecvMixAudioInfo](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setMediaExtraInfoCallback) | Extra information of mixed audio stream received |
| [IThunderMediaExtraInfoCallback.onRecvMixVideoInfo](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setMediaExtraInfoCallback) | Extra information of mixed video stream received |
| [IThunderAudioFilePlayerCallback.onAudioFilePlaying](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#IThunderAudioFilePlayerCallback.onAudioFilePlaying) | Callback interface for ongoing playing |
| [IThunderAudioFilePlayerCallback.onAudioFilePause](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#IThunderAudioFilePlayerCallback.onAudioFilePause) | Callback interface for paused playing |
| [IThunderAudioFilePlayerCallback.onAudioFileResume](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#IThunderAudioFilePlayerCallback.onAudioFileResume) | Callback interface for recovering playing |
| [IThunderAudioFilePlayerCallback.onAudioFileStop](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#IThunderAudioFilePlayerCallback.onAudioFileStop) | Callback interface for user-triggered playing suspending |
| [IThunderAudioFilePlayerCallback.onAudioFileSeekComplete](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#IThunderAudioFilePlayerCallback.onAudioFileSeekComplete) | Callback interface for fast forward to specified time |
| [ThunderAudioFilePlayer.setMixStandard](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#ThunderAudioFilePlayer.setMixStandard) | Set whether audio file is a mixed video standard stream |
| [ThunderAudioFilePlayer.isMixStandard](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#ThunderAudioFilePlayer.isMixStandard) | Query whether audio file is a mixed video standard stream |
| [LiveTranscoding.setAudioOnlyStandardSreamUrl](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setLiveTranscodingTask) | Set whether external audio URL is mixed video standard stream |
| [LiveTranscoding.enableMixVideoExtraInfo](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.5.1#setLiveTranscodingTask) | Enable video mixing with media extra information |


## v2.4.20

This version is released on December 6, 2019.

**Precautions**
> - Modification made in [v2.4.13](#v2.4.13) is not included in this version and related interfaces will be included in version 2.6. ==

- [v2.4.16](#v2.4.16): Contains high/low stream view features and some new callback interface

### New Interfaces

| Method | Function |
| --------------------------------------------------- | ------------------------------------------------------------ |
| [setRemotePlayType](setRemotePlayType) | Set whether to enable multi-person microphone connection view to enter multi-person mode. This interface is called before channel entry |
| [setMultiVideoViewLayout](#setMultiVideoViewLayout) | Set layout parameters in the scenario of multiple people connected on microphone |


## v2.4.16

This version is released on December 6, 2019.

This version features high/low streams, which provides smooth view switching experience in Web SDK 2.1.2.

### New Interfaces

| Method | Function |
| ------------------------------------------------------------ | ---------------------------- |
| [changeRemoteVideoStreamType](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#changeRemoteVideoStreamType) | Set the size of remote high/low streams |
| [setDefaultRemoteVideoStreamType](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#setDefaultRemoteVideoStreamType) | Set the type of video streams subscribed by default |
| [onWarning](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#onWarning) | Alarm callback during SDK operation |
| [onRemoteVideoStatsOfUid](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#onRemoteVideoStatsOfUid) | Callback on remote video stream information during the call |
| [onRemoteAudioTransStatsOfUid](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#onRemoteAudioTransStatsOfUid) | Transmission information callback for remote audio streams during the call |
| [onRemoteVideoTransStatsOfUid](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#onRemoteVideoTransStatsOfUid) | Transmission information callback for remote video streams during the call |

### Modified Interfaces

| Method | Function | Modification Description |
| ------------------------------------------------------------ | ----------------- | ---------------------- |
| [enableWebSdkCompatibility](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#enableWebSdkCompatibility) | Enable compatibility with Web SDK | Soft parse is used globally after compatibility enablement |
| [onLeaveRoom](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.13#onLeaveRoom) | Callback upon leaving a room | Statistical fields are added |


## v2.4.1

This version is released on October 31, 2019.

- 1. Optimize the issues related to sound collection and accompaniment synchronization on Android models

- 2. Resolve the bugs found during online operation

## v2.4.0

This version is released on October 15, 2019.

- 1. SDK package name has been changed. Obtain the new configuration by referring to SDK Integration Methods.[](/en/cloud/v2/developer/doc.htm?serviceId=102&typeCode=DEPLOYMENT&title=Android&version=blank&parentId=761)

- 2. Media extra information can be carried in audio-only mode. In such scenarios, service data is carried in audio streams to the receive end during services

| Method | Function |
| ------------------------------------------------------- | -------------------------- |
| [setMediaExtraInfoDelegate](#setMediaExtraInfoDelegate) | Set callback and monitoring of media extra information |
| [sendMediaExtraInfo](#sendMediaExtraInfo) | Send media extra information |

- 3. More complete accompaniment play interfaces are provided. Callback information for different statuses is enriched.

| Method | Function |
| ------------------------------------------------------------ | -------------------------------- |
| [ThunderAudioFilePlayer.setPlayerLocalVolume](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.setPlayerLocalVolume) | Adjust volume size when music files are played on local end. |
| [ThunderAudioFilePlayer.setPlayerPublishVolume](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.setPlayerPublishVolume) | Adjust remote volume of music files |
| [ThunderAudioFilePlayer.getPlayerLocalVolume](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.getPlayerLocalVolume) | Get the local volume of music files |
| [ThunderAudioFilePlayer.getPlayerPublishVolume](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.getPlayerPublishVolume) | Get the remote volume of music files |
| [ThunderAudioFilePlayer.setLooping](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.setLooping) | Set times of loop playbacks. |
| [ThunderAudioFilePlayer.selectAudioTrack](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.selectAudioTrack) | Switch to specified sound track. |
| [ThunderAudioFilePlayer.getAudioTrackCount](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#ThunderAudioFilePlayer.getAudioTrackCount) | Obtain the number of sound tracks with opened files. |
| [IThunderAudioFilePlayerCallback.onAudioFilePlayError](cloud/v2/developer/doc.htm?serviceId=102&typeCode=API_DOC&title=Android&version=2.4.0#IThunderAudioFilePlayerCallback.onAudioFilePlayError) | Callback interface of playing status |

## Earlier Versions

### v2.3.20
- 1. Repair the bugs found during online operation.

### v2.3.1
- 1. Add H265-based microphone connection, which provides an encoding/decoding protocol for video microphone connection that outperforms the H.264 protocol.
- 2. Add voice-based location recognition. Voice location and volume can be configured for remote users.
- 3. Change UID type to String. For example, the API joinRoom() allows app to specify account ID to join the channel. Callback interfaces with UIDs, including onJoinRoomSuccess and onUserJoined, use string-type UIDs.

### v2.2.11
- 1. Resolve the issue that multimedia volume turns up after microphone is disabled.
- 2. Resolve screen recording and view bugs.
- 3. Add parameter type QUALITY_DOWN to the callback interface of NetWorkQuality.


### v2.2.4
- 1. Add functional interfaces for screen recording.
- 2. Add interfaces that accommodate with and interconnect with Web SDK.
- 3. Add interface for setting voice format and improved audio recording and playing interfaces.
- 4. Add camera control functions: portrait and land/scape orientation, and mirroring.
- 5. Add multiple SDK event callback interfaces to satisfy various service requirements
- 6. Add the voice change function with 13 special voice effects provided, including girly, mature-man, heavy metal, and Luban effects.
- 7. Add voice effects in multiple scenarios. Currently, a total of 9 scenarios are provided, including hiphop, rock, and concert scenarios.
- 8. Add and improve interfaces for monitoring YUV source streams, which are connected to special effect libraries such as beautification library.
- 9. Further optimize SDK performance items.


### v2.1.5
- 1. Change the SDK integration mode to online warehouse import. For details, see “[Integration Documents](https://www.sunclouds.com/cloud/v2/developer/doc.htm?serviceId=102&typeCode=DEPLOYMENT&title=SDK集成方法&version=2.0.0)”.
- 2. Names of some SDK interfaces
- 3. Update the integration mode of surfaceView.

### v2.1.2:
- 1. Add the cross-channel subscription function. Audio/video streams of other channels can be subscribed to implement cross-channel microphone connection.
- 2. Add the interface for automatic audio capture.
- 3. Add interface for mixing streams and CDN stream publishing to implement video mixing and stream publishing to CDN at server.
- 4. Add the watermark function for local video. A PNG picture can be added to local video as watermark and the watermarked video can be released through SUNCLOUADS interaction network.
- 5. Add interfaces for customized video modules. Users can configure customized video sources other than default cameras.