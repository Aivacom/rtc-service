# Event callback

## Interface List

- ### ThunderEventHandler

| Public callback function | Function Name |
| ---:| :--- |
| void | [onError](#ThunderEventHandler.onError)(int error) |
| void | [onJoinRoomSuccess](#ThunderEventHandler.onJoinRoomSuccess)(String room, String uid, int elapsed) |
| void | [onLeaveRoom](#ThunderEventHandler.onLeaveRoom)([ThunderEventHandler.RoomStats](#ThunderEventHandler.RoomStats) status) |
| void | [onBizAuthResult](#ThunderEventHandler.onBizAuthResult)(boolean bPublish, int result) |
| void | [onSdkAuthResult](#ThunderEventHandler.onSdkAuthResult)(int result) |
| void | [onUserBanned](#ThunderEventHandler.onUserBanned)(boolean status) |
| void | [onUserJoined](#ThunderEventHandler.onUserJoined)(String uid, int elapsed) |
| void | [onUserOffline](#ThunderEventHandler.onUserOffline)(String uid, int reason) |
| void | [onTokenWillExpire](#ThunderEventHandler.onTokenWillExpire)(byte[] token) |
| void | [onTokenRequested](#ThunderEventHandler.onTokenRequested)() |
| void | [onNetworkQuality](#ThunderEventHandler.onNetworkQuality)(String uid, int txQuality, int rxQuality) |
| void | [onRoomStats](#ThunderEventHandler.onRoomStats)([ThunderNotification.RoomStats](#ThunderNotification.RoomStats) stats) |
| void | [onPlayVolumeIndication](#ThunderEventHandler.onPlayVolumeIndication)([ThunderEventHandler.AudioVolumeInfo](#ThunderEventHandler.AudioVolumeInfo)[] speakers, int totalVolume) |
| void | [onCaptureVolumeIndication](#ThunderEventHandler.onCaptureVolumeIndication)(int totalVolume, int cpt, int micVolume) |
| void | [onConnectionLost](#ThunderEventHandler.onConnectionLost)() |
| void | [onAudioPlayData](#ThunderEventHandler.onAudioPlayData)(byte[] data, long cpt, long pts, String uid, long duration) |
| void | [onAudioPlaySpectrumData](#ThunderEventHandler.onAudioPlaySpectrumData)(byte[] data) |
| void | [onRecvUserAppMsgData](#ThunderEventHandler.onRecvUserAppMsgData)(byte[] data, String uid) |
| void | [onSendAppMsgDataFailedStatus](#ThunderEventHandler.onSendAppMsgDataFailedStatus)(int status) |
| void | [onRemoteAudioStopped](#ThunderEventHandler.onRemoteAudioStopped)(String uid, boolean stop) |
| void | [onRemoteVideoStopped](#ThunderEventHandler.onRemoteVideoStopped)(String uid, boolean stop) |
| void | [onRemoteVideoPlay](#ThunderEventHandler.onRemoteVideoPlay)(String uid, int width, int height, int elapsed) |
| void | [onVideoSizeChanged](#ThunderEventHandler.onVideoSizeChanged)(String uid, int width, int height, int rotation) |
| void | [onFirstLocalAudioFrameSent](#ThunderEventHandler.onFirstLocalAudioFrameSent)(int elapsed) |
| void | [onFirstLocalVideoFrameSent](#ThunderEventHandler.onFirstLocalVideoFrameSent)(int elapsed) |
| void | [onPublishStreamToCDNStatus](#ThunderEventHandler.onPublishStreamToCDNStatus)(String url, int errorCode) |
| void | [onNetworkTypeChanged](#ThunderEventHandler.onNetworkTypeChanged)(int type) |
| void | [onConnectionStatus](#ThunderEventHandler.onConnectionStatus)(int status) |
| void | [onAudioCaptureStatus](#ThunderEventHandler.onAudioCaptureStatus)(int status) |
| void | [onVideoCaptureStatus](#ThunderEventHandler.onVideoCaptureStatus)(int status) |
| void | [onLocalVideoStats](#ThunderEventHandler.onLocalVideoStats)([ThunderEventHandler.LocalVideoStats](#ThunderEventHandler.LocalVideoStats) stats) |
| void | [onLocalAudioStats](#ThunderEventHandler.onLocalAudioStats)([ThunderEventHandler.LocalAudioStats](#ThunderEventHandler.LocalAudioStats) stats) |
| void | [onRemoteVideoStatsOfUid](#ThunderEventHandler.onRemoteVideoStatsOfUid)(String uid, [ThunderEventHandler.RemoteVideoStats](#ThunderEventHandler.RemoteVideoStats) stats) |
| void | [onRemoteAudioStatsOfUid](#ThunderEventHandler.onRemoteAudioStatsOfUid)(String uid, [ThunderEventHandler.RemoteAudioStats](#ThunderEventHandler.RemoteAudioStats) stats) |

- ### IAudioFrameObserver

| Public callback function | Function Name |
| ---:| :--- |
| boolean | [onRecordAudioFrame](#IAudioFrameObserver.onRecordAudioFrame)(ByteBuffer samples, int numOfSamples, int bytesPerSample, int channels, int samplesPerSec) |
| boolean | [onPlaybackAudioFrame](#IAudioFrameObserver.onPlaybackAudioFrame)(ByteBuffer samples, int numOfSamples, int bytesPerSample, int channels, int samplesPerSec) |
| boolean | [onPlaybackAudioFrameBeforeMixing](#IAudioFrameObserver.onPlaybackAudioFrameBeforeMixing)(String uid, ByteBuffer samples, int numOfSamples, int bytesPerSample, int channels, int samplesPerSec) |

- ### IGPUProcess

| Public callback function | Function Name |
| ---:| :--- |
| void | [onInit](#IGPUProcess.onInit)(int textureTarget, int outputWidth, int outputHeight) |
| void | [onDestroy](#IGPUProcess.onDestroy)() |
| void | [onDraw](#IGPUProcess.onDraw)(final int textureId, final FloatBuffer cubeBuffer,final FloatBuffer textureBuffer, float[] texMatrix) |
| void | [onOutputSizeChanged](#IGPUProcess.onOutputSizeChanged)(final int width, final int height) |

- ### IVideoCaptureObserver

| Public callback function | Function Name |
| ---:| :--- |
| void | [onCaptureVideoFrame](#IVideoCaptureObserver.onCaptureVideoFrame)(int width, int height, byte[] data, int length, int imageFormat) |

- ### IVideoDecodeObserver

| Public callback function | Function Name |
| ---:| :--- |
| void | [onVideoDecodeFrame](#IVideoDecodeObserver.onVideoDecodeFrame)(String uid, int w, int h, byte[] data, int dateLen, long renderTimeMs) |

- ### ThunderCustomVideoSource

| Public callback function | Function Name |
| ---:| :--- |
| boolean | [onInitialize](#ThunderCustomVideoSource.onInitialize)([ThunderVideoFrameConsumer](#ThunderVideoFrameConsumer) consumer) |
| boolean | [onStart](#ThunderCustomVideoSource.onStart()) |
| boolean | [onStop](#ThunderCustomVideoSource.onStop()) |
| boolean | [onDispose](#ThunderCustomVideoSource.onDispose()) |

- ### ThunderVideoFrameConsumer

| Public callback function | Function Name |
| ---:| :--- |
| void | [consumeByteArrayFrame](#ThunderVideoFrameConsumer.consumeByteArrayFrame)(byte[] data, int format, int width, int height, int rotation, long timestamp) |

- ### IThunderLogCallback

| Public callback function | Function Name |
| ---:| :--- |
| void | [onThunderLogWithLevel](#IThunderLogCallback.onThunderLogWithLevel)(int level, String tag, String msg) |

- ### IThunderMediaExtraInfoCallback

| Public callback function | Function Name |
| ---:| :--- |
| void | [onSendMediaExtraInfoFailedStatus](#IThunderMediaExtraInfoCallback.onSendMediaExtraInfoFailedStatus)(int status) |
| void | [onRecvMediaExtraInfo](#IThunderMediaExtraInfoCallback.onRecvMediaExtraInfo)(int status) |
| void | [onRecvMixAudioInfo](#IThunderMediaExtraInfoCallback.onRecvMixAudioInfo)(int status) |
| void | [onRecvMixVideoInfo](#IThunderMediaExtraInfoCallback.onRecvMixVideoInfo)(int status) |

- ### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback

| Public callback function | Function Name |
| ---:| :--- |
| void | [onAudioFilePlayError](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayError)(int errorCode) |
| void | [onAudioFileVolume](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileVolume)(long volume, long currentMs, long totalMs) |
| void | [onAudioFileSeekComplete](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileSeekComplete)(int millisecond) |
| void | [onAudioFilePlaying](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlaying)() |
| void | [onAudioFilePause](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePause)() |
| void | [onAudioFileResume](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileResume)() |
| void | [onAudioFileStop](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileStop)() |
| void | [onAudioFilePlayEnd](#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayEnd)() |

## Detailed callback description

### ThunderEventHandler

#### ThunderEventHandler.onError

```java
public void onError(int error)
```

Report the SDK error message.

##### Parameter[](#onError)

| Parameter | Description |
| :--- | :--- |
| error | Error message code |

--------------------------

#### ThunderEventHandler.onJoinRoomSuccess

```java
public void onJoinRoomSuccess(String room, String uid, int elapsed)
```

Report the user of uid joining room successfully.

After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), receiving such a notification indicates that connection with server is normal, and the interface that can only be called after joining room successfully may be called.

##### Parameter[](#onJoinRoomSuccess)

| Parameter | Description |
| :--- | :--- |
| room | Room No. |
| uid | User ID |
| elapsed | Indicates time spent on joining room, that is, time elapsed (in millisecond) from calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) to calling back this function |

--------------------------

#### ThunderEventHandler.onLeaveRoom

```java
public void onLeaveRoom(ThunderEventHandler.RoomStats status)
```

Report has left the room.

After calling [ThunderEngine.leaveRoom](function.md#ThunderEngine.leaveRoom), this callback will be received when leaving room normally.

##### Parameter[](#onLeaveRoom)

| Parameter | Description |
| :--- | :--- |
| RoomStats | Reserved parameters, not yet realized. For details, refer to [ThunderEventHandler.RoomStats](#ThunderEventHandler.RoomStats) |

--------------------------

#### ThunderEventHandler.onBizAuthResult

```java
public void onBizAuthResult(boolean bPublish, int result)
```

Report business authentication results.

Results of service authentication. AIVACOM forwards authentication requests to business authentication server, and returns authentication results to developer through this interface.

##### Parameter[](#onBizAuthResult)

| Parameter | Description |
| :--- | :--- |
| bPublish | true: publishing authentication <br>false: playing authentication |
| result | Authentication results <br>0: pass<br> Other values: fail. Subject to developer customization. SDK simply passes-through |

--------------------------

#### ThunderEventHandler.onSdkAuthResult

```java
public void onSdkAuthResult(int result)
```

Report SDK authentication results.

Results of SDK authentication. After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), once uplink/downlink media data is available, the authentication results of SDK will be reported.

##### Parameter[](#onSdkAuthResult)

| Parameter | Description |
| :--- | :--- |
| result | Authentication results. For detailed meaning of the values, refer to [ThunderRtcConstant.AuthResult](function.md#ThunderRtcConstant.AuthResult) |

--------------------------

#### ThunderEventHandler.onUserBanned

```java
public void onUserBanned(boolean status)
```

Notification of user banned.

This callback notification will be received when user banning status changes

##### Parameter[](#onUserBanned)

| Parameter | Description |
| :--- | :--- |
| status | Banning status:<br> true: banned<br> false: unbanned |

--------------------------

#### ThunderEventHandler.onUserJoined

```java
public void onUserJoined(String uid, int elapsed)
```

Notification of user joining current room (valid for audio-only mode only).

This callback will be triggered in the following circumstances

- Remote user/anchor calls the [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) method to join room
- Remote user/anchor rejoins room after a network failure

##### Parameter[](#onUserJoined)

| Parameter | Description |
| :--- | :--- |
| uid | ID of remote user/anchor who joined room recently |
| elapsed | Delay (in millisecond) from local user calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) to triggering callback |

--------------------------

#### ThunderEventHandler.onUserOffline

```java
public void onUserOffline(String uid, int reason)
```

Notification for user leaving current room (valid for audio-only mode only).

It prompts that a remote user/anchor has left the room (or is offline). There are two reasons that user leaves a room, regular leave or timeout.

##### Parameter[](#onUserOffline)

| Parameter | Description |
| :--- | :--- |
| uid | ID of user who left room |
| reason | The offline reason, refer to [ThunderRtcConstant.UserOfflineReason](function.md#ThunderRtcConstant.UserOfflineReason) for detail |

--------------------------

#### ThunderEventHandler.onTokenWillExpire

```java
public void onTokenWillExpire(byte[] token)
```

Report token is about to expire.

- Token needs to be specified when calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom). Token has a certain valid period. If token is about to expire during the call, SDK will trigger this callback 30 seconds in advance, reminding App to update token.
- Upon receiving this callback, user needs to generate a new token at server, and call [ThunderEngine.updateToken](function.md#ThunderEngine.updateToken) to send newly generated token to SDK.

##### Parameter[](#onTokenWillExpire)

| Parameter | Description |
| :--- | :--- |
| token | Expiring token |

--------------------------

#### ThunderEventHandler.onTokenRequested

```java
public void onTokenRequested()
```

Report token has expired.

- Token needs to be specified when calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom). Token has a certain valid period. If token expires during the call, this callback notification will be received.
- Upon receiving this callback, user needs to generate a new token at server, and call [ThunderEngine.updateToken](function.md#ThunderEngine.updateToken) to send newly generated token to SDK.

--------------------------

#### ThunderEventHandler.onNetworkQuality

```java
public void onNetworkQuality(String uid, int txQuality, int rxQuality)
```

Report the uplink and downlink network quality of each user.

##### Parameter[](#onNetworkQuality)

| Parameter | Description |
| :--- | :--- |
| uid | For each callback, network quality of user corresponding to the uid is reported. If uid is 0, network quality of local user is reported |
| txQuality | Network uplink quality, refer to [ThunderRtcConstant.NetworkQuality](function.md#ThunderRtcConstant.NetworkQuality) |
| rxQuality | Network downlink quality, refer to [ThunderRtcConstant.NetworkQuality](function.md#ThunderRtcConstant.NetworkQuality) |

--------------------------

#### ThunderEventHandler.onRoomStats

```java
public void onRoomStats(ThunderNotification.RoomStats stats)
```

Notification for uplink/downlink traffic (periodic notification sent once every 2 seconds). After joining room [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), user will receive this callback.

##### Parameter[](#onRoomStats)

| Parameter | Description |
| :--- | :--- |
| stats | Upstream and downstream traffic data of the room, see [ThunderNotification.RoomStats](#ThunderNotification.RoomStats) class for details |

--------------------------

#### ThunderEventHandler.onPlayVolumeIndication

```java
public void onPlayVolumeIndication(ThunderEventHandler.AudioVolumeInfo[] speakers, int totalVolume)
```

Report which users are speaking and the speakers' volume.

After calling [ThunderEngine.setAudioVolumeIndication](function.md#ThunderEngine.setAudioVolumeIndication) is enabled, this callback will be received when someone speaks in the room.

##### Parameter[](#onPlayVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| speakers | Audio volume information array. <br>Each speaker includes:<br> uid: speaker's uid. <br>volume: speaker's volume. <br>pts: capture timestamp, <br>refer to [ThunderEventHandler.AudioVolumeInfo](#ThunderEventHandler.AudioVolumeInfo) for detail |
| totalVolume | Total volume (after audio mixing) [0-100] |

--------------------------

#### ThunderEventHandler.onCaptureVolumeIndication

```java
public void onCaptureVolumeIndication(int totalVolume, int cpt, int micVolume)
```

Report the cpature volume

This callback will be received after calling [ThunderEngine.enableCaptureVolumeIndication](function.md#ThunderEngine.enableCaptureVolumeIndication) is enabled.

##### Parameter[](#onCaptureVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| totalVolume | Total volume of capture (including microphone capture and file playback) [0-100] |
| cpt | The timestamp of microphone capture (ms) |
| micVolume | The volume of microphone capture only [0-100] |

--------------------------

#### ThunderEventHandler.onConnectionLost

```java
public void onConnectionLost(){}
```

Callback when losing connection with server.

After calling [joinRoom](function.md#ThunderEngine.joinRoom), regardless of whether joining is successful or not, SDK will trigger this callback as long as server cannot be connected in 10 seconds. Before app proactively calls [leaveRoom](function.md#ThunderEngine.leaveRoom), SDK will be automatically reconnecting.

--------------------------

#### ThunderEventHandler.onAudioPlayData

```java
public void onAudioPlayData(byte[] data, long cpt, long pts, String uid, long duration)
```

Report the audio playback data。

This callback will be received after calling [ThunderEngine.enableAudioDataIndication](function.md#ThunderEngine.enableAudioDataIndication) is enabled.

##### 参数[](#onAudioPlayData)

| 参数 | 描述 |
| :--- | :--- |
| data | Audio data before decoding |
| cpt | Collection timestamp (ms) |
| pts | Play timestamp (ms) |
| uid | User id |
| duration | Audio duration (ms) |

--------------------------

#### ThunderEventHandler.onAudioPlaySpectrumData

```java
public void onAudioPlaySpectrumData(byte[] data)
```

Report the audio playback spectrum data.

This callback will be received after calling [ThunderEngine.enableAudioPlaySpectrum](function.md#ThunderEngine.enableAudioPlaySpectrum) is enabled.

##### Parameter[](#onAudioPlaySpectrumData)

| Parameter | Description |
| :--- | :--- |
| Date | Audio spectrum data |

--------------------------

#### ThunderEventHandler.onRecvUserAppMsgData

```java
public void onRecvUserAppMsgData(byte[] data, String uid)
```

Callback when received developer's custom broadcast messages.

##### Parameter[](#onRecvUserAppMsgData)

| Parameter | Description |
| :--- | :--- |
| Date | Pass-through message received |
| uid | uid of user who sends the message |

--------------------------

#### ThunderEventHandler.onSendAppMsgDataFailedStatus

```java
public void onSendAppMsgDataFailedStatus(int status)
```

Callback when failure in sending deveploper's custom broadcast messages.

##### Parameter[](#onSendAppMsgDataFailedStatus)

| Parameter | Description |
| :--- | :--- |
| status | Failure status <br>1: Frequency is too high <br>2: Data sent is too large <br>3: Publishing is not started successfully |

--------------------------

#### ThunderEventHandler.onRemoteAudioStopped

```java
public void onRemoteAudioStopped(String uid, boolean stop)
```

Callback when the remote user's audio stream starts or stops.

After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), this callback will be received when there are changes in existing audio streams in the room and subsequent audio stream status.

##### Parameter[](#onRemoteAudioStopped)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| Stop | true: Remote user audio stream has stopped <br>false: Remote user audio stream has started |

--------------------------

#### ThunderEventHandler.onRemoteVideoStopped

```java
public void onRemoteVideoStopped(String uid, boolean stop)
```

Callback when the remote user's video stream starts or stops.

After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), this callback will be received when there are changes in existing video streams in the room and subsequent video stream status.

##### Parameter[](#onRemoteVideoStopped)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| Stop | true: Remote user video stream has stopped <br>false: Remote user video stream has started |

--------------------------

#### ThunderEventHandler.onRemoteVideoPlay

```java
public void onRemoteVideoPlay(String uid, int width, int height, int elapsed)
```

Callback when displaying the first frame of remote video.

After calling [ThunderEngine.setRemoteVideoCanvas](function.md#ThunderEngine.setRemoteVideoCanvas), this callback will be received when remote video stream is received and the first frame is displayed

##### Parameter[](#onRemoteVideoPlay)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| width | Remote video resolution width |
| height | Remote video resolution height |
| elapsed | Time elapsed (ms) from calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) to calling back the event |

--------------------------

#### ThunderEventHandler.onVideoSizeChanged

```java
public void onVideoSizeChanged(String uid, int width, int height, int rotation)
```

Callback when the resolution of local or remote video changes.

After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), this callback will be received when the resolution of local or remote video changes.

##### Parameter[](#onVideoSizeChanged)

| Parameter | Description |
| :--- | :--- |
| uid | User id. uid is 0 when callback is received by user as an anchor; uid is anchor uid when callback is received by user a viewer |
| width | Video resolution width after change |
| height | Video resolution height after change |
| rotation | Reserved parameters, not yet realized |

--------------------------

#### ThunderEventHandler.onFirstLocalAudioFrameSent

```java
public void onFirstLocalAudioFrameSent(int elapsed)
```

Callback when first local audio frame sent successfully. (As an anchor, this callback is received after the first audio frame is successfully uploaded)

##### Parameter[](#onFirstLocalAudioFrameSent)

| Parameter | Description |
| :--- | :--- |
| elapsed | Time elapsed (in milliseconds) from local user calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) to triggering this callback |

--------------------------

#### ThunderEventHandler.onFirstLocalVideoFrameSent

```java
public void onFirstLocalVideoFrameSent(int elapsed)
```

Callback when first local video frame sent successfully. (As an anchor, this callback is received after the first video frame is successfully uploaded)

##### Parameter[](#onFirstLocalVideoFrameSent)

| Parameter | Description |
| :--- | :--- |
| elapsed | Time elapsed (in milliseconds) from local user calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom) to triggering this callback |

--------------------------

#### ThunderEventHandler.onPublishStreamToCDNStatus

```java
public void onPublishStreamToCDNStatus(String url, int errorCode)
```

Report the result of pushing stream to the CDN. This callback will be triggered when stream pushing status changes.

This callback will be received after user calling [ThunderEngine.addPublishOriginStreamUrl](function.md#ThunderEngine.addPublishOriginStreamUrl) or [ThunderEngine.addPublishTranscodingStreamUrl](function.md#ThunderEngine.addPublishTranscodingStreamUrl) to pushing stream.

##### Parameter[](#onPublishStreamToCDNStatus)

| Parameter | Description |
| :--- | :--- |
| url | The URL to which the stream will be pushed |
| errorCode | The status code of stream pushing results, referring to [ThunderRtcConstant.ThunderPublishCDNErrorCode](function.md#ThunderRtcConstant.ThunderPublishCDNErrorCode) |

--------------------------

#### ThunderEventHandler.onNetworkTypeChanged

```java
public void onNetworkTypeChanged(int type)
```

Callback when the network type changes.

After creating and initializing engine, this callback will be received when network type changes.

##### Parameter[](#onNetworkTypeChanged)

| Parameter | Description |
| :--- | :--- |
| type | Network type, referring to [ThunderRtcConstant.ThunderNetworkType](function.md#ThunderRtcConstant.ThunderNetworkType) |

--------------------------

#### ThunderEventHandler.onConnectionStatus

```java
public void onConnectionStatus(int status)
```

Report the connection status with the server.

After calling [ThunderEngine.joinRoom](function.md#ThunderEngine.joinRoom), this callback will be received when network connection status between SDK and server (service and avp) changes.

- In thunder mode, only connection status with avp will be checked.
- In thunderbolt mode and without publishing or subscription (not connecting avp), only service connection status will be checked.
- In thunderbolt mode and with publishing or subscription, service and avp connection status will be checked at the same time.

##### Parameter[](#onConnectionStatus)

| Parameter | Description |
| :--- | :--- |
| status | The connection status code with server, refer to [ThunderRtcConstant.ThunderConnectionStatus](function.md#ThunderRtcConstant.ThunderConnectionStatus) |

--------------------------

#### ThunderEventHandler.onAudioCaptureStatus

```java
public void onAudioCaptureStatus(int status)
```

Callback when the audio device capture status changes.

Start audio capture. This callback will be received in case of changes in audio device capture status.

##### Parameter[](#onAudioCaptureStatus)

| Parameter | Description |
| :--- | :--- |
| status | The audio device capture status, refer to [ThunderRtcConstant.ThunderAudioDeviceStatus](function.md#ThunderRtcConstant.ThunderAudioDeviceStatus) |

--------------------------

#### ThunderEventHandler.onVideoCaptureStatus

```java
public void onVideoCaptureStatus(int status)
```

Callback when the video device capture status changes.

Start camera capture. This callback will be received when there are changes in camera device capture status.

##### Parameter[](#onVideoCaptureStatus)

| Parameter | Description |
| :--- | :--- |
| status | The video device (camera) capture status, refer to [ThunderRtcConstant.ThunderVideoCaptureStatus](function.md#ThunderRtcConstant.ThunderVideoCaptureStatus) |

--------------------------

#### ThunderEventHandler.onLocalVideoStats

```java
public void onLocalVideoStats(ThunderEventHandler.LocalVideoStats stats)
```

Report statistics of local video streams.

This callback describes statistics of video streams sent locally. Callback timing is as follows:

- Immediate callback when calling the publishing interface
- Immediate callback on bracket change during publishing
- Periodic callback at an interval of 2s

##### Parameter[](#onLocalVideoStats)

| Parameter | Description |
| :--- | :--- |
| stats | The statistics of local video, refer to [ThunderEventHandler.LocalVideoStats](#ThunderEventHandler.LocalVideoStats) |

--------------------------

#### ThunderEventHandler.onLocalAudioStats

```java
public void onLocalAudioStats(ThunderEventHandler.LocalAudioStats stats)
```

Report the statistics of the local audio stream.

This callback describes statistics of audio streams sent locally. Callback timing: periodic callback at an interval of 2s

##### Parameter[](#onLocalAudioStats)

| Parameter | Description |
| :--- | :--- |
| stats | The statistics of local audio , refer to [ThunderEventHandler.LocalAudioStats](#ThunderEventHandler.LocalAudioStats) |

--------------------------

#### ThunderEventHandler.onRemoteVideoStatsOfUid

```java
public void onRemoteVideoStatsOfUid(String uid, ThunderEventHandler.RemoteVideoStats stats)
```

Report status message of remote video stream during the call.

This callback describes end-to-end video streaming status of remote user during the call. For each remote user (anchor), it is triggered once every 2 seconds. In case multiple remote users (anchors) exist at the same time, this callback will be triggered multiple times every 2 seconds

##### Parameter[](#onRemoteVideoStatsOfUid)

| Parameter | Description |
| :--- | :--- |
| uid | The uid of remote user (anchor) |
| stats | The status message of remote video , refer to [ThunderEventHandler.RemoteVideoStats](#ThunderEventHandler.RemoteVideoStats) |

--------------------------

#### ThunderEventHandler.onRemoteAudioStatsOfUid

```java
public void onRemoteAudioStatsOfUid(String uid, ThunderEventHandler.RemoteAudioStats stats)
```

Report status message of remote audio stream during the call.

This callback describes end-to-end audio streaming status of remote user during the call. For each remote user (anchor), it is triggered once every 2 seconds. In case multiple remote users (anchors) exist at the same time, this callback will be triggered multiple times every 2 seconds

##### Parameter[](#onRemoteAudioStatsOfUid)

| Parameter | Description |
| :--- | :--- |
| uid | The uid of remote user (anchor) |
| stats | The status message of remote audio, refer to [ThunderEventHandler.RemoteAudioStats](#ThunderEventHandler.RemoteAudioStats) |

--------------------------

### IAudioFrameObserver

#### IAudioFrameObserver.onRecordAudioFrame

```java
boolean onRecordAudioFrame(ByteBuffer samples,
                           int numOfSamples,
                           int bytesPerSample,
                           int channels,
                           int samplesPerSec)
```

Report the raw audio capture data.

##### Parameter[](#onRecordAudioFrame)

| Parameter | Description |
| :--- | :--- |
| samples | Sample data of this frame |
| numOfSamples | Number of samples |
| bytesPerSample | Bytes per sample: For PCM, 16 bits are used in general, that is, two bytes |
| channels | Number of channels (crossed data for stereo); 1: single track, 2: dual track |
| samplesPerSec | Sampling rate, SamplesPerCall = (int)(SampleRate × sampleInterval); where, sample ≥ 0.01, in seconds |

##### Return value[](#onRecordAudioFrame)

- True.

--------------------------

#### IAudioFrameObserver.onPlaybackAudioFrame

```java
boolean onPlaybackAudioFrame(ByteBuffer samples,
                             int numOfSamples,
                             int bytesPerSample,
                             int channels,
                             int samplesPerSec)
```

Report the raw audio play data.

##### Parameter[](#onPlaybackAudioFrame)

| Parameter | Description |
| :--- | :--- |
| samples | Sample data of this frame |
| numOfSamples | Number of samples |
| bytesPerSample | Bytes per sample: For PCM, 16 bits are used in general, that is, two bytes |
| channels | Number of channels (crossed data for stereo); 1: single track, 2: dual track |
| samplesPerSec | Sampling rate, SamplesPerCall = (int)(SampleRate × sampleInterval); where, sample ≥ 0.01, in seconds |

##### Return value[](#onPlaybackAudioFrame)

- True.

--------------------------

#### IAudioFrameObserver.onPlaybackAudioFrameBeforeMixing

```java
boolean onPlaybackAudioFrameBeforeMixing(String uid,
                                         ByteBuffer samples,
                                         int numOfSamples,
                                         int bytesPerSample,
                                         int channels,
                                         int samplesPerSec)
```

Report the raw decoded audio data of remote user.

##### Parameter[](#onPlaybackAudioFrameBeforeMixing)

| Parameter | Description |
| :--- | :--- |
| uid | Remote user uid |
| samples | Sample data of this frame |
| numOfSamples | Number of samples |
| bytesPerSample | Bytes per sample: For PCM, 16 bits are used in general, that is, two bytes |
| channels | Number of channels (crossed data for stereo); 1: single track, 2: dual track |
| samplesPerSec | Sampling rate, SamplesPerCall = (int)(SampleRate × sampleInterval); where, sample ≥ 0.01, in seconds |

##### Return value[](#onPlaybackAudioFrameBeforeMixing)

- True.

--------------------------

### IGPUProcess

#### IGPUProcess.onInit

```java
void onInit(int textureTarget, int outputWidth, int outputHeight)
```

Allow developers to use third-party special effects.

Including "Update texture type" and “Use shader in OES texture".

##### Parameter[](#onInit)

| Parameter | Description |
| :--- | :--- |
| textureTarget | Texture type ( GL_TEXTURE_EXTERNAL_OES / GL_TEXTURE_2D ) |
| outputWidth | Texture width |
| outputHeight | Texture height |

--------------------------

#### IGPUProcess.onDestroy

```java
void onDestroy()
```

Destroying resources of special effects.

--------------------------

#### IGPUProcess.onDraw

```java
void onDraw(final int textureId,
            final FloatBuffer cubeBuffer,
            final FloatBuffer textureBuffer,
            float[] texMatrix)
```

Process every frame.

##### Parameter[](#onDraw)

| Parameter | Description |
| :--- | :--- |
| textureId | Texture ID |
| cubeBuffer | Vertex coordinates |
| textureBuffer | Texture coordinates |
| texMatrix | Texture matrix |

--------------------------

#### IGPUProcess.onOutputSizeChanged

```java
void onOutputSizeChanged(final int width, final int height)
```

Callback when the texture size update.

##### Parameter[](#onOutputSizeChanged)

| Parameter | Description |
| :--- | :--- |
| width | Updated texture width |
| height | Updated texture height |

--------------------------

### IVideoCaptureObserver

#### IVideoCaptureObserver.onCaptureVideoFrame

```java
void onCaptureVideoFrame(int width, int height, byte[] data, int length, int imageFormat)
```

Callback original yuv (NV21) data captured by camera to developer.

##### Parameter[](#onCaptureVideoFrame)

| Parameter | Description |
| :--- | :--- |
| width | Video frame width |
| height | Video frame height |
| Date | NV21 data of video frame |
| length | Video frame length |
| imageFormat | Video image format. For the optional value, refer to class android.graphics.ImageFormat |

--------------------------

### IVideoDecodeObserver

#### IVideoDecodeObserver.onVideoDecodeFrame

```java
void onVideoDecodeFrame(String uid, int w, int h, byte[] data, int dateLen, long renderTimeMs)
```

Callback decoded video data for rendering (I420) to developer

##### Parameter[](#onVideoDecodeFrame)

| Parameter | Description |
| :--- | :--- |
| uid | uid of user to whom video frame belongs |
| w | Video frame width |
| h | Video frame height |
| Date | I420 data of video frame |
| dateLen | Video frame length |
| renderTimeMs | Current rendering timestamp |

--------------------------

### ThunderCustomVideoSource

#### ThunderCustomVideoSource.onInitialize

```java
boolean onInitialize(ThunderVideoFrameConsumer consumer)
```

Initialize video source.

In this callback function, external video stream is pushed by calling consumer.consumeByteArrayFrame.

##### Parameter[](#onInitialize)

| Parameter | Description |
| :--- | :--- |
| consumer | The interface object for pushing external video stream, refer to [ThunderVideoFrameConsumer](#ThunderVideoFrameConsumer) |

##### Return value[](#onInitialize)

- True.

--------------------------

#### ThunderCustomVideoSource.onStart

```java
boolean onStart()
```

Start video source.

##### Return value[](#onStart)

- True.

--------------------------

#### ThunderCustomVideoSource.onStop

```java
boolean onStop()
```

Stop video source.

##### Return value[](#onStop)

- True.

--------------------------

#### ThunderCustomVideoSource.onDispose

```java
boolean onDispose()
```

Dispose video source.

##### Return value[](#onDispose)

- True.

--------------------------

### ThunderVideoFrameConsumer

#### ThunderVideoFrameConsumer.consumeByteArrayFrame

```java
void consumeByteArrayFrame(byte[] data, int format, int width, int height, int rotation, long timestamp)
```

Receive video frames of type ByteArray.

Call this function to transmit video frame of type ByteArray to SDK, and SDK will push this video frame out.

##### Parameter[](#consumeByteArrayFrame)

| Parameter | Description |
| :--- | :--- |
| Date | Byte Array type of video data |
| format | Pixel format. For optional values, refer to [ThunderRtcConstant.ExternalVideoPixelFormat](function.md#ThunderRtcConstant.ExternalVideoPixelFormat) |
| width | Video frame width |
| height | Video frame height |
| rotation | Clockwise rotation angle for video frame. If rotation angle is defined, media engine will rotate image. <br>You may set angle value to 0, 90, 180 or 270 degrees as needed. If it is set to other values, the system will automatically ignore |
| timestamp | Timestamp of incoming video frame. Developer must set a timestamp for each video frame |

--------------------------

### IThunderLogCallback

#### IThunderLogCallback.onThunderLogWithLevel

```java
void onThunderLogWithLevel(int level, String tag, String msg)
```

Report the log information.

After setting this callback, log messages will be called back through this interface.

##### Parameter[](#onThunderLogWithLevel)

| Parameter | Description |
| :--- | :--- |
| level | Log level, refer to [ThunderRtcConstant.ThunderLogLevel](function.md#ThunderRtcConstant.ThunderLogLevel) |
| tag | Log tag |
| msg | Log content |

--------------------------

### IThunderMediaExtraInfoCallback

#### IThunderMediaExtraInfoCallback.onSendMediaExtraInfoFailedStatus

```java
void onSendMediaExtraInfoFailedStatus(int status)
```

Callback when failure in sending media extra information.

##### Parameter[](#onSendMediaExtraInfoFailedStatus)

| Parameter | Description |
| :--- | :--- |
| status | Failure error code, refer to [ThunderRtcConstant.ThunderSendMediaExtraInfoFailedStatus](function.md#ThunderRtcConstant.ThunderSendMediaExtraInfoFailedStatus) |

--------------------------

#### IThunderMediaExtraInfoCallback.onRecvMediaExtraInfo

```java
void onRecvMediaExtraInfo(java.lang.String uid,
                          java.nio.ByteBuffer data,
                          int dataLen)
```

Callback when received media extra information.

##### Parameter[](#onRecvMediaExtraInfo)

| Parameter | Description |
| :--- | :--- |
| uid | Anchor uid |
| Date | Received media extra information |
| dataLen | Length of media extra information |

--------------------------

#### IThunderMediaExtraInfoCallback.onRecvMixAudioInfo

```java
void onRecvMixAudioInfo(java.lang.String uid, ArrayList<ThunderEventHandler.MixAudioInfo> infos)
```

Callback when received extra information of mixed audio stream.

##### Parameter[](#onRecvMixAudioInfo)

| Parameter | Description |
| :--- | :--- |
| uid | Mixed audio stream uid |
| infos | Raw stream data of mixed audio stream, identifying which streams contribute to this mixed audio stream, refer to [ThunderEventHandler.MixAudioInfo](#ThunderEventHandler.MixAudioInfo) |

--------------------------

#### IThunderMediaExtraInfoCallback.onRecvMixVideoInfo

```java
void onRecvMixVideoInfo(java.lang.String uid, ArrayList<ThunderEventHandler.MixVideoInfo> infos)
```

Callback when received extra information of mixed video stream.

##### Parameter[](#onRecvMixVideoInfo)

| Parameter | Description |
| :--- | :--- |
| uid | Mixed video stream uid |
| infos | Raw stream data of mixed video stream, identifying which streams contribute to this mixed video stream and stream, refer to [ThunderEventHandler.MixVideoInfo](#ThunderEventHandler.MixVideoInfo) |

--------------------------

### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayError

```java
void onAudioFilePlayError(int errorCode)
```

 Callback when audio file playing occur error

##### Parameter[](#onAudioFilePlayError)

| Parameter | Description |
| :--- | :--- |
| errorCode | Audio file playback error codes |

Meaning of error codes:

| Error code | Meaning |
| :---: | :--- |
| 0 | File opened successfully |
| -1 | Error parsing file format |
| -2 | Error decoding file format |
| -3 | File format is not supported |
| -4 | File path not in existence |

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileVolume

```java
void onAudioFileVolume(long volume, long currentMs, long totalMs)
```

Report the volume of the playing audio file.

##### Parameter[](#onAudioFileVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Volume value [0-100] |
| currentMs | play progress (in milliseconds) |
| totalMs | Total file length (in milliseconds) |

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileSeekComplete

```java
void onAudioFileSeekComplete(int millisecond)
```

Callback when the audio file seeking is completed.

##### Parameter[](#onAudioFileSeekComplete)

| Parameter | Description |
| :--- | :--- |
| millisecond | Actual fast forward progress |

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlaying

```java
void onAudioFilePlaying()
```

Callback when start playback.

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePause

```java
void onAudioFilePause()
```

Callback when pause playback.

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileResume

```java
void onAudioFileResume()
```

Callback when resume playback.

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileStop

```java
void onAudioFileStop()
```

Callback when playback being stopped by user.

--------------------------

#### ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayEnd

```java
void onAudioFilePlayEnd()
```

Callback when end playback.

--------------------------

## Parameter type

### ThunderEventHandler internal parameter class

#### ThunderEventHandler.AudioVolumeInfo

Speaker volume information class

```java
public static class AudioVolumeInfo {
        public String uid;//Speaker uid
        public int volume;//Speaker volume
        public int pts;//Capture timestamp
}
```

--------------------------

#### ThunderEventHandler.RoomStats

Reserved parameter class, not yet realized

[Used in interface ThunderEventHandler.onLeaveRoom](#ThunderEventHandler.onLeaveRoom).

```java
public static class RoomStats {
        public int temp;
}
```

--------------------------

#### ThunderEventHandler.MixAudioInfo

Audio stream information for audio mixing.

```java
public static class MixAudioInfo {
        public String uid;//User uid to which the audio stream belongs
        public int volume;//Volume value of audio stream [0,100]
    }
```

--------------------------

#### ThunderEventHandler.MixVideoInfo

Video stream information for video mixing (including video stream layout)

```java
public static class MixVideoInfo {
        public String uid;   //User id
        public int width;    //Original width of this user's video
        public int height;   //Original height of this user's video
        public int cropX;    //X coordinate of the begin point used to crop the original video in video mixing
        public int cropY;    //Y coordinate of the begin point used to crop the original video in video mixing
        public int cropW;    //Width of the original video to be cropped in video mixing
        public int cropH;    //Height of the original video to be cropped in video mixing
        public int layoutX;  //X coordinate of the begin point of this user's video in video mixing canvas
        public int layoutY;  //Y coordinate of the begin point of this user's video in video mixing canvas
        public int layoutW;  //Width of this user's video in video mixing canvas
        public int layoutH;  //Height of this user's video in video mixing canvas
        public int zOrder;   //Layer number of this user's video frame in video mixing. The value range is the integer in [0, 100], and the minimum value is 0, indicating that the image in this region is at the lowest level
        public float alpha;  //Transparency of this user's video frame in video mixing. The value range is [0.0, 1.0]. 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque.
    }
```

--------------------------

#### ThunderEventHandler.LocalVideoStats

Local video statistics class

```java
public static class LocalVideoStats {
        public  int sentBitrate;            // Actual sending bit rate (unit: Kbps), with the exception of sending bit rate of reloaded videos after packet loss
        public  int sentFrameRate;          // Actual sending frame rate (unit: fps), with the exception of sending frame rate of reloaded videos after packet loss
        public  int renderOutputFrameRate;  // Output frame rate of local preview (unit: fps)
        public  int targetBitRate;          // Target encoding bit rate of current encoder (unit: Kbps). This bit rate is a value estimated by this SDK in accordance with current network status.
        public  int targetFrameRate;        // Target encoding frame rate of current coder (unit: fps)
        public  int qualityAdaptIndication; // Quality adaptability of local videos since last statistics (based on target frame rate and target bit rate), see ThunderRtcConstant.ThunderVideoQualityAdapt for detailed definition
        public  int encoderOutputFrameRate; // Output frame rate of local encoder (unit: fps)
        public  int encodedBitrate;         // Bit rate of video encoding (Kbps). This parameter includes no encoding bit rate of reloaded videos after packet loss.
        public  int encodedFrameWidth;      // Encoded video width (px)
        public  int encodedFrameHeight;     // Encoded video height (px)
        public  int encodedFrameCount;      // Number of frames sent by video, an accumulated value
        public  int codecType;              // Encoding type, see ThunderRtcConstant.ThunderVideoCodecType for detailed definition
        public  int configBitRate;          // Bit rate configured in the background, kbps
        public  int configFrameRate;        // Frame rate configured in the background
        public  int configWidth;            // Video width configured in the background
        public  int configHeight;           // Video height configured in the background
}
```

--------------------------

#### ThunderEventHandler.LocalAudioStats

Local audio statistics class

```java
public static class LocalAudioStats {
        public int numChannels;    // Number of channels
        public int sendSampleRate; // Sampling rate sent (unit: Hz)
        public int sendBitrate;    // Average value of bit rate of sent data (unit: Kbps)
}
```

--------------------------

#### ThunderEventHandler.RemoteVideoStats

Remote video statistics class

```java
public static class RemoteVideoStats {
        public int delay; // Captured play delay
        public int width;  // Width of remote video stream
        public int height;  // Height of remote video stream
        public int receivedBitrate;  // Receiving bit rate (unit: Kbps)
        public int decoderOutputFrameRate;  // Output frame rate of remote video decoder (unit: fps)
        public int rendererOutputFrameRate; // Output frame rate of remote video renderer (unit: fps)
        public int packetLossRate; // Packet loss rate (%) of remote video after network confrontation
        public int rxStreamType; // Types of video stream, including large stream and small stream
        public int totalFrozenTime; // The accumulated time (ms) from the time when a remote user joins a channel to the time of video freezing
        public int frozenRate; // The percentage (%) of the accumulated time (from the time when a remote user joins a channel to the time of video freezing) accounting for total effective time of videos
}
```

--------------------------

#### ThunderEventHandler.RemoteAudioStats

Remote audio statistics class

```java
public static class RemoteAudioStats {
        public int quality;  //Quality of audio streams sent by remote users.
                             //0: Unknown;
                             //1: Excellent;
                             //2: Good;
                             //3: Poor, flawed but does not affect communication;
                             //4: Bad, communication can be made but not smoothly;
                             //5: Very Bad, communication can barely be made;
                             //6: Disconnected, communication can not be made at all
        public int networkTransportDelay;  // Network delay from an audio sending end to an audio receiving end
        public int jitterBufferDelay;  // Delay from a receiving end to network jitter buffer
        public int frameLossRate;  // Frame loss rate (%) of remote audio streams
        public int numChannels;  // Number of channels
        public int receivedSampleRate; // Sampling rate (Hz) of remote audios
        public int receivedBitrate; // Average bit rate of remote audios within a statistical period
        public int totalFrozenTime; // The accumulated time (ms) from the time when a remote user joins a channel to the time of audio freezing; during one statistical period, an audio frame loss rate of 4% is recorded as a single freeze
                                    // totalFrozenTime = number of times of audio freezing * 2 * 1000 (ms)
        public int frozenRate; // The percentage (%) of the accumulated time (from the time when a remote user joins a channel to the time of audio freezing) accounting for total effective time of audios
}
```

--------------------------

#### ThunderNotification.RoomStats

Uplink/downlink traffic data in the room class

```java
public static class RoomStats {
        public int txBitrate; //Chain sending bit rate (unit: bps)
        public int rxBitrate; //Chain receiving bit rate (unit: bps)
        public int txAudioBitrate;  //Audio packet sending bit rate (unit: bps)
        public int rxAudioBitrate;  //Audio packet receiving bit rate (unit: bps)
        public int txVideoBitrate;  //Video packet sending bit rate (unit: bps)
        public int rxVideoBitrate;  //Video packet receiving bit rate (unit: bps)
}
```

--------------------------
