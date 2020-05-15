# Functional Interface

## Interface List

- ### ThunderEngine

| Static Public member function | Function Name |
| ---:| :--- |
| static synchronized ThunderEngine | [createEngine](#ThunderEngine.createEngine)(Context context, String appId, long sceneId, ThunderEventHandler handler) |
| static synchronized ThunderEngine | [createWithLoop](#ThunderEngine.createWithLoop)(Context context, String appId, long sceneId, ThunderEventHandler handler, Looper loop) |
| static synchronized void | [destroyEngine](#ThunderEngine.destroyEngine)() |
| static String | [getVersion](#ThunderEngine.getVersion)() |
| static int | [setLogLevel](#ThunderEngine.setLogLevel)(int filter) |
| static int | [setLogFilePath](#ThunderEngine.setLogFilePath)(String filePath) |
| static int | [setLogCallback](#ThunderEngine.setLogCallback)([IThunderLogCallback](.mdnotification.md#IThunderLogCallback) callback) |

| Public member functions | Function Name |
| ---:| :--- |
| void | [setSceneId](#ThunderEngine.setSceneId)(long sceneId) |
| int | [setMediaMode](#ThunderEngine.setMediaMode)(int mode) |
| int | [setRoomMode](#ThunderEngine.setRoomMode)(int mode) |
| int | [setArea](#ThunderEngine.setArea)(int area) |
| int | [joinRoom](#ThunderEngine.joinRoom)(byte[] token, String roomName, String uid) |
| int | [leaveRoom](#ThunderEngine.leaveRoom)() |
| int | [updateToken](#ThunderEngine.updateToken)(byte[] token) |
| int | [setAudioConfig](#ThunderEngine.setAudioConfig)(int profile, int commutMode, int scenarioMode) |
| int | [enableVoicePosition](#ThunderEngine.enableVoicePosition)(boolean enable) |
| int | [setRemoteUidVoicePosition](#ThunderEngine.setRemoteUidVoicePosition)(String uid, int azimuth, int gain) |
| int | [enableLoudspeaker](#ThunderEngine.enableLoudspeaker)(boolean enable) |
| int | [isLoudspeakerEnabled](#ThunderEngine.isLoudspeakerEnabled)() |
| int | [setLoudSpeakerVolume](#ThunderEngine.setLoudSpeakerVolume)(int volume) |
| int | [setAudioVolumeIndication](#ThunderEngine.setAudioVolumeIndication)(int interval, int moreThanThd, int lessThanThd, int smooth) |
| int | [enableCaptureVolumeIndication](#ThunderEngine.enableCaptureVolumeIndication)(int interval, int moreThanThd, int lessThanThd, int smooth) |
| boolean | [startAudioSaver](#ThunderEngine.startAudioSaver)(String fileName, int saverMode, int fileMode) |
| boolean | [stopAudioSaver](#ThunderEngine.stopAudioSaver)() |
| void | [setSoundEffect](#ThunderEngine.setSoundEffect)(int mode) |
| void | [setVoiceChanger](#ThunderEngine.setVoiceChanger)(int mode) |
| int | [stopLocalAudioStream](#ThunderEngine.stopLocalAudioStream)(boolean stop) |
| int | [stopRemoteAudioStream](#ThunderEngine.stopRemoteAudioStream)(String uid, boolean stop) |
| int | [stopAllRemoteAudioStreams](#ThunderEngine.stopAllRemoteAudioStreams)(boolean stop) |
| int | [setMicVolume](#ThunderEngine.setMicVolume)(int volume) |
| int | [setRemoteAudioStreamsVolume](#ThunderEngine.setRemoteAudioStreamsVolume)(String uid, int volume) |
| [ThunderAudioFilePlayer](#ThunderAudioFilePlayer) | [createAudioFilePlayer](#ThunderEngine.createAudioFilePlayer)() |
| void | [destroyAudioFilePlayer](#ThunderEngine.destroyAudioFilePlayer)([ThunderAudioFilePlayer](#ThunderAudioFilePlayer) audioFilePlayer) |
| int | [setEnableEqualizer](#ThunderEngine.setEnableEqualizer)(boolean enabled) |
| int | [setEqGains](#ThunderEngine.setEqGains)(final int[] gains) |
| int | [setEnableReverb](#ThunderEngine.setEnableReverb)(boolean enabled) |
| int | [setReverbExParameter](#ThunderEngine.setReverbExParameter)([ReverbExParameter](#ThunderRtcConstant.ReverbExParameter) param) |
| int | [setEnableCompressor](#ThunderEngine.setEnableCompressor)(boolean enabled) |
| int | [setCompressorParam](#ThunderEngine.setCompressorParam)([CompressorParam](#ThunderRtcConstant.CompressorParam) param) |
| int | [setEnableLimiter](#ThunderEngine.setEnableLimiter)(boolean enabled) |
| int | [setLimiterParam](#ThunderEngine.setLimiterParam)([LimterParam](#ThunderRtcConstant.LimterParam) param) |
| void | [enableAudioPlaySpectrum](#ThunderEngine.enableAudioPlaySpectrum)(boolean enable) |
| void | [setAudioPlaySpectrumInfo](#ThunderEngine.setAudioPlaySpectrumInfo)(int spectrumLen, int notifyIntervalMS) |
| int | [sendUserAppMsgData](#ThunderEngine.sendUserAppMsgData)(byte[] msgData) |
| int | [sendMediaExtraInfo](#ThunderEngine.sendMediaExtraInfo)(ByteBuffer data, int dataLen) |
| int | [setMediaExtraInfoCallback](#ThunderEngine.setMediaExtraInfoCallback)([IThunderMediaExtraInfoCallback](.mdnotification.md#IThunderMediaExtraInfoCallback) callback) |
| int | [enableMixVideoExtraInfo](#ThunderEngine.enableMixVideoExtraInfo)(boolean enable) |
| void | [enableAudioDataIndication](#ThunderEngine.enableAudioDataIndication)(boolean enablePlay) |
| void | [setAudioSourceType](#ThunderEngine.setAudioSourceType)(int sourceType) |
| int | [setEnableInEarMonitor](#ThunderEngine.setEnableInEarMonitor)(boolean enable) |
| int | [setVideoEncoderConfig](#ThunderEngine.setVideoEncoderConfig)([ThunderVideoEncoderConfiguration](#ThunderVideoEncoderConfiguration) yyVideoConfig) |
| int | [setLocalVideoCanvas](#ThunderEngine.setLocalVideoCanvas)([ThunderVideoCanvas](#ThunderVideoCanvas) local) |
| int | [setRemotePlayType](#ThunderEngine.setRemotePlayType)(int remotePlayType) |
| int | [setMultiVideoViewLayout](#ThunderEngine.setMultiVideoViewLayout)([ThunderMultiVideoViewParam](#ThunderMultiVideoViewParam) params) |
| int | [setRemoteVideoCanvas](#ThunderEngine.setRemoteVideoCanvas)([ThunderVideoCanvas](#ThunderVideoCanvas) remote) |
| int | [setLocalCanvasScaleMode](#ThunderEngine.setLocalCanvasScaleMode)(int mode) |
| int | [setRemoteCanvasScaleMode](#ThunderEngine.setRemoteCanvasScaleMode)(String uid, int mode) |
| int | [startVideoPreview](#ThunderEngine.startVideoPreview)() |
| int | [stopVideoPreview](#ThunderEngine.stopVideoPreview)() |
| int | [enableLocalVideoCapture](#ThunderEngine.enableLocalVideoCapture)((boolean enable) |
| int | [stopLocalVideoStream](#ThunderEngine.stopLocalVideoStream)(boolean stop) |
| int | [stopRemoteVideoStream](#ThunderEngine.stopRemoteVideoStream)(String uid, boolean stop) |
| int | [stopAllRemoteVideoStreams](#ThunderEngine.stopAllRemoteVideoStreams)(boolean stop) |
| int | [registerVideoCaptureTextureObserver](#ThunderEngine.registerVideoCaptureTextureObserver)([IGPUProcess](.mdnotification.md#IGPUProcess) observer) |
| int | [registerVideoCaptureFrameObserver](#ThunderEngine.registerVideoCaptureFrameObserver)([IVideoCaptureObserver](.mdnotification.md#IVideoCaptureObserver) observer) |
| int | [registerVideoDecodeFrameObserver](#ThunderEngine.registerVideoDecodeFrameObserver)(String uid, [IVideoDecodeObserver](.mdnotification.md#IVideoDecodeObserver) observer) |
| int | [registerAudioFrameObserver](#ThunderEngine.registerAudioFrameObserver)([IAudioFrameObserver](.mdnotification.md#IAudioFrameObserver) observer) |
| int | [setRecordingAudioFrameParameters](#ThunderEngine.setRecordingAudioFrameParameters)(int sampleRate, int room, int mode, int samplesPerCall) |
| int | [setPlaybackAudioFrameParameters](#ThunderEngine.setPlaybackAudioFrameParameters)(int sampleRate, int room, int mode, int samplesPerCall) |
| int | [setVideoWatermark](#ThunderEngine.setVideoWatermark)([ThunderBoltImage](#ThunderBoltImage) watermark) |
| int | [setCustomAudioSource](#ThunderEngine.setCustomAudioSource)(boolean enabled, int sampleRate, int channel) |
| int | [pushCustomAudioFrame](#ThunderEngine.pushCustomAudioFrame)(byte[] data, long timeStamp) |
| int | [setCustomVideoSource](#ThunderEngine.setCustomVideoSource)([ThunderCustomVideoSource](.mdnotification.md#ThunderCustomVideoSource) videoSource) |
| int | [addPublishOriginStreamUrl](#ThunderEngine.addPublishOriginStreamUrl)(String url) |
| int | [removePublishOriginStreamUrl](#ThunderEngine.removePublishOriginStreamUrl)(String url) |
| int | [setLiveTranscodingTask](#ThunderEngine.setLiveTranscodingTask)(String taskId, [LiveTranscoding](#LiveTranscoding) transcoding) |
| int | [removeLiveTranscodingTask](#ThunderEngine.removeLiveTranscodingTask)(String taskId) |
| int | [addPublishTranscodingStreamUrl](#ThunderEngine.addPublishTranscodingStreamUrl)(String taskId, String url) |
| int | [removePublishTranscodingStreamUrl](#ThunderEngine.removePublishTranscodingStreamUrl)(String taskId, String url) |
| int | [addSubscribe](#ThunderEngine.addSubscribe)(String roomId, String uid) |
| int | [removeSubscribe](#ThunderEngine.removeSubscribe)(String roomId, String uid) |
| int | [switchFrontCamera](#ThunderEngine.switchFrontCamera)(boolean bFront) |
| int | [setVideoCaptureOrientation](#ThunderEngine.setVideoCaptureOrientation)(int orientation) |
| int | [setLocalVideoMirrorMode](#ThunderEngine.setLocalVideoMirrorMode)(int mode) |
| int | [enableWebSdkCompatibility](#ThunderEngine.enableWebSdkCompatibility)(boolean enabled) |

- ### ThunderAudioFilePlayer

| public member functions | Function Name |
| ---:| :--- |
| void | [open](#ThunderAudioFilePlayer.open)(String path) |
| void | [close](#ThunderAudioFilePlayer.close)() |
| void | [play](#ThunderAudioFilePlayer.play)() |
| void | [stop](#ThunderAudioFilePlayer.stop)() |
| void | [pause](#ThunderAudioFilePlayer.pause)() |
| void | [resume](#ThunderAudioFilePlayer.resume)() |
| void | [seek](#ThunderAudioFilePlayer.seek)(long timeMS) |
| long | [getTotalPlayTimeMS](#ThunderAudioFilePlayer.getTotalPlayTimeMS)() |
| long | [getCurrentPlayTimeMS](#ThunderAudioFilePlayer.getCurrentPlayTimeMS)() |
| void | [setPlayVolume](#ThunderAudioFilePlayer.setPlayVolume)(int volume) |
| int | [setPlayerLocalVolume](#ThunderAudioFilePlayer.setPlayerLocalVolume)(int volume) |
| int | [setPlayerPublishVolume](#ThunderAudioFilePlayer.setPlayerPublishVolume)(int volume) |
| int | [getPlayerLocalVolume](#ThunderAudioFilePlayer.getPlayerLocalVolume)() |
| int | [getPlayerPublishVolume](#ThunderAudioFilePlayer.getPlayerPublishVolume)() |
| int | [getAudioTrackCount](#ThunderAudioFilePlayer.getAudioTrackCount)() |
| int | [selectAudioTrack](#ThunderAudioFilePlayer.selectAudioTrack)(int audioTrack) |
| void | [setSemitone](#ThunderAudioFilePlayer.setSemitone)(int val) |
| int | [setLooping](#ThunderAudioFilePlayer.setLooping)(int cycle) |
| void | [enablePublish](#ThunderAudioFilePlayer.enablePublish)(boolean enable) |
| synchronized void | [setPlayerNotify](#ThunderAudioFilePlayer.setPlayerNotify)([IThunderAudioFilePlayerCallback](.mdnotification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback) callback) |
| synchronized void | [enableVolumeIndication](#ThunderAudioFilePlayer.enableVolumeIndication)(boolean enable, int interval) |
| synchronized void | [setMixStandard](#ThunderAudioFilePlayer.setMixStandard)(boolean standard) |
| synchronized boolean | [isMixStandard](#ThunderAudioFilePlayer.isMixStandard)() |

## Detailed Introduction for Interfaces

> Introduction: If the return value of API is int, unless otherwise specified, 0 indicates a successful call, and less than 0 indicates a failed call. For detailed return code, see [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

### ThunderEngine

#### ThunderEngine.createEngine

```java
public static synchronized ThunderEngine createEngine(Context context,
                                                      String appId,
                                                      long sceneId,
                                                      ThunderEventHandler handler)
```

Create ThunderEngine and initialize ThunderEngine instance.

##### Description[](#createEngine)

- Now, the SDK only supports one ThunderEngine instance, indicating that it can be only created one by application.
- Unless otherwise specified, all interface functions of ThunderEngine are asynchronously called, and the interface is called in the same thread.
- SceneId is used to differentiate scenes of the same business, contributing to analyze data based on them.
- This method needs to be called on the main thread.

> **Note:**
>
> - Users of the same AppId can communicate with each other.

##### Parameter[](#createEngine)

| Parameter | Description |
| :--- | :--- |
| context | The context of the Android Application |
| appId | The signed AppId for applications |
| sceneId | The scene Id customized by the developer can subdivide business scenes; if unnecessary, fill 0 |
| handler | ThunderEventHandler is a abstract object providing default implementation, by which SDK can report events to applications when SDK is running. |

##### Return[](#createEngine)

- ThunderEngine instance object

--------------------------

#### ThunderEngine.createWithLoop

```java
public static synchronized ThunderEngine createWithLoop(Context context,
                                                        String appId,
                                                        long sceneId,
                                                        ThunderEventHandler handler,
                                                        Looper loop)
```

Create ThunderEngine and initialize ThunderEngine instance.

##### Description[](#createWithLoop)

- Now, the SDK only supports one ThunderEngine instance, indicating that it can be only created by one application.
- Unless otherwise specified, all interface functions of ThunderEngine are asynchronously called, and the interface is called in the same thread.
- SceneId is used to differentiate scenes of the same business, contributing to analyze data based on them.

> **Note:**
>
> - Users of the same AppId can communicate with each other.

##### Parameter[](#createWithLoop)

| Parameter | Description |
| :--- | :--- |
| context | The context of the Android Application |
| appId | AppID signed for application developers |
| sceneId | The scene Id customized by the developer can subdivide business scenes; if unnecessary, fill 0 |
| handler | ThunderEventHandler is an abstract object providing default implementation, by which SDK can call back events from applications when SDK is running. |
| loop | Looper objects correlated with thread can assign handler callback function to be performed in Associated thread. |

##### Return[](#createWithLoop)

- ThunderEngine instance object

--------------------------

#### ThunderEngine.destroyEngine

```java
public static synchronized void destroyEngine()
```

Destroy ThunderEngine instance object

##### Description[](#destroyEngine)

- This method releases all resources used by SDK.
- Some applications only operate voice communication required by users. Resources can be released for other operations if they are not needed. This method may be applicable for such applications.
- If [destroyEngine](#ThunderEngine.destroyEngine) is called, the user cannot use its method and event notices will not be triggered.
- To use the communication function again, [createEngine](#ThunderEngine.createEngine) must be called again to create a ThunderEngine instance.

> **Note:**
>
> - The created file player object [ThunderAudioFilePlayer](#ThunderAudioFilePlayer) will also be released.

--------------------------

#### ThunderEngine.getVersion

```java
public static String getVersion()
```

Get SDK version information.

##### Return[](#getVersion)

- SDK version information

--------------------------

#### ThunderEngine.setLogFilePath

```java
public static int setLogFilePath(String filePath)
```

Set path of log files (open log and save its information).

##### Description[](#setLogFilePath)

- One of the methods for outputting SDK logs. Specify the output directory and ensure its writability, and SDK outputs logs to this directory in logcat under debug.

> **Note:**
>
> - Ensure that the specified directory has write permission.

##### Parameter[](#setLogFilePath)

| Parameter | Description |
| :--- | :--- |
| filePath | Path for saving logs |

##### Return[](#setLogFilePath)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLogCallback

```java
public static int setLogCallback(IThunderLogCallback callback)
```

Set log callback.

##### Description[](#setLogCallback)

- One of methods for outputting SDK logs. The SDK calls back log messages to application for writing.
- After the log callback is set, the setLogFilePath will be invalid.

##### Parameter[](#setLogCallback)

| Parameter | Description |
| :--- | :--- |
| callback | For the callback interface instances, refer to [IThunderLogCallback](.mdnotification.md#IThunderLogCallback) interface for detail |

##### Return[](#setLogCallback)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLogLevel

```java
public static int setLogLevel(int filter)
```

Set log level.

##### Description[](#setLogLevel)

- Set filtering level for log output, and call it before setLogFilePath or setLogCallback. If this interface is not called, the default log level THUNDER_LOG_LEVEL_INFO will be used.

##### Parameter[](#setLogLevel)

| Parameter | Description |
| :--- | :--- |
| filter | Use the attributes of constants [ThunderRtcConstant.ThunderLogLevel](#ThunderRtcConstant.ThunderLogLevel) to set log level |

##### Return[](#setLogLevel)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setSceneId

```java
public void setSceneId(long sceneId)
```

Set scenario Id.

##### Parameter[](#setSceneId)

| Parameter | Description |
| :--- | :--- |
| sceneId | The scene Id customized by the developer can subdivide business scenes; If unnecessary, fill 0 |

--------------------------

#### ThunderEngine.setMediaMode

```java
public int setMediaMode(int mode)
```

Set media mode.

##### Description[](#setMediaMode)

- Media mode includes pure audio and audio/video.
- By default, SDK uses audio/video mode [ThunderRtcConstant.ThunderRtcProfile.THUNDER_PROFILE_DEFAULT](#ThunderRtcConstant.ThunderRtcProfile).
- [ThunderRtcConstant.ThunderRtcProfile.THUNDER_PROFILE_DEFAULT](#ThunderRtcConstant.ThunderRtcProfile) is equal to [ThunderRtcConstant.ThunderRtcProfile.THUNDER_PROFILE_NORMAL](#ThunderRtcConstant.ThunderRtcProfile) .

> **Note:**
>
> - Call it before joining room ([joinRoom](#ThunderEngine.joinRoom)).
> - It can only be reset when [destroyEngine](#ThunderEngine.destroyEngine) is performed.

##### Parameter[](#setMediaMode)

| Parameter | Description |
| :--- | :--- |
| mode | Media mode. For the optional value, refer to class attributes of [ThunderRtcConstant.ThunderRtcProfile](#ThunderRtcConstant.ThunderRtcProfile) for details |

##### Return[](#setMediaMode)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRoomMode

```java
public int setRoomMode(int mode)
```

Set room mode.

##### Description[](#setRoomMode)

- By default, SDK uses live mode [ThunderRtcConstant.RoomConfig.THUNDER_ROOMCONFIG_LIVE](#ThunderRtcConstant.RoomConfig)。
- It can be used before and after joining room.
- SDK can use different optimization methods by knowing usage scenes of applications (such as communication mode or live mode).

> **Note:**
>
> - It can only be reset when [destroyEngine](#ThunderEngine.destroyEngine) is performed.
> - The optional value of parameters can only be [ThunderRtcConstant.RoomConfig](#ThunderRtcConstant.RoomConfig) options listed in the document.

##### Parameter[](#setRoomMode)

| Parameter | Description |
| :--- | :--- |
| mode | Room mode. For the optional value, refer to class attributes of [ThunderRtcConstant.RoomConfig](#ThunderRtcConstant.RoomConfig) for details |

##### Return[](#setRoomMode)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setArea

```java
public int setArea(int area)
```

Set country and area of users.

To accommodate to different laws and regulations at home and abroad, AIVACOM NETWORK provides both domestic (by default) and international central systems. Set it by referring to the following points:

- If applications are mainly conducted abroad, this interface shall be called to set abroad area.
- The users in domestic and international central systems cannot communicate with each other. So make ensure that users in the same room shall be in the same system.
- The two systems are deployed globally, supporting global access.

> **Note:**
>
> - Only call it before the [joinRoom](#ThunderEngine.joinRoom) can be valid. It is necessary for abroad users but not for domestic users.
> - The optional value of parameters can only be [ThunderRtcConstant.RoomConfig](#ThunderRtcConstant.RoomConfig) options listed in the document.
> - It can only be reset when [destroyEngine](#ThunderEngine.destroyEngine) is performed.

##### Parameter[](#setArea)

| Parameter | Description |
| :--- | :--- |
| area | User’s area. For the optional value, refer to class attributes of [ThunderRtcConstant.AreaType](#ThunderRtcConstant.AreaType) for details |

##### Return[](#setArea)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.joinRoom

```java
public int joinRoom(byte[] token, String roomName, String uid)
```

Join a room.

- This method lets users join the (audio/video) communication room. In the same room, users can communicate with each other, and group chat starts when multiple users join it.
- If during the call, users have to call [leaveRoom](#ThunderEngine.leaveRoom) to leave before joining the next one.

> **Note:**
>
> - The applications cannot communicate with each other when using different appId.
> - Successful function return only indicates that the request is executed successfully. After receiving the callback on [ThunderEventHandler.onJoinRoomSuccess](.mdnotification.md#ThunderEventHandler.onJoinRoomSuccess) , it can indicate the success of joining room.

##### Parameter[](#joinRoom)

| Name | Description |
| :--- | :--- |
| token | For the requirements of authentication, see [Authentication Access Manual](#TODO:) for details |
| roomName | Room name (unique for each AppId) only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| uid | User ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |

##### Return[](#joinRoom)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.leaveRoom

```java
public int leaveRoom()
```

Leaving room indicates hang off or exiting conversation.

> **Note:**
>
> - When [joinRoom](#ThunderEngine.joinRoom) is called, you have to call [leaveRoom](#ThunderEngine.leaveRoom) to end conversation before starting the next one.
> - No matter whether the user is idle or in a call, [leaveRoom](#ThunderEngine.leaveRoom) can be called, without adverse effects. This method can release all resources related to conversation.

##### Return[](#leaveRoom)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.updateToken

```java
public int updateToken(byte[] token)
```

Update token.

Token is used for business authentication. The format is suggested as follows. See [Authentication Access Manual](#TODO:) for detail

| uint16 | uint32 | uint64 | uint64 | uint32 | uint16 | nBytes | 20 Bytes |
| -------- | ------ | ------ | ------------- | ------------ | ------------- | -------------- | ---------------- |
| TokenLen | AppId | uid | TimeStamp(ms) | ValidTime(s) | BizExtInfoLen | BizExtInfoData | DigitalSignature |

Refer to the following descriptions:

- The multi-byte integer uses network byte order, generally Big Endian.
- TokenLen: the length of the whole token includes its 2 bytes and abstract.
- Token expiration time=Timestamp+ValidTime*1000, the UTC time in millisecond since 1970.
- BizExtInfoData: The extension information of service authentication shall be customized by the developer.
- DigitalSignature: The digital signature adopts hmac-sha1 algorithm to obtain [TokenLen,BizExtInfoData] by calculating all data before DigitalSignature. The private key uses assigned appSecret when applying for appId.
- Token has to be transmitted by http, so the whole Token shall be encoded by url base64. Note that the url encode is not performed for the whole base64.

##### Parameter[](#updateToken)

| Parameter | Description |
| :--- | :--- |
| token | For requirements of authentication, refer to "[User Authentication Description](#TODO:)" for detail |

##### Return[](#updateToken)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setAudioConfig

```java
public int setAudioConfig(int profile, int commutMode, int scenarioMode)
```

It is used to set audio parameter and application scene.

> **Note:**
>
> - Call it before playing audio [stopLocalAudioStream](#ThunderEngine.stopLocalAudioStream) .

##### Parameter[](#setAudioConfig)

| Parameter | Description |
| :--- | :--- |
| profile | Audio type. For the optional value, refer to class attributes of [ThunderRtcConstant.AudioConfig](#ThunderRtcConstant.AudioConfig) for details |
| commuMode | Interactive mode. For the optional value, refer to class attributes of [ThunderRtcConstant.CommutMode](#ThunderRtcConstant.CommutMode) for details |
| scenarioMode | Scenario mode. For the optional value, refer to class attributes of [ThunderRtcConstant.ScenarioMode](#ThunderRtcConstant.ScenarioMode) for details |

##### Return[](#setAudioConfig)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableVoicePosition

```java
public int enableVoicePosition(boolean enable)
```

Enable/Disable voice stereo of remote users.

> **Note:**
>
> - Call this method before [joinRoom](#ThunderEngine.joinRoom)

##### Parameter[](#enableVoicePosition)

| Parameter | Description |
| :--- | :--- |
| enable | true: enable voice stereo of remote users <br>false: disable voice stereo of remote users |

##### Return[](#enableVoicePosition)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRemoteUidVoicePosition

```java
public int setRemoteUidVoicePosition(String uid, int azimuth, int gain)
```

Set spatial location and volume of remote user's voice.

##### Parameter[](#setRemoteUidVoicePosition)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| azimuth | Set the position where the remote user’s voice appears, with value range of [-90,90].<br> 0: voice appears in the right ahead. (default)<br> -90: voice appears in the left side.<br> 90: voice appears in the right side. |
| gain | Set the voice volume of remote user, with value range of [0,100]. The default value is 100.0, indicating user’s original volume. The smaller the value, the lower the volume |

##### Return[](#setRemoteUidVoicePosition)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableLoudspeaker

```java
public int enableLoudspeaker(boolean enabled)
```

Enable/Disable loudspeaker.

- This method forces the voice routing to loudspeaker.

##### Parameter[](#enableLoudspeaker)

| Parameter | Description |
| :--- | :--- |
| enabled | true: play by loudspeaker<br>false: play by receiver |

##### Return[](#enableLoudspeaker)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.isLoudspeakerEnabled

```java
public boolean isLoudspeakerEnabled()
```

Query the enabled status of loudspeaker.

##### Return[](#isLoudspeakerEnabled)

- true: play by loudspeaker
- false: play not by loudspeaker

--------------------------

#### ThunderEngine.setLoudSpeakerVolume

```java
public int setLoudSpeakerVolume(int volume)
```

Set loudspeaker volume.

##### Parameter[](#setLoudSpeakerVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Volume value [0-400] |

##### Return[](#setLoudSpeakerVolume)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setAudioVolumeIndication

```java
public int setAudioVolumeIndication(int interval,
                                        int moreThanThd,
                                        int lessThanThd,
                                        int smooth)
```

Enable volume indication for speaker.

- By using this method, SDK can feed current speaker and speaker’s volume back to an application periodically. Report by callback interface [ThunderEventHandler.onPlayVolumeIndication](.mdnotification.md#ThunderEventHandler.onPlayVolumeIndication) .

> **Note:**
>
> - It can only be reset when destroyEngine is performed.
> - The voice volume collected by local microphone or playing file is not included.

##### Parameter[](#setAudioVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| interval | The callback interval (unit: millisecond) is <br><=0: The volume indication is disabled,<br> >0: Use this numerical value as volume indication of interval enabling. The interval of more than 200 milliseconds is recommended, which is 0 by default. |
| moreThanThd | From >= moreThanThd to < moreThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| lessThanThd | From >= lessThanThd to < lessThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| smooth | Invalid momentarily. Fill 0 |

##### Return[](#setAudioVolumeIndication)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableCaptureVolumeIndication

```java
public int enableCaptureVolumeIndication(int interval,
                                             int moreThanThd,
                                             int lessThanThd,
                                             int smooth)
```

Enable/Disable collected volume callback.

- By using this method, SDK can feed current microphone capture volume back to an application periodically. Report it by [ThunderEventHandler.onCaptureVolumeIndication](.mdnotification.md#ThunderEventHandler.onCaptureVolumeIndication).

##### Parameter[](#enableCaptureVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| interval | The callback interval (unit: millisecond) is <br><=0: The volume indication is disabled, <br>> 0: Use this numerical value as capture volume indication of interval enabling, which is 0 by default |
| moreThanThd | From >= moreThanThd to < moreThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| lessThanThd | From >= lessThanThd to < lessThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| smooth | Invalid momentarily. Fill 0 |

##### Return[](#enableCaptureVolumeIndication)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.startAudioSaver

```java
public boolean startAudioSaver(String fileName, int saverMode, int fileMode)
```

Start saving audio data as aac format file.

##### Parameter[](#startAudioSaver)

| Parameter | Description |
| :--- | :--- |
| fileName | The save path of file must be full path including file name with postfix of .aac. The directory for saving file must be created in advance, and the folder cannot be created by this interface. For example: /sdcard/helloworld.aac |
| saverMode | Audio saving mode. For the optional value, refer to class attributes of [ThunderRtcConstant.ScenarioMode](#ThunderRtcConstant.AudioSaverMode) for details |
| fileMode | Audio writing mode. For the optional value, refer to class attributes of [ThunderRtcConstant.AudioSaverWfMode](#ThunderRtcConstant.AudioSaverWfMode) for details |

##### Return[](#startAudioSaver)

- true: Success.
- false: Method call failed

--------------------------

#### ThunderEngine.stopAudioSaver

```java
public boolean stopAudioSaver()
```

Stop saving audio data as aac format file.

##### Return[](#stopAudioSaver)

- true: Success.
- false: Method call failed

--------------------------

#### ThunderEngine.setSoundEffect

```java
public void setSoundEffect(int mode)
```

Set sound effect mode.

##### Parameter[](#setSoundEffect)

| Parameter | Description |
| :--- | :--- |
| mode | sound effect mode. For the optional value, refer to class attributes of [ThunderRtcConstant.SoundEffectMode](#ThunderRtcConstant.SoundEffectMode) for details |

--------------------------

#### ThunderEngine.setVoiceChanger

```java
public void setVoiceChanger(int mode)
```

Set voice change mode.

##### Parameter[](#setVoiceChanger)

| Parameter | Description |
| :--- | :--- |
| mode | Voice change mode. For the optional value, refer to class attributes of [ThunderRtcConstant.VoiceChangerMode](#ThunderRtcConstant.VoiceChangerMode) for details |

--------------------------

#### ThunderEngine.stopLocalAudioStream

```java
public int stopLocalAudioStream(boolean stop)
```

Enable/Disable the capture, encode and upstream of local audio.

> **Note:**
>
> - Call this method after calling [joinRoom](#ThunderEngine.joinRoom) successfully.

##### Parameter[](#stopLocalAudioStream)

| Parameter | Description |
| :--- | :--- |
| stop | true: disable the capture, encode and upstream of local audio<br>false: enable the capture, encode and upstream of local audio |

##### Return[](#stopLocalAudioStream)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopRemoteAudioStream

```java
public int stopRemoteAudioStream(String uid, boolean stop)
```

Stop/Resume receiving audio stream of a specified user.

> **Note:**
>
> - Subscription configuration is only reset when [destroyEngine](#ThunderEngine.destroyEngine) is performed
> - After stopping receiving the specified audio stream, you can receive all audio streams through [stopAllRemoteAudioStreams](#ThunderEngine.stopAllRemoteAudioStreams) and vice versa.
> - This interface has no priority relationship with [stopAllRemoteAudioStreams](#ThunderEngine.stopAllRemoteAudioStreams), and the interface called later will be valid.

##### Parameter[](#stopRemoteAudioStream)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote users |
| Stop | True: stop receiving audio stream of specified remote user<br>false: start receiving audio stream of specified remote user |

##### Return[](#stopRemoteAudioStream)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopAllRemoteAudioStreams

```java
public int stopAllRemoteAudioStreams(boolean stop)
```

Stop/Resume receiving all remote audio streams. Process this interface based on the following rules:

- By default, SDK receives all audio stream data.
- After the setting of receiving all (stop=false), all audio streams in the room will be subscribed automatically. You can specify one stream of not being subscribed by [stopRemoteAudioStream](#ThunderEngine.stopRemoteAudioStream).
- After the setting of receiving nothing (stop=true), all audio stream in the room will not be subscribed. You can specify one stream being subscribed by [stopRemoteAudioStream](#ThunderEngine.stopRemoteAudioStream).

> **Note:**
>
> - Subscription configuration is only reset when [destroyEngine](#ThunderEngine.destroyEngine) is performed.
> - This interface has no priority relationship with [stopRemoteAudioStream](#ThunderEngine.stopRemoteAudioStream) , and which interface called later will be valid.

##### Parameter[](#stopAllRemoteAudioStreams)

| Parameter | Description |
| :--- | :--- |
| stop | true: stop receiving all remote audios<br>false: resume receiving all remote audios |

##### Return[](#stopAllRemoteAudioStreams)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setMicVolume

```java
public int setMicVolume(int volume)
```

Set microphone volume.

##### Parameter[](#setMicVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Volume value [0-400] |

##### Return[](#setMicVolume)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRemoteAudioStreamsVolume

```java
public int setRemoteAudioStreamsVolume(String uid, int volume)
```

Set the volume of the remote audio stream.

##### Parameter[](#setRemoteAudioStreamsVolume)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| volume | Volume value [0-400] |

##### Return[](#setRemoteAudioStreamsVolume)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.createAudioFilePlayer

```java
public ThunderAudioFilePlayer createAudioFilePlayer()
```

Create instance object of audio file player.

##### Return[](#createAudioFilePlayer)

- [ThunderAudioFilePlayer](#ThunderAudioFilePlayer) : instance object of audio file player

--------------------------

#### ThunderEngine.destroyAudioFilePlayer

```java
public void destroyAudioFilePlayer(ThunderAudioFilePlayer audioFilePlayer)
```

Destroy instance object of audio file player.

##### Parameter[](#destroyAudioFilePlayer)

| Parameter | Description |
| :--- | :--- |
| audioFilePlayer | Instance object of audio file player [ThunderAudioFilePlayer](#ThunderAudioFilePlayer) ) |

--------------------------

#### ThunderEngine.setEnableEqualizer

```java
public int setEnableEqualizer(boolean enabled)
```

Enable/Disable local voice equalizer.

##### Parameter[](#setEnableEqualizer)

| Parameter | Description |
| :--- | :--- |
| enabled | true: Enable<br>false: Disable |

##### Return[](#setEnableEqualizer)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setEqGains

```java
public int setEqGains(final int[] gains)
```

Set voice equalizer parameters.

##### Parameter[](#setEqGains)

| Parameter | Description |
| :--- | :--- |
| gains | The value range of each element: -12 <= gains[i] <= 12, in which the value range of i: -12 <= gains[i] <= 12 |

##### Return[](#setEqGains)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setEnableReverb

```java
public int setEnableReverb(boolean enabled)
```

Enable/Disable local voice reverberation.

##### Parameter[](#setEnableReverb)

| Parameter | Description |
| :--- | :--- |
| enabled | true: Enable<br>false: Disable |

##### Return[](#setEnableReverb)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setReverbExParameter

```java
public int setReverbExParameter(ThunderRtcConstant.ReverbExParameter param)
```

Set local voice reverberation parameters

##### Parameter[](#setReverbExParameter)

| Parameter | Description |
| :--- | :--- |
| param | The parameters of voice reverberation, refer to [ThunderRtcConstant.ReverbExParameter](#ThunderRtcConstant.ReverbExParameter) for details |

##### Return[](#setReverbExParameter)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setEnableCompressor

```java
public int setEnableCompressor(boolean enabled)
```

Enable/Disable audio compressor.

##### Parameter[](#setEnableCompressor)

| Parameter | Description |
| :--- | :--- |
| enabled | true: Enable<br>false: disable |

##### Return[](#setEnableCompressor)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setCompressorParam

```java
public int setCompressorParam(ThunderRtcConstant.CompressorParam param)
```

Set audio compressor parameters.

##### Parameter[](#setCompressorParam)

| Parameter | Description |
| :--- | :--- |
| param | The parameters of audio compressor, refer to [ThunderRtcConstant.CompressorParam](#ThunderRtcConstant.CompressorParam) for details |

##### Return[](#setCompressorParam)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setEnableLimiter

```java
public int setEnableLimiter(boolean enabled)
```

Enable/Disable limiter.

##### Parameter[](#setEnableLimiter)

| Parameter | Description |
| :--- | :--- |
| enabled | true: Enable<br>false: Disable |

##### Return[](#setEnableLimiter)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLimiterParam

```java
public int setLimiterParam(ThunderRtcConstant.LimterParam param)
```

Set limiter parameters.

##### Parameter[](#setLimiterParam)

| Parameter | Description |
| :--- | :--- |
| param | The parameters of limiter, refer to [ThunderRtcConstant.LimterParam](#ThunderRtcConstant.LimterParam) for details |

##### Return[](#setLimiterParam)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableAudioPlaySpectrum

```java
public void enableAudioPlaySpectrum(boolean enable)
```

Enable/Disable data callback on audio play spectrum.

The [ThunderEventHandler.onAudioPlaySpectrumData](.mdnotification.md#ThunderEventHandler.onAudioPlaySpectrumData) function will be called back after it is enabled.

##### Parameter[](#enableAudioPlaySpectrum)

| Parameter | Description |
| :--- | :--- |
| enable | true: Enable<br>false: Disable (default) |

--------------------------

#### ThunderEngine.setAudioPlaySpectrumInfo

```java
public void setAudioPlaySpectrumInfo(int spectrumLen, int notifyIntervalMS)
```

Set callback information of audio play spectrum data.

##### Parameter[](#setAudioPlaySpectrumInfo)

| Parameter | Description |
| :--- | :--- |
| spectrumLen | The length of spectrum is [12 - 256], and is 256 by default |
| notifyIntervalMS | The interval of spectrum callback must be the multiple of 10, and is 30MS by default |

--------------------------

#### ThunderEngine.sendUserAppMsgData

```java
public int sendUserAppMsgData(byte[] msgData)
```

Sending developer's custom broadcast messages in room.

This interface sends messages through media UDP channel with features of low-lantency and unreliability. Specified constraints are as follows:

- The sender must join the room.
- Call the interface after successfully uploading audio and video (messages cannot be sent if only a viewer or authentication fails).
- The frequency of calling this interface shall not be more than 2 times per second, and the msgData size is not more than 200 bytes.
- msg will be dropped if any of the conditions above is not met.
- The messages cannot be guaranteed to be delivered to all online users in room, and cannot be guaranteed be delivered in order.

Get the reason for failed sending of msg through [ThunderEventHandler.onSendAppMsgDataFailedStatus](.mdnotification.md#ThunderEventHandler.onSendAppMsgDataFailedStatus) interface function.
Get the custom broadcast messages from other users through [ThunderEventHandler.onRecvUserAppMsgData](.mdnotification.md#ThunderEventHandler.onRecvUserAppMsgData) interface function.

##### Parameter[](#sendUserAppMsgData)

| Parameter | Description |
| :--- | :--- |
| msgData | Message sent |

##### Return[](#sendUserAppMsgData)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.sendMediaExtraInfo

```java
public int sendMediaExtraInfo(java.nio.ByteBuffer data, int dataLen)
```

Send media extra information.
Use video channel when uploading video, otherwise use audio channel.

Specified constraints are as follows:

- The sender must join the room, and call it after successfully publishing audio.
- The fastest call frequency is 100 ms one time in audio publishing (publishing in a pure audio mode or only audio publishing in an audio/video mode); the size of media extra information cannot exceed 200 bytes.
- In audio/video mode, the call frequency of video publishing cannot exceed the frame rate, and the extra information shall be no more than 2048 bytes. For example, the default frame rate of 15fps is adopted for stream publishing, indicating that the call frequency cannot exceed 1000/15=66.7 ms each time
- Packet loss may occur

Get the reason for failed sending of media extra information through [IThunderMediaExtraInfoCallback.onSendMediaExtraInfoFailedStatus](.mdnotification.md#IThunderMediaExtraInfoCallback.onSendMediaExtraInfoFailedStatus).
Receive the media extra information from other users through [IThunderMediaExtraInfoCallback.onRecvMediaExtraInfo](.mdnotification.md#IThunderMediaExtraInfoCallback.onRecvMediaExtraInfo) interface function.

##### Parameter[](#sendMediaExtraInfo)

| Parameter | Description |
| :--- | :--- |
| Date | The media extra information data to be transmitted which must be created using ByteBuffer.allocateDirect(int) |
| dataLen | The length of media extra information data.<br>If there is only audio publishing (publishing in a pure audio mode or only audio publishing in an audio/video mode), the size of extra information shall be no more than 200 bytes.<br>If there is video publishing in audio/video mode, the extra information shall be no more than 2048 bytes |

##### Return[](#sendMediaExtraInfo)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setMediaExtraInfoCallback

```java
public int setMediaExtraInfoCallback(IThunderMediaExtraInfoCallback callback)
```

Set callback monitoring of media extra information.

##### Parameter[](#setMediaExtraInfoCallback)

| Parameter | Description |
| :--- | :--- |
| callback | The callback instance object of media extra information, refer to [IThunderMediaExtraInfoCallback](.mdnotification.md#IThunderMediaExtraInfoCallback) for details |

##### Return[](#setMediaExtraInfoCallback)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableMixVideoExtraInfo

```java
public int enableMixVideoExtraInfo(boolean enable)
```

Enable mixed video carry media extra information, for example, mixed video carry layout information.
After it is enabled, the callback on [IThunderMediaExtraInfoCallback.onRecvMixVideoInfo](.mdnotification.md#IThunderMediaExtraInfoCallback.onRecvMixVideoInfo) can be received when this mixed video stream is played in audience terminal.

##### Parameter[](#enableMixVideoExtraInfo)

| Parameter | Description |
| :--- | :--- |
| enable | true: Enable<br>false: Disable (default) |

##### Return[](#enableMixVideoExtraInfo)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableAudioDataIndication

```java
public void enableAudioDataIndication(boolean enablePlay)
```

Enable/Disable reporting Audio playback Data.
Get audio playback data through the [ThunderEventHandler.onAudioPlayData](.mdnotification.md#ThunderEventHandler.onAudioPlayData) interface function

##### 参数[](#enableAudioDataIndication)

| Parameter | Description |
| :--- | :--- |
| enablePlay | true: Enable<br>false: Disable (default) |

--------------------------

#### ThunderEngine.setAudioSourceType

```java
public void setAudioSourceType(int sourceType)
```

Set the audio source type.

##### Parameter[](#setAudioSourceType)

| Parameter | Description |
| :--- | :--- |
| sourceType | Audio source type. For the optional value, refer to class attributes of [ThunderRtcConstant.SourceType](#ThunderRtcConstant.SourceType) for details |

--------------------------

#### ThunderEngine.setEnableInEarMonitor

```java
public int setEnableInEarMonitor(boolean enable)
```

Enable/Disable in-ear monitor.

##### Parameter[](#setEnableInEarMonitor)

| Parameter | Description |
| :--- | :--- |
| enabled | true: enable <br>false: disable (default) |

##### Return[](#setEnableInEarMonitor)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setVideoEncoderConfig

```java
public int setVideoEncoderConfig(ThunderVideoEncoderConfiguration yyVideoConfig)
```

Set video encoding configuration.

- SDK will get specified parameters for encoding video from configuration server based on config. If the developer has special parameter requirements for encoding video, contact technical support for personalized configuration.
- If the video has been published, update the video encoding parameters. The updated video effect can be seen from local review and remote subscription.

##### Parameter[](#setVideoEncoderConfig)

| Parameter | Description |
| :--- | :--- |
| yyVideoConfig | For the video encoding configuration, refer to  [ThunderVideoEncoderConfiguration](#ThunderVideoEncoderConfiguration) for details |

##### Return[](#setVideoEncoderConfig)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLocalVideoCanvas

```java
public int setLocalVideoCanvas(ThunderVideoCanvas local)
```

Set local view.
If this view is not set, the preview and publishing can also be enabled. The local collected picture can seen after setting this view.

##### Parameter[](#setLocalVideoCanvas)

| Parameter | Description |
| :--- | :--- |
| local | The video rendering canvas instance, refer to [ThunderVideoCanvas](#ThunderVideoCanvas) for details |

##### Return[](#setLocalVideoCanvas)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRemotePlayType

```java
public int setRemotePlayType(int remotePlayType)
```

Set the playing type of remote video. The default is the common audience view.

> **Note:**
>
> - Call it before joining room.

##### Parameter[](#setRemotePlayType)

| Parameter | Description |
| :--- | :--- |
| remotePlayType | Playing type of remote video. For the optional value, refer to [ThunderRtcConstant.ThunderRtcRemotePlayType](#ThunderRtcConstant.ThunderRtcRemotePlayType) |

##### Return[](#setRemotePlayType)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setMultiVideoViewLayout

```java
public int setMultiVideoViewLayout(ThunderMultiVideoViewParam params)
```

Set the layout parameters of the multi videos on the view

This function is mostly used for scenario of multiplayer interaction.
Under this situation, the multi-channel video streams shall be displayed in the same view to reduce performance consumption.
This function is called to set the locations where the multi-channel video streams are placed respectively.

Support setting background image and its display location.

##### Parameter[](#setMultiVideoViewLayout)

| Parameter | Description |
| :--- | :--- |
| params | The layout parameters of multiplayer interaction video in rendering view, refer to [ThunderMultiVideoViewParam](#ThunderMultiVideoViewParam) for details |

##### Return[](#setMultiVideoViewLayout)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRemoteVideoCanvas

```java
public int setRemoteVideoCanvas(ThunderVideoCanvas remote)
```

Set the rendering canvas of remote video.

##### Parameter[](#setRemoteVideoCanvas)

| Parameter | Description |
| :--- | :--- |
| remote | The display view instance, refer to [ThunderVideoCanvas](#ThunderVideoCanvas) for details |

##### Return[](#setRemoteVideoCanvas)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLocalCanvasScaleMode

```java
public int setLocalCanvasScaleMode(int mode)
```

Set the scale mode of the local video stream on the canvas.

##### Parameter[](#setLocalCanvasScaleMode)

| Parameter | Description |
| :--- | :--- |
| mode | Local view scale mode. For the optional value, refer to [ThunderRtcConstant.ThunderVideoRenderMode](#ThunderRtcConstant.ThunderVideoRenderMode) |

##### Return[](#setLocalCanvasScaleMode)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRemoteCanvasScaleMode

```java
public int setRemoteCanvasScaleMode(String uid, int mode)
```

Set the scale mode of the remote video stream on the canvas.

##### Parameter[](#setRemoteCanvasScaleMode)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| mode | Remote specified view scale mode. For the optional value, refer to [ThunderRtcConstant.ThunderVideoRenderMode](#ThunderRtcConstant.ThunderVideoRenderMode) |

##### Return[](#setRemoteCanvasScaleMode)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.startVideoPreview

```java
public int startVideoPreview()
```

Start video preview of local camera.

##### Return[](#startVideoPreview)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopVideoPreview

```java
public int stopVideoPreview()
```

Stop video preview of local camera.

##### Return[](#stopVideoPreview)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableLocalVideoCapture

```java
public int enableLocalVideoCapture(boolean enable)
```

Enable/Disable local video capture.

##### Parameter[](#enableLocalVideoCapture)

| Parameter | Description |
| :--- | :--- |
| enabled | true: enable local video capture<br>false: disable local video capture (default) |

##### Return[](#enableLocalVideoCapture)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopLocalVideoStream

```java
public int stopLocalVideoStream(boolean stop)
```

Disable/Enable local video sending.

##### Parameter[](#stopLocalVideoStream)

| Parameter | Description |
| :--- | :--- |
| Stop | true: stop sending local video (default)<br>false: start sending local video |

##### Return[](#stopLocalVideoStream)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopRemoteVideoStream

```java
public int stopRemoteVideoStream(String uid, boolean stop)
```

 Stop/Resume receiving video stream of a specified user.

- After stopping receiving specified video stream, you can receive all video streams through [stopAllRemoteVideoStreams](#ThunderEngine.stopAllRemoteVideoStreams), vice versa.
- This interface has no priority relationship with [stopAllRemoteVideoStreams](#ThunderEngine.stopAllRemoteVideoStreams), and the interface called later will be valid.

##### Parameter[](#stopRemoteVideoStream)

| Parameter | Description |
| :--- | :--- |
| uid | uid of remote user |
| Stop | true: stop receiving specified video stream<br>false: receive specified video stream |

##### Return[](#stopRemoteVideoStream)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.stopAllRemoteVideoStreams

```java
public int stopAllRemoteVideoStreams(boolean stop)
```

Stop/Receive all remote videos

- After the setting of receiving all (stop=false), all video streams in the room will be subscribed automatically. You can specify one stream of not being subscribed by[stopRemoteVideoStream](#ThunderEngine.stopRemoteVideoStream).
- After the setting of receiving nothing (stop=true), all video streams in the room will not be subscribed. You can specify one stream being subscribed by [stopRemoteVideoStream](#ThunderEngine.stopRemoteVideoStream).
- This interface has no priority relationship with [stopRemoteVideoStream](#ThunderEngine.stopRemoteVideoStream), and the interface called later will be valid.

##### Parameter[](#stopAllRemoteVideoStreams)

| Parameter | Description |
| :--- | :--- |
| Stop | true: stop receiving all video streams <br>false: resume receiving all video streams (clear all configuration records of [stopRemoteVideoStream](#ThunderEngine.stopRemoteVideoStream) at the same time) |

##### Return[](#stopAllRemoteVideoStreams)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.registerVideoCaptureTextureObserver

```java
public int registerVideoCaptureTextureObserver(IGPUProcess observer)
```

Register observer object for capturing video texture data, which is used for beautification etc.

##### Parameter[](#registerVideoCaptureTextureObserver)

| Parameter | Description |
| :--- | :--- |
| observer | The observer object instance for collecting video texture data can obtain and process rendering texture data of video’s each frame. See [IGPUProcess](.mdnotification.md#IGPUProcess) for details.<br>If the null is transmitted, cancel registration. |

##### Return[](#registerVideoCaptureTextureObserver)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.registerVideoCaptureFrameObserver

```java
public int registerVideoCaptureFrameObserver(IVideoCaptureObserver observer)
```

Register observer object for collecting data of camera.

##### Parameter[](#registerVideoCaptureFrameObserver)

| Parameter | Description |
| :--- | :--- |
| observer | The observer object instance for collecting data of camera can obtain and render collected data of video camera yuv. See [IVideoCaptureObserver](.mdnotification.md#IVideoCaptureObserver) for details.<br>If the null is transmitted, cancel registration. |

##### Return[](#registerVideoCaptureFrameObserver)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.registerVideoDecodeFrameObserver

```java
public int registerVideoDecodeFrameObserver(String uid, IVideoDecodeObserver observer)
```

Register the decoded YUV (I420) video data observer object for the specified user.

##### Parameter[](#registerVideoDecodeFrameObserver)

| Parameter | Description |
| :--- | :--- |
| uid | uid needing to be monitored. |
| observer | The decoded observer object for video data can obtain and process decoded video data. See [IVideoDecodeObserver](.mdnotification.md#IVideoDecodeObserver) for details.<br>If the null is transmitted, cancel registration. |

##### Return[](#registerVideoDecodeFrameObserver)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.registerAudioFrameObserver

```java
public int registerAudioFrameObserver(IAudioFrameObserver observer)
```

Register audio observer object.

##### Parameter[](#registerAudioFrameObserver)

| Parameter | Description |
| :--- | :--- |
| observer | The observer object for audio frame data can obtain and process audio frame data. See [IAudioFrameObserver](.mdnotification.md#IAudioFrameObserver) for details.<br>If the null is transmitted, cancel registration. |

##### Return[](#registerAudioFrameObserver)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setRecordingAudioFrameParameters

```java
public int setRecordingAudioFrameParameters(int sampleRate, int room, int mode, int samplesPerCall)
```

Set the format of captured audio data which will report.

##### Parameter[](#setRecordingAudioFrameParameters)

| Parameter | Description |
| :--- | :--- |
| sampleRate | Specify sampling rate of audio callback data, and it can be set as 8000, 16000, 32000, 44100 or 48000 |
| room | Set number of channels for audio callback data; 1: single track 2: dual track |
| mode | Specify operation mode of audio callback data. See [ThunderRtcConstant.ThunderAudioRawFrameOperationMode](#ThunderRtcConstant.ThunderAudioRawFrameOperationMode) for details |
| samplesPerCall | Specify number of samples for audio callback data. For example, the RTMP in push flow is always 1024. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setRecordingAudioFrameParameters)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setPlaybackAudioFrameParameters

```java
public int setPlaybackAudioFrameParameters(int sampleRate, int room, int mode, int samplesPerCall)
```

Set the format of playing audio data which will report.

##### Parameter[](#setPlaybackAudioFrameParameters)

| Parameter | Description |
| :--- | :--- |
| sampleRate | Specify sampling rate of audio callback data, and it can be set as 8000, 16000, 32000, 44100 or 48000 |
| room | Set number of channels for audio callback data; 1: single track 2: dual track |
| mode | Specify operation mode of audio callback data. See [ThunderRtcConstant.ThunderAudioRawFrameOperationMode](#ThunderRtcConstant.ThunderAudioRawFrameOperationMode) for details |
| samplesPerCall | Specify number of samples for audio callback data. For example, the RTMP in push flow is always 1024. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setPlaybackAudioFrameParameters)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setVideoWatermark

```java
public int setVideoWatermark(ThunderBoltImage watermark)
```

Set watermark of local video.

- This interface adopts a picture in PNG format as a watermark in local video and releases with it.
- If the size of picture in PNG format is inconsistent with settings in this method, SDK will make it coincident by clipping.
- Only one watermark can be added into the live video, and the watermark added later will replace the last one.
- The watermark will rotate with the rotation of screen.

##### Parameter[](#setVideoWatermark)

| Parameter | Description |
| :--- | :--- |
| watermark | The watermark pictures to be added into local live video, refer to [ThunderBoltImage](#ThunderBoltImage) for details. The settings of null indicates canceling watermark |

##### Return[](#setVideoWatermark)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setCustomAudioSource

```java
public int setCustomAudioSource(boolean enabled, int sampleRate, int channel)
```

Set parameters of external audio source.

- This interface shall be called before [pushCustomAudioFrame](#ThunderEngine.pushCustomAudioFrame).

##### Parameter[](#setCustomAudioSource)

| Parameter | Description |
| :--- | :--- |
| enabled | true: enable external audio capture <br>false: disable external audio capture (default) |
| sampleRate | The sampling rate of external audio source can be 8000, 16000, 32000, 44100 or 48000 |
| channel | Number of channels for external audio source (support two at most) |

##### Return[](#setCustomAudioSource)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.pushCustomAudioFrame

```java
public int pushCustomAudioFrame(byte[] data, long timeStamp)
```

Push external audio frame.

- Call this interface after [setCustomAudioSource](#ThunderEngine.setCustomAudioSource), and then, upload the external audio data

##### Parameter[](#pushCustomAudioFrame)

| Parameter | Description |
| :--- | :--- |
| Date | External PCM audio frame data |
| timeStamp | Timestamp of external audio frame is used to synchronize external video source |

##### Return[](#pushCustomAudioFrame)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setCustomVideoSource

```java
public int setCustomVideoSource(ThunderCustomVideoSource videoSource)
```

Set customized video source.

- The user needs to implement [ThunderCustomVideoSource](.mdnotification.md#ThunderCustomVideoSource) interface, monitor corresponding methods, and upload external video stream by using [ThunderVideoFrameConsumer.consumeByteArrayFrame](.mdnotification.md#ThunderVideoFrameConsumer.consumeByteArrayFrame) in onInitialize function.

##### Parameter[](#setCustomVideoSource)

| Parameter | Description |
| :--- | :--- |
| videoSource | Operation interface for external video source |

##### Return[](#setCustomVideoSource)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.addPublishOriginStreamUrl

```java
public int addPublishOriginStreamUrl(String url)
```

Add a publishing address of source stream.

- After this interface is called, the anchor's current audio/video stream will be pushed to the specified CDN address. To update url, first call the [removePublishOriginStreamUrl](#ThunderEngine.removePublishOriginStreamUrl), and add after removing the original address.
- Only one-channel stream publishing address can be added each time by this method. If multi-channel streams need to be pushed, this method have to be called repeatedly. A maximum of 5 addresses are supported for stream publishing.
- The server will push the source stream to corresponding URL after publishing. It can be called after joining the room (joinroom), and the configuration will be cleared after leaving the room.

##### Parameter[](#addPublishOriginStreamUrl)

| Parameter | Description |
| :--- | :--- |
| url | Stream publishing address, with the format of RTMP.<br>The special characters such as Chinese cannot be supported, and the address length cannot be more than 512 bytes.<br>Note: some CDN manufacturers may not support 512 bytes, for example, the Aliyun only supports 256 bytes. |

##### Return[](#addPublishOriginStreamUrl)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.removePublishOriginStreamUrl

```java
public int removePublishOriginStreamUrl(String url)
```

Remove the publishing address of source stream.

- After this interface is called, the anchor's current audio/video stream will not be pushed to the specified CDN address.

##### Parameter[](#removePublishOriginStreamUrl)

| Parameter | Description |
| :--- | :--- |
| url | The address to stop pushing stream, the format is RTMP.<br>The special characters such as Chinese cannot be supported, and the address length cannot be more than 512 bytes.<br>Note: some CDN manufacturers may not support 512 bytes, for example, the Aliyun only supports 256 bytes. |

##### Return[](#removePublishOriginStreamUrl)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLiveTranscodingTask

```java
public int setLiveTranscodingTask(String taskId, LiveTranscoding transcoding)
```

Add or update transcoding task.

- After this interface is called, the server of AIVACOM will start stream mixing and transcoding tasks, and pull various set source streams to mix videos and audios. The application needs to specify task ID to differentiate different stream mixing and transcoding tasks.
- This interface can be called repeatedly to update stream mixing parameters in the mix process. Multiple stream mixing tasks can be set in the same room.
- This interface is called only after you join a room (joinRoom). The configuration will be cleaned after you leave the room.
- The stream publishing address can be added into the stream mixing and transcoding tasks by [addPublishTranscodingStreamUrl](#ThunderEngine.addPublishTranscodingStreamUrl) interface. The mixing and transcoding stream will be pushed to specified address after operating the stream mixing and transcoding.

##### Parameter[](#setLiveTranscodingTask)

| Parameter | Description |
| :--- | :--- |
| taskId | Task ID for stream mixing and transcoding tasks is generated and managed by the developer. It shall be unique in a room and supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| transcoding | The configuration information of stream mixing and transcoding, refer to [LiveTranscoding](#LiveTranscoding) for details |

##### Return[](#setLiveTranscodingTask)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.removeLiveTranscodingTask

```java
public int removeLiveTranscodingTask(String taskId)
```

Remove a transcoding task.

- After this interface is called, the server of AIVACOM will delete and stop the stream mixing task, but the url added by the addPublishTranscodingStreamUrl will not be remove.

##### Parameter[](#removeLiveTranscodingTask)

| Parameter | Description |
| :--- | :--- |
| taskId | Task ID for stream mixing and transcoding tasks is generated and managed by the developer. It shall be unique in a room and supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |

##### Return[](#removeLiveTranscodingTask)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.addPublishTranscodingStreamUrl

```java
public int addPublishTranscodingStreamUrl(String taskId, String url)
```

Add a publishing address of transcoding stream.

- Call this interface after adding transcoding task by calling [setLiveTranscodingTask](#ThunderEngine.setLiveTranscodingTask) interface.
- After this interface is called, the specified mixing stream will be pushed to the specified CDN address. To update url, first call the [removePublishTranscodingStreamUrl](#ThunderEngine.removePublishTranscodingStreamUrl) and add after removing the original address.
- Add stream publishing address for specified transcoding task, and only one address can added by this method. If multiple-channel streams have to be pushed, call this method repeatedly. 5 stream publishing addresses can be supported at most in the same transcoding task.
- This interface is called only after you join a room (joinRoom). The configuration will be cleaned after you leave the room.

##### Parameter[](#addPublishTranscodingStreamUrl)

| Parameter | Description |
| :--- | :--- |
| taskId | The transcoding task ID is generated and managed by users. It shall be unique globally, and only supports character set composed of a-zA-Z0-9 with length of no more than 20 characters. |
| url | Stream publishing address, with the format of RTMP.<br>The special characters such as Chinese cannot be supported, and the address length cannot be more than 512 bytes.<br>Note: some CDN manufacturers may not support 512 bytes, for example, the Aliyun only supports 256 bytes |

##### Return[](#addPublishTranscodingStreamUrl)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.removePublishTranscodingStreamUrl

```java
public int removePublishTranscodingStreamUrl(String taskId, String url)
```

Remove the publishing address of the transcoding stream.

- After this interface is called, the specified transcoding stream will not be pushed to the specified CDN address.
- Only one-channel stream publishing address can be deleted each time by this method. If multi-channel streams need to be removed, this method have to be called repeatedly.
- Call it after joining room (joinRoom).

##### Parameter[](#removePublishTranscodingStreamUrl)

| Parameter | Description |
| :--- | :--- |
| taskId | The transcoding task ID is generated by application. It shall be unique globally, and only supports character set composed of a-zA-Z0-9 with length of no more than 20 characters. |
| url | The publishing stream address to be deleted, the format is RTMP.<br>The special characters such as Chinese cannot be supported, and the address length cannot be more than 512 bytes.<br>Note: some CDN manufacturers may not support 512 bytes, for example, the Aliyun only supports 256 bytes. |

##### Return[](#removePublishTranscodingStreamUrl)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.addSubscribe

```java
public int addSubscribe(String roomId, String uid)
```

Subscribe stream of specified user across the room.

- Subscribe audio/video stream of other rooms after joining the room. Namely, this function can be called after joining the room (joinRoom). Leaving the room will empty the configuration.

##### Parameter[](#addSubscribe)

| Parameter | Description |
| :--- | :--- |
| roomId | Room ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| uid | User ID, the corresponding anchor uid of audio/video to be subscribed |

##### Return[](#addSubscribe)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.removeSubscribe

```java
public int removeSubscribe(String roomId, String uid)
```

Remove the subscription of stream of specified user across the room.

- Remove the subscription of audio/video stream of other rooms. It plays a opposite role with the [addSubscribe](#ThunderEngine.addSubscribe) interface. It also shall be called after joining the room (joinRoom).

##### Parameter[](#removeSubscribe)

| Parameter | Description |
| :--- | :--- |
| roomId | Room ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| uid | User ID, the corresponding anchor uid of audio/video to be unsubscribed |

##### Return[](#removeSubscribe)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.switchFrontCamera

```java
public int switchFrontCamera(boolean bFront)
```

Switch to front/rear camera.

- It needs to be called after starting the preview [startVideoPreview](#ThunderEngine.startVideoPreview).
- The front camera is by default enabled when this method is not called.

##### Parameter[](#switchFrontCamera)

| Parameter | Description |
| :--- | :--- |
| bFront | true: enable front camera (default)<br>false: switch to rear camera |

##### Return[](#switchFrontCamera)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setVideoCaptureOrientation

```java
public int setVideoCaptureOrientation(int orientation)
```

Set the capture angle of camera (landscape/portrait).

- It can be valid before or after calling [startVideoPreview](#ThunderEngine.startVideoPreview) .
- The capture orientation is vertical by default when this method is not called.

##### Parameter[](#setVideoCaptureOrientation)

| Parameter | Description |
| :--- | :--- |
| orientation | The capture orientation of camera. For the optional value, refer to [ThunderRtcConstant.ThunderVideoCaptureOrientation](#ThunderRtcConstant.ThunderVideoCaptureOrientation) for details |

##### Return[](#setVideoCaptureOrientation)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.setLocalVideoMirrorMode

```java
public int setLocalVideoMirrorMode(int mode)
```

Set local video mirror mode.

- It can be valid before or after calling [startVideoPreview](#ThunderEngine.startVideoPreview) .
- This method is only applicable for front camera other than rear camera. The preview and stream publishing of rear camera will not be mirrored.
- By default, the front camera mirrors preview other than stream publishing.

##### Parameter[](#setLocalVideoMirrorMode)

| Parameter | Description |
| :--- | :--- |
| mode | Mirror mode. For the optional value, see[ThunderRtcConstant.ThunderVideoMirrorMode](#ThunderRtcConstant.ThunderVideoMirrorMode) for details |

##### Return[](#setLocalVideoMirrorMode)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderEngine.enableWebSdkCompatibility

```java
public int enableWebSdkCompatibility(boolean enabled)
```

Enable/Disable WebSDK compatibility.

- After enabling WebSDK compatibility, the encoding B-frames is prohibited internally, because it cannot be encoded normally by WebSDK.
- This is applicable for live scenes and shall be called before publishing. It has nothing to join/exit channel, and only be reset when destroyEngine is performed
- Audio/Video connection is compatible with Web SDK by default, and there is no need to calling this method.

##### Parameter[](#enableWebSdkCompatibility)

| Parameter | Description |
| :--- | :--- |
| enabled | true: Compatible<br>false: Incompatible (default) |

##### Return[](#enableWebSdkCompatibility)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

### ThunderAudioFilePlayer

#### ThunderAudioFilePlayer.open

```java
public void open(final String path)
```

Open the file to be played, and the following formats are supported: mp3, aac, wav.

##### Parameter[](#open)

| Parameter | Description |
| :--- | :--- |
| path | Audio file path |

--------------------------

#### ThunderAudioFilePlayer.close

```java
public void close()
```

Close play file, and [ThunderAudioFilePlayer.open](#ThunderAudioFilePlayer.open) can be called again.

--------------------------

#### ThunderAudioFilePlayer.play

```java
public void play()
```

Start playing.

--------------------------

#### ThunderAudioFilePlayer.stop

```java
public void stop()
```

Stop playing, and call [ThunderAudioFilePlayer.play](#ThunderAudioFilePlayer.play) to play again.

--------------------------

#### ThunderAudioFilePlayer.pause

```java
public void pause()
```

Suspend playing, and call [ThunderAudioFilePlayer.resume](#ThunderAudioFilePlayer.resume) to continue.

--------------------------

#### ThunderAudioFilePlayer.resume

```java
public void resume()
```

Continue to play.

--------------------------

#### ThunderAudioFilePlayer.seek

```java
public void seek(final long timeMS)
```

Skip to specified play time.(Only support local audio files)

##### Parameter[](#seek)

| Parameter | Description |
| :--- | :--- |
| timeMS | The time (in seconds), shall be no more than the value obtained by [ThunderAudioFilePlayer.getTotalPlayTimeMS](#ThunderAudioFilePlayer.getTotalPlayTimeMS) |

--------------------------

#### ThunderAudioFilePlayer.getTotalPlayTimeMS

```java
public long getTotalPlayTimeMS()
```

Get the total play time of files.

##### Return[](#getTotalPlayTimeMS)

- Total play time in seconds

--------------------------

#### ThunderAudioFilePlayer.getCurrentPlayTimeMS

```java
public long getCurrentPlayTimeMS()
```

Get the time which has been played.

##### Return[](#getCurrentPlayTimeMS)

- The time (in seconds) which has been played, shall be no more than the value obtained by [ThunderAudioFilePlayer.getTotalPlayTimeMS](#ThunderAudioFilePlayer.getTotalPlayTimeMS)

--------------------------

#### ThunderAudioFilePlayer.setPlayVolume

```java
public void setPlayVolume(int volume)
```

Set play volume of current music files locally (anchor) and remotely (audience).

##### Parameter[](#setPlayVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-100] |

--------------------------

#### ThunderAudioFilePlayer.setPlayerLocalVolume

```java
public int setPlayerLocalVolume(int volume)
```

Adjust the local volume of music files. Call this method in the room.

##### Parameter[](#setPlayerLocalVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-100] |

##### Return[](#setPlayerLocalVolume)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.setPlayerPublishVolume

```java
public int setPlayerPublishVolume(int volume)
```

Adjust remote volume of music files. Call this method in the room.

##### Parameter[](#setPlayerPublishVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-100] |

##### Return[](#setPlayerPublishVolume)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.getPlayerLocalVolume

```java
public int getPlayerLocalVolume()
```

Get the local volume of music files.

##### Return[](#getPlayerLocalVolume)

- [0-100]: Volume value, ranging from [0 to 100]
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.getPlayerPublishVolume

```java
public int getPlayerPublishVolume()
```

Get the remote volume of music files.

##### Return[](#getPlayerPublishVolume)

- [0-100]: Volume value, ranging from [0 to 100]
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.getAudioTrackCount

```java
public int getAudioTrackCount()
```

Get audio track count of audio files.

##### Return[](#getAudioTrackCount)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.selectAudioTrack

```java
public int selectAudioTrack(int audioTrack)
```

Switch to specified audio track.

##### Parameter[](#selectAudioTrack)

| Parameter | Description |
| :--- | :--- |
| audiotrack | Specified audio track to be switch to. 0 indicates the first audio track |

##### Return[](#selectAudioTrack)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.setSemitone

```java
public void setSemitone(int val)
```

Set a tone for audio playing.

##### Parameter[](#setSemitone)

| Parameter | Description |
| :--- | :--- |
| val | Optional value of tone quantity: -5, -4, -3, -2, -1, 0(normal), 1, 2, 3, 4, 5 |

--------------------------

#### ThunderAudioFilePlayer.setLooping

```java
public int setLooping(int cycle)
```

Sets times of loop playbacks.

##### Parameter[](#setLooping)

| Parameter | Description |
| :--- | :--- |
| cycle | -1: indicates infinite loop <br>0: No loop (default value); Positive integer: Loop times<br> |

##### Return[](#setLooping)

- 0: Success.
- <0: Failure. For detailed return code, refer to [ThunderRtcConstant.ThunderRet](.mdcode.md#ThunderRtcConstant.ThunderRet)

--------------------------

#### ThunderAudioFilePlayer.enablePublish

```java
public void enablePublish(boolean enable)
```

Whether to use this currently played audio file as the live accompaniment.

##### Parameter[](#enablePublish)

| Parameter | Description |
| :--- | :--- |
| enable | true: Enable<br>false: disable (default) |

--------------------------

#### ThunderAudioFilePlayer.setPlayerNotify

```java
public synchronized void setPlayerNotify(IThunderAudioFilePlayerCallback callback)
```

Set callback interface of audio file player.

##### Parameter[](#setPlayerNotify)

| Parameter | Description |
| :--- | :--- |
| callback | The callback interface of audio file player, refer to [ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback](.mdnotification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback) for details |

--------------------------

#### ThunderAudioFilePlayer.enableVolumeIndication

```java
public synchronized void enableVolumeIndication(boolean enable, int interval)
```

Enable the volume callback on audio file playing.

##### Parameter[](#enableVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| enable | true: Enable<br>false: disable (default) |
| interval | Callback interval (in seconds). More than 200 ms is recommended; if <=0, reset it as 200ms. |

--------------------------

#### ThunderAudioFilePlayer.setMixStandard

```java
public synchronized void setMixStandard(boolean standard)
```

Set whether audio file is a mixed video standard stream.

##### Parameter[](#setMixStandard)

| Parameter | Description |
| :--- | :--- |
| standard | true: Standard stream<br>false: Non-standard stream (default) |

--------------------------

#### ThunderAudioFilePlayer.isMixStandard

```java
public synchronized boolean isMixStandard()
```

Query whether audio file is a mixed video standard stream.

##### Return[](#isMixStandard)

- true: Mixed video standard stream
- false: Not mixed video standard stream

--------------------------

## Parameter type

### ThunderRtcConstant

#### ThunderRtcConstant.RoomConfig

```java
public static final class RoomConfig
```

Room mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_ROOMCONFIG_LIVE(0) | Live streaming mode, where quality is prioritized and delay is large. Applicable to viewer or audience scenario. When audience publishes audio/video and becomes anchors, the value changes to communication mode. |
| THUNDER_ROOMCONFIG_COMMUNICATION(1) | Communication mode is applicable for 1v1 communication and group conversation due to its short time delay and fluent communication. |
| THUNDER_ROOMCONFIG_MULTIAUDIOROOM(4) | Audio room mode is applicable for group audio room due to its low time delay and low bandwidth occupied |

--------------------------

#### ThunderRtcConstant.AudioConfig

```java
public static final class AudioConfig
```

Audio Profiles

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_CONFIG_DEFAULT(0) | Default settings. which is 1 in communication mode, and 2 in live mode. |
| THUNDER_AUDIO_CONFIG_SPEECH_STANDARD(1) | Specify the sampling rate of 16 KHz, and the audio encode, single track and encoding rate of 18 kbps SILK |
| THUNDER_AUDIO_CONFIG_MUSIC_STANDARD_STEREO(2) | Specify the sampling rate of 44.1 KHz, and the music encode, dual track and encoding rate of 24 kbps SILK. The encode is long in time delay, EAAC+ |
| THUNDER_AUDIO_CONFIG_MUSIC_STANDARD(3) | Specify the sampling rate of 44.1 KHz, and the music encode, dual track and encoding rate of 40 kbps SILK. The encode is low in time delay, ELD AAC |
| THUNDER_AUDIO_CONFIG_MUSIC_HIGH_QUALITY_STEREO(4) | Specify the sampling rate of 44.1KHz, and the music encode, dual track and encoding rate of 128kbps, AAC LC |

--------------------------

#### ThunderRtcConstant.CommutMode

```java
public static final class CommutMode
```

Interactive mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_COMMUT_MODE_DEFAULT(0) | Default mode, equals to THUNDER_COMMUT_MODE_HIGH(1) |
| THUNDER_COMMUT_MODE_HIGH(1) | High interactive mode |
| THUNDER_COMMUT_MODE_LOW(2) | Low interactive mode |

--------------------------

#### ThunderRtcConstant.ScenarioMode

```java
public static final class ScenarioMode
```

Scenario mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_SCENARIO_MODE_DEFAULT(0) | Default mode, equals to THUNDER_SCENARIO_MODE_STABLE_FIRST(1) |
| THUNDER_SCENARIO_MODE_STABLE_FIRST(1) | Fluent priority: applicable for stable education |
| THUNDER_SCENARIO_MODE_QUALITY_FIRST(2) | Tone quality priority: applicable for show field with a few or without interaction |

--------------------------

#### ThunderRtcConstant.AreaType

```java
public static final class AreaType
```

Scenario mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AREA_DEFAULT(0) | Default value (China) |
| THUNDER_AREA_FOREIGN(1) | Overseas |

--------------------------

#### ThunderRtcConstant.AuthResult

```java
public static final class AuthResult
```

Authentication results

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUTHRES_SUCCUSS(0) | Authentication succeeded |
| THUNDER_AUTHRES_ERR_SERVER_INTERNAL(10000) | Server internal error, try again |
| THUNDER_AUTHRES_ERR_NO_TOKEN(10001) | If there is no token, call [ThunderEngine.updateToken](#ThunderEngine.updateToken) |
| THUNDER_AUTHRES_ERR_TOKEN_ERR(10002) | Token authentication failed (incorrect digital signature), which may be caused by incorrect appSecret |
| THUNDER_AUTHRES_ERR_APPID(10003) | appid in token is inconsistent with appid when execute authentication |
| THUNDER_AUTHRES_ERR_UID(10004) | uid in token is inconsistent with uid when execute authentication |
| THUNDER_AUTHRES_ERR_TOKEN_EXPIRE(10005) | token has expired |
| THUNDER_AUTHRES_ERR_NO_APP(10006) | App does not exist, which is not registered in the management background |
| THUNDER_AUTHRES_ERR_TOKEN_WILL_EXPIRE(10007) | token is about to expire |
| THUNDER_AUTHRES_ERR_BAND(10008) | The user is baned |

--------------------------

#### ThunderRtcConstant.UserOfflineReason

```java
public static final class UserOfflineReason
```

Offline reason for user

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_OFFLINE_QUIT(0) | The user is offline actively |
| THUNDER_OFFLINE_DROPPED(1) | The packet could not be received for long time, lost connection due to timeout. Note: Because SDK uses unreliable channel, the counterpart may leave our side actively. So it is misjudged as timeout offline |
| THUNDER_OFFLINE_BECOME_AUDIENCE(2) | User status is switched from anchor to audience (live mode) |

--------------------------

#### ThunderRtcConstant.NetworkQuality

```java
public static final class NetworkQuality
```

Network quality

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_QUALITY_UNKNOWN(0) | Unknown quality |
| THUNDER_QUALITY_EXCELLENT(1) | Excellent network quality |
| THUNDER_QUALITY_GOOD(2) | Good network quality |
| THUNDER_QUALITY_POOR(3) | The network quality is poor, but the communication is not affected even the user can feel its defects. |
| THUNDER_QUALITY_BAD(4) | The network quality is bad, and the communication can be barely made but is not smooth |
| THUNDER_QUALITY_VBAD(5) | The network quality is very bad, the communication cannot be made basically |
| THUNDER_QUALITY_DOWN(6) | The network has been disconnected, and the communication cannot be made at all |

--------------------------

#### ThunderRtcConstant.SourceType

```java
public static final class SourceType
```

Audio publishing mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_PUBLISH_MODE_MIC(0) | Microphone (only microphone capture is published to room) |
| THUNDER_PUBLISH_MODE_FILE(1) | Accompaniment (only file play is published to room) |
| THUNDER_PUBLISH_MODE_MIX(2) | Mix (the microphone capture and file play are published to room) |
| THUNDER_PUBLISH_MODE_NONE(3) | Stop all upstream audio data |

--------------------------

#### ThunderRtcConstant.SoundEffectMode

```java
public static final class SoundEffectMode
```

Sound effect mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_SOUND_EFFECT_MODE_NONE() | Disable mode |
| THUNDER_SOUND_EFFECT_MODE_VALLEY() | VALLEY mode |
| THUNDER_SOUND_EFFECT_MODE_RANDB() | R&B mode |
| THUNDER_SOUND_EFFECT_MODE_KTV() | KTV mode |
| THUNDER_SOUND_EFFECT_MODE_CHARMING() | CHARMING mode |
| THUNDER_SOUND_EFFECT_MODE_POP() | Pop mode |
| THUNDER_SOUND_EFFECT_MODE_HIPHOP() | Hip-hop mode |
| THUNDER_SOUND_EFFECT_MODE_ROCK() | Rock mode |
| THUNDER_SOUND_EFFECT_MODE_CONCERT() | Concert mode |
| THUNDER_SOUND_EFFECT_MODE_STUDIO() | Studio mode |

--------------------------

#### ThunderRtcConstant.VoiceChangerMode

```java
public static final class VoiceChangerMode
```

Voice changing mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_VOICE_CHANGER_MODE_NONE(0) | Disable mode |
| THUNDER_VOICE_CHANGER_MODE_ETHEREAL(1) | Ethereal |
| THUNDER_VOICE_CHANGER_MODE_THRILLER(2) | Thriller |
| THUNDER_VOICE_CHANGER_MODE_LUBAN(3) | Luban |
| THUNDER_VOICE_CHANGER_MODE_LORIE(4) | Lorie |
| THUNDER_VOICE_CHANGER_MODE_UNCLE(5) | Uncle |
| THUNDER_VOICE_CHANGER_MODE_DIEFAT(6) | Die-fat |
| THUNDER_VOICE_CHANGER_MODE_BADBOY(7) | Bad boy |
| THUNDER_VOICE_CHANGER_MODE_WRACRAFT(8) | Warcraft |
| THUNDER_VOICE_CHANGER_MODE_HEAVYMETAL(9) | Heavy metal |
| THUNDER_VOICE_CHANGER_MODE_COLD(10) | Cold |
| THUNDER_VOICE_CHANGER_MODE_HEAVYMECHINERY(11) | Heavy mechinery |
| THUNDER_VOICE_CHANGER_MODE_TRAPPEDBEAST(12) | Trapped breast |
| THUNDER_VOICE_CHANGER_MODE_POWERCURRENT(13) | Power current |

--------------------------

#### ThunderRtcConstant.AudioSaverMode

```java
public static final class AudioSaverMode
```

Audio saving mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_SAVER_ONLY_CAPTURE(0) | Only save upstream audio data in channel. The voices of microphone capture and accompaniment can be saved after being set as upstream |
| THUNDER_AUDIO_SAVER_ONLY_RENDER(1) | Save downstream audio data in room |
| THUNDER_AUDIO_SAVER_BOTH(2) | Save upstream and downstream audio data in room |

--------------------------

#### ThunderRtcConstant.AudioSaverWfMode

```java
public static final class AudioSaverWfMode
```

Writing file mode for saving audio

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_SAVER_FILE_APPEND(0) | Open a file and put additional data at the end of file |
| THUNDER_AUDIO_SAVER_FILE_OVERRIDE(1) | Open a file, and the written data will overlap its original content |

--------------------------

#### ThunderRtcConstant.ThunderAudioRawFrameOperationMode

```java
public static final class ThunderAudioRawFrameOperationMode
```

The use mode of onRecordAudioFrame

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_ONLY(0) | Read-only mode. The user can only get original audio data from AudioFrame |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_WRITE_ONLY(1) | Write-only mode. The user replaces the data in AudioFrame to Thunder SDK for encoding and transmission |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_WRITE(2) | Read/write mode. The user obtains and modifies data from AudioFrame, and return it to Thunder SDK for encoding and transmission. |

--------------------------

#### ThunderRtcConstant.ExternalVideoPixelFormat

```java
public static final class ExternalVideoPixelFormat
```

External video pixel format

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_PIXEL_FORMAT_RGBA(0) | RGBA format |
| THUNDER_PIXEL_FORMAT_I420(1) | I420 format |
| THUNDER_PIXEL_FORMAT_NV21(2) | NV21 format |

--------------------------

#### ThunderRtcConstant.ThunderNetworkType

```java
public static final class ThunderNetworkType
```

Network connection type

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_NETWORK_TYPE_UNKNOWN(0) | Unknown network connection type |
| THUNDER_NETWORK_TYPE_DISCONNECTED(1) | The network has been disconnected |
| THUNDER_NETWORK_TYPE_CABLE(2) | Cable network |
| THUNDER_NETWORK_TYPE_WIFI(3) | Wi-Fi (hotspot included) |
| THUNDER_NETWORK_TYPE_MOBILE(4) | Mobile network. 2G, 3G and 4G network cannot be differentiated |
| THUNDER_NETWORK_TYPE_MOBILE_2G(5) | 2G mobile network |
| THUNDER_NETWORK_TYPE_MOBILE_3G(6) | 3G mobile network |
| THUNDER_NETWORK_TYPE_MOBILE_4G(7) | 4G mobile network |

--------------------------

#### ThunderRtcConstant.ThunderConnectionStatus

```java
public static final class ThunderConnectionStatus
```

The network connection status with server

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_CONNECTION_STATUS_CONNECTING(0) | Connecting |
| THUNDER_CONNECTION_STATUS_CONNECTED(1) | Connected |
| THUNDER_CONNECTION_STATUS_DISCONNECTED(2) | Disconnected |

--------------------------

#### ThunderRtcConstant.ThunderVideoCaptureOrientation

```java
public static final class ThunderVideoCaptureOrientation
```

Video capture orientation

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_ORIENTATION_PORTRAIT(0) | Portrait |
| THUNDER_VIDEO_CAPTURE_ORIENTATION_LANDSCAPE(1) | Landscape |

--------------------------

#### ThunderRtcConstant.ThunderVideoMirrorMode

```java
public static final class ThunderVideoMirrorMode
```

Mirror mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_MIRROR_PUBLISH_NO_MIRROR(0) | The preview other than stream publishing is mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_MIRROR(1) | Both preview and stream publishing are not mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_NO_MIRROR(2) | Neither preview and stream publishing is not mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_NO_MIRROR_PUBLISH_MIRROR(3) | Preview is not mirrored, but publish is mirrored |

--------------------------

#### ThunderRtcConstant.ThunderPublishCDNErrorCode

```java
public static final class ThunderPublishCDNErrorCode
```

Stream publishing results

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_PUBLISH_CDN_ERR_SUCCESS(0) | Stream publishing succeeded |
| THUNDER_PUBLISH_CDN_ERR_TOCDN_FAILED(1) | Publishing stream to external server (CDN) is failed.<br> 1. Check whether url is correct. <br>2. Check whether the token in the URL is valid (generally, token is required during cdn stream publishing and can be ignored if it doe not exist). |
| THUNDER_PUBLISH_CDN_ERR_THUNDERSERVER_FAILED(2) | Publish the stream to thunder internal server is failed.<br> 1. Check anchor’s upstream network <br>2. Contact us to troubleshoot internal transmission problems |
| THUNDER_PUBLISH_CDN_ERR_THUNDERSERVER_STOP(3) | Stop stream publishing |

--------------------------

#### ThunderRtcConstant.ThunderSendMediaExtraInfoFailedStatus

```java
public static final class ThunderSendMediaExtraInfoFailedStatus
```

Failure status of sending extra information

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_EMPTY(1) | Extra information is null. |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_TOO_LARGE(2) | The data to be sent each time is too large. No more than 200 bytes when only publishing audio, and no more than 2048 bytes when publishing video |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_FREQUENCY_TOO_HIGHT(3) | The sending frequency is too high, which cannot exceeds 100ms each time |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NOT_IN_ANCHOR_SYSTEM(4) | Not an anchor system |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_JOIN_MEDIA(5) | Channel not to be joined |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_PUBLISH_SUCCESS(6) | Publishing failed |

--------------------------

#### ThunderRtcConstant.ThunderAudioDeviceStatus

```java
public static final class ThunderAudioDeviceStatus
```

Audio device status

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_SUCCESS(0) | Callback on successful initialization of audio capture device |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_ERROR_OR_NO_PERMISSION(1) | Callback on initialization failure of audio capture. It may be caused by no permission |
| THUNDER_AUDIO_DEVICE_STATUS_RELEASE_CAPTURE_SUCCESS(2) | Callback on successful release of audio capture device |

--------------------------

#### ThunderRtcConstant.ThunderVideoCaptureStatus

```java
public static final class ThunderVideoCaptureStatus
```

Video capture status

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_STATUS_SUCCESS(0) | Succeeded |
| THUNDER_VIDEO_CAPTURE_STATUS_AUTHORIZED(1) | Authorize |
| THUNDER_VIDEO_CAPTURE_STATUS_NOT_DETERMINED(2) | No permission given |
| THUNDER_VIDEO_CAPTURE_STATUS_RESTRICTED(3) | Occupied |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(4) | No permission |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(5) | Close |

--------------------------

#### ThunderRtcConstant.LiveTranscodingMode

```java
public static final class LiveTranscodingMode
```

Configuration bracket for video mixing and transcoding output

Each bracket includes configuration of audio and video.

The default configuration of audio's each bracket is:

| Encoding protocol | Bit rate | Sampling rate | Number of channels |
| :--- | :--- | :--- | :--- |
| encode | bitrate | sample | channel |
| 1 | 128 | 44100 | 2 |

The default configuration of video's each bracket is:

| Profile (value) | Bracket value | Resolution | Bit rate | Frame rate |
| :--- | :--- | :--- | :--- | :--- |
| TRANSCODING_MODE_320X180(1) | 1 | 320*180 | 150kbps | 15fps |
| TRANSCODING_MODE_320X240(2) | 2 | 320*240 | 200kbps | 15fps |
| TRANSCODING_MODE_640X360(3) | 3 | 640*360 | 500kbps | 15fps |
| TRANSCODING_MODE_640X480(4) | 4 | 640*480 | 500kbps | 15fps |
| TRANSCODING_MODE_960X544(5) | 5 | 960*544 | 1000kbps | 24fps |
| TRANSCODING_MODE_1280X720(6) | 6 | 1280*720 | 1600kbps | 24fps |
| TRANSCODING_MODE_1920X1080(7) | 7 | 1920*1080 | 4500kbps | 24fps |
|  | 101 | 180*320 | 150kbps | 15fps |
|  | 102 | 240*320 | 200kbps | 15fps |
|  | 103 | 360*640 | 500kbps | 15fps |
|  | 104 | 480*640 | 500kbps | 15fps |
|  | 105 | 544*960 | 1000kbps | 24fps |
|  | 106 | 720*1280 | 1600kbps | 24fps |
|  | 107 | 1080*1920 | 4500kbps | 24fps |

--------------------------

#### ThunderRtcConstant.ThunderUserRole

```java
public static final class ThunderUserRole
```

User role

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERUSER_ROLE_AUDIENCE(0) | Only audience |
| THUNDERUSER_ROLE_ANCHOR(1) | Anchor. If the audience interacts with the anchor, it will become an anchor |

--------------------------

#### ThunderRtcConstant.ThunderLogLevel

```java
public static final class ThunderLogLevel
```

Log level

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERLOG_LEVEL_TRACE(0) | TRACE |
| THUNDERLOG_LEVEL_DEBUG(1) | DEBUG |
| THUNDERLOG_LEVEL_INFO(2) | INFO |
| THUNDERLOG_LEVEL_WARN(3) | WARN |
| THUNDERLOG_LEVEL_ERROR(4) | ERROR |
| THUNDERLOG_LEVEL_RELEASE(10) | RELEASE |

--------------------------

#### ThunderRtcConstant.ThunderCameraPosition

```java
public static final class ThunderCameraPosition
```

Camera position

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERCAMERA_POSITION_FRONT(0) | Front camera |
| THUNDERCAMERA_POSITION_BACK(1) | Rear camera. |

--------------------------

#### ThunderRtcConstant.ThunderPublishOrientation

```java
public static final class ThunderPublishOrientation
```

Orientation for publishing video

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERPUBLISH_VIDEO_ORIENTATION_PORTRAIT(0) | Portrait |
| THUNDERPUBLISH_VIDEO_ORIENTATION_LANDSCAPE(1) | Landscape |

--------------------------

#### ThunderRtcConstant.ThunderVideoEncodeType

```java
public static final class ThunderVideoEncodeType
```

Protocol type for encoding video

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERVIDEO_ENCODE_TYPE_H264(0) | H264 |
| THUNDERVIDEO_ENCODE_TYPE_H265(1) | H265 |

--------------------------

#### ThunderRtcConstant.ThunderVideoViewScaleMode

```java
public static final class ThunderVideoViewScaleMode
```

The video displays scale mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERVIDEOVIEW_SCALE_MODE_FILL(0) | Fill the window. If the proportion is not fit, it will be stretched to fill the window. |
| THUNDERVIDEOVIEW_SCALE_MODE_ASPECT_FIT(1) | Adapt to the window. If the proportion is not fit, black edge will be left |
| THUNDERVIDEOVIEW_SCALE_MODE_CLIP_TO_BOUNDS(2) | Fill the window. If the proportion is not fit, it will be cut out |

--------------------------

#### ThunderRtcConstant.ThunderPublishPlayType

```java
public static final class ThunderPublishPlayType
```

Publish play type

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERPUBLISH_PLAY_SINGLE(0) | Single publishing |
| THUNDERPUBLISH_PLAY_INTERACT(1) | Video connection publishing |
| THUNDERPUBLISH_PLAY_SCREENCAP(2) | Screen recording publishing |
| THUNDERPUBLISH_PLAY_MULTI_INTERACT(3) | Multi-person video connection publishing |

--------------------------

#### ThunderRtcConstant.ThunderRtcRemotePlayType

```java
public static final class ThunderRtcRemotePlayType
```

Remote end display type

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_REMOTE_PLAY_NORMAL(0) | common audience view |
| THUNDER_REMOTE_PLAY_MULTI(1) | Multiple interaction view |

--------------------------

#### ThunderRtcConstant.ThunderPublishVideoMode

```java
public static final class ThunderPublishVideoMode
```

Video gear configuration

| Profile (value) | Meaning | Resolution | CodeRate | FrameRate |
| :--- | :--- | :--- | :--- | :--- |
| THUNDERPUBLISH_VIDEO_MODE_NORMAL(1) | 标清档 | 320*240(横屏) | 200Kbps | 15fps |
| THUNDERPUBLISH_VIDEO_MODE_HIGHQULITY(2) | 高清档 | 368*640(竖屏) | 500Kbps | 15fps |
| THUNDERPUBLISH_VIDEO_MODE_SUPERQULITY(3) | 超清档 | 544*960(竖屏) | 1000Kbps | 24fps |
| THUNDERPUBLISH_VIDEO_MODE_BLUERAY_2M(4) | 蓝光档 | 720*1280(竖屏) | 1500Kbps | 24fps |
| THUNDERPUBLISH_VIDEO_MODE_BLUERAY_4M(5) | 蓝光档 | 1080*1920(竖屏) | 3000Kbps | 24fps |

--------------------------

#### ThunderRtcConstant.ThunderVideoViewType

```java
public static final class ThunderVideoViewType
```

View type

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERVIDEO_VIEW_PREVIEW(1) | Preview |
| THUNDERVIDEO_VIEW_PLAYVIEW(2) | Play view |

--------------------------

#### ThunderRtcConstant.ThunderRtcProfile

```java
public static final class ThunderRtcProfile
```

Media mode

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_PROFILE_DEFAULT(0) | Default mode, equals to THUNDER_PROFILE_NORMAL(1) audio/video mode |
| THUNDER_PROFILE_NORMAL(1) | Audio/video mode (audio and video are both used) |
| THUNDER_PROFILE_ONLY_AUDIO(2) | Pure audio mode (for scenario without video, so as to get more quality audio) |

--------------------------

#### ThunderRtcConstant.ThunderVideoRenderMode

```java
public static final class ThunderVideoRenderMode
```

Video rendering mode (the same as the scale mode)

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDERVIDEOVIEW_SCALE_MODE_FILL(0) | Fill the window. If the proportion is not fit, it will be stretched to fill the window. |
| THUNDERVIDEOVIEW_SCALE_MODE_ASPECT_FIT(1) | Adapt to the window. If the proportion is not fit, black edge will be left |
| THUNDERVIDEOVIEW_SCALE_MODE_CLIP_TO_BOUNDS(2) | Fill the window. If the proportion is not fit, it will be cut out |

--------------------------

#### ThunderRtcConstant.LiveEngineCaptureType

```java
public static final class LiveEngineCaptureType
```

Live engine capture Class

| Profile (value) | Meaning |
| :--- | :--- |
| THUNDER_CAPTURE_TYPE_DEFAULT_CAMERA(0) | Camera |
| THUNDER_CAPTURE_TYPE_SCREEN_RECORD(1) | Screen recording |
| THUNDER_CAPTURE_TYPE_EXTERNAL_SOURCE(2) | External stream publishing yuv |

--------------------------

#### ThunderRtcConstant.ThunderVideoCodecType

```java
public static final class ThunderVideoCodecType
```

Protocol Class for encoding and decoding video

| Profile (value) | Meaning |
| :--- | :--- |
| VIDEO_CODEC_UNKNOW(0) | Unknown type |
| VIDEO_CODEC_VP8(1) | VP8 |
| VIDEO_CODEC_H264(2) | H264 |
| VIDEO_CODEC_H265(3) | H265 |

--------------------------

#### ThunderRtcConstant.ThunderVideoQualityAdapt

```java
public static final class ThunderVideoQualityAdapt
```

Quality adaptability of local videos since last statistics (based on target frame rate and target code rate)

| Profile (value) | Meaning |
| :--- | :--- |
| ADAPT_NONE(0) | The quality of local video is constant |
| ADAPT_UP_BANDWIDTH(1) | The quality of local video has been improved because of higher network bandwidth |
| ADAPT_DOWN_BANDWIDTH(2) | The quality of local video becomes worse because of lower network bandwidth |

--------------------------

#### ThunderRtcConstant.ReverbExParameter

Reverberation parameter Class

```java
public static final class ReverbExParameter {
        /**
         * Room size; range [0~100]
         */
        public float mRoomSize = 0;
        /**
         * Pre-delay; range [0~200]
         */
        public float mPreDelay = 0;
        /**
         * Reverberation; range: [0~100]
         */
        public float mReverberance = 0;
        /**
         * High frequency factor; range [0~100]
         */
        public float mHfDamping = 0;
        /**
         * Low frequency; range: [0~100]
         */
        public float mToneLow = 0;
        /**
         * High frequency; range: [0~100]
         */
        public float mToneHigh = 0;
        /**
         * Wet gain; range: [-20~10]
         */
        public float mWetGain = 0;
        /**
         * Dry gain; range: [-20~10]
         */
        public float mDryGain = 0;
        /**
         * Stereo width range: [0~100]
         */
        public float mStereoWidth = 0;
    }
```

--------------------------

#### ThunderRtcConstant.CompressorParam

Compressor parameter Class

```java
public static final class CompressorParam {
        /**
         * Threshol; range: [-40~0]
         */
        public int mThreshold = 0;
        /**
         * Gain
         */
        public int mMakeupGain = 0;
        /**
         * Ratio
         */
        public int mRatio = 0;
        /**
         * Slope
         */
        public int mKnee = 0;
        /**
         * Release time; range: greater than0
         */
        public int mReleaseTime = 0;
        /**
         * Start time; range: greater than 0
         */
        public int mAttackTime = 0;
    }
```

--------------------------

#### ThunderRtcConstant.LimterParam

Limiter parameter Class

```java
public static final class LimterParam {
        /*
         *  -30 ~ 0
         */
        public float fCeiling = 0;
        /*
         *  -10 ~ 0
         */
        public float fThreshold = 0;
        /*
         *   0 ~ 30
         */
        public float fPreGain = 0;
        /*
         *  0 ~ 1000
         */
        public float fRelease = 0;
        /*
         *  0 ~ 1000
         */
        public float fAttack = 0;
        /*
         *   0 ~ 8
         */
        public float fLookahead = 0;
        /*
         * 0.5 ~ 2
         */
        public float fLookaheadRatio = 0;
        /*
         * 0 ~ 100
         */
        public float fRMS = 0;
        /*
         * 0 ~ 1
         */
        public float fStLink = 0;
    }
```

--------------------------

### ThunderVideoEncoderConfiguration

Parameter Class of video encoding configuration

```java
public class ThunderVideoEncoderConfiguration {
    public int playType;//Playing method
    public int publishMode;//Publish bracket
}
```

| Profile (value) | Meaning |
| :--- | :--- |
| playType | Play type. For the optional value, refer to [ThunderRtcConstant.ThunderVideoCaptureOrientation](#ThunderRtcConstant.ThunderPublishPlayType) for details |
| publishMode | Publish bracket. For the optional value, refer to [ThunderRtcConstant.ThunderVideoCaptureOrientation](#ThunderRtcConstant.ThunderPublishVideoMode) for details |

--------------------------

### ThunderBoltImage

Parameter Class for video watermark configuration

```java
public class ThunderBoltImage {

    /*
     * During the local video living streaming and mixed video publishing, URL is defined differently.
     * During the local live streaming, URL indicates the local absolute path of image on the local live streaming video;
     * During the mixed video publishing, URL indicates the address of watermark image outputted by mixed audio. (The watermark is not supported in the mixed video output stream for the time being).
     */
    public String url;
    public int x;      //The horizontal coordinate at upper left corner of the picture on the video frame.
    public int y;      //The vertical coordinate at upper left corner of the picture on the video frame.
    public int width;  //The width of the picture on the video frame.
    public int height; //The height of the picture on the video frame.

}
```

--------------------------

### ThunderMultiVideoViewParam

The display layout parameter of multi-channel videos when there is multiple interaction

```java
public class ThunderMultiVideoViewParam {
    public ArrayList<VideoPosition> mVideoPositions;    // Layout parameters of video/view
    public VideoPosition mBgPosition;                   // Layout parameters of video/view background picture
    public Bitmap mBgBitmap;                            // Video/view background picture
}
```

| Parameter | Description |
| :--- | :--- |
| mVideoPositions | The position information of all grids. Multiple video is combined based on array |
| mBgPosition | The position information of background pictures |
| bgImageName | Background picture |

```java
/*
 * The following is VideoPosition diagram. The outline border indicates the overall video layout, and Video is a single vide area.
 *
 * |---------------------------------------------|
 * | (0,0)                                       |
 * |                                             |
 * |                             (mX,mY)         |
 * |                               |---width---| |
 * |                               |           | |
 * |                        height |           | |
 * |                               | Video     | |
 * |                               |           | |
 * |                               |-----------| |
 * |---------------------------------------------|
 */
public class VideoPosition {
    public int mIndex  = 0;  // Seat information for a single video/view layout
    public int mX      = 0;  // X coordinate of a single video/view layout
    public int mY      = 0;  // Y coordinate of a single video/view layout
    public int mWidth  = 0;  // Width of a single video/view
    public int mHeight = 0;  // Height of a single video/view
}
```

--------------------------

### ThunderVideoCanvas

Video display canvas

```java
public class ThunderVideoCanvas {
    public Object mView = null;//The view used to render video, often filled with FrameLayout
    public int mRenderMode;//Render vidio scale mode, refer to ThunderRtcConstant.ThunderVideoRenderMode for optional values
    public String mUid;//User’s uid
    public int mSeatIndex;// Display location of the user specified by mUid
}
```

--------------------------

### LiveTranscoding

Configuration Class of video mixing and transcoding task

```java
public class LiveTranscoding {

    //Video mixing transcoding bracket, developing output video coding parameters (such as resolution, bit rate, frame rate, etc.) by setting bracket, which is configured in the background of AIVACOM, and may be changed according to the needs of developers. See ThunderRtcConstant.LiveTranscodingMode for the default configuration information of the bracket
    private int mTransCodingMode;

    // Other parameters of video mixing, such as audio and video accompany address, lyrics address, etc.
    private String mAudioUrl = "";  // Audio file url as standard
    private String mLyricUrl = "";   // Lyrics file url corresponding to audio. Blank indicates that there is no lyrics. Otherwise, the lyrics will be added to the mixed video in the default style
    private String mMediaUrl = "";  // Video file url as standard
    private MediaStreamLayout mMediaStreamLayout; //Layout of video standard stream in video mixing, see LiveTranscoding.MediaStreamLayout below for details

    //All users in video mixing, see LiveTranscoding.TranscodingUser below for details
    private ArrayList<TranscodingUser> mUserList = new ArrayList<>();


    //Related operable functions
    /**
     * Add a user to the mixed video layout
     *
     * @param user
     * @return 0
     */
    public int addUser(TranscodingUser user);
    /**
     * Set user mixed video layout in batches
     * In this method, the user sets all users participating in the combined picture. This method replaces the original data with new User data.
     *
     * @param users All mixed video users in channel
     */
    public void setUsers(ArrayList<TranscodingUser> users);

    /**
     * Get current user location information
     *
     * @return Get information of all users in mixed video canvas in channel
     */
    public final ArrayList<TranscodingUser> getUsers()

    /**
     * Remove users joining video mixing
     *
     * @param uid ID User ID to be removed
     * @return 0
     */
    public int removeUser(String uid);

    /**
     * Remove the mixed video of this channel. That is, the user will not use the mixed video
     *
     * @return 0
     */
    public int removeAllUser();

    /**
     * Get the number of users joining video mixing
     *
     * @return Number of users joining video mixing
     */
    public int getUserCount();
    /**
     *  Set the bracket of mixed video outputted
     *
     * @param transCodingMode
     */
    public void setTransCodingMode(int transCodingMode);

    /**
     * Get the bracket of mixed video outputted
     *
     * @return Bracket of mixed video outputted
     */
    public int getTransCodingMode();

    /**
     * Set the external pure audio url as the standard stream for this mixed video. As the progress of the standard stream playback is required internally for synchronization of mixed video,
     * the client should use ThunderAudioFilePlayer to play this audio and call setMixStandard in ThunderAudioFilePlayer to set the standard stream.
     * If the user wants to use a customized style lyrics in the mixed video, the anchor can use the sendMediaExtraInfo interface to send the lyrics progress, and call setAudioOnlyStandardSreamUrl to set the lyricUrl parameter to null,
     * the audience will receive the onRecvMediaExtraInfo callback of IThunderMediaExtraInfoCallback when playing this mixed video stream, then read out the corresponding lyrics progress, and draw the lyrics according to the progress.
     * @param audioUrl Standard video file url
     * @param lyricUrl url of the lyrics file corresponding to the audio. The bank indicates no lyrics, otherwise the lyrics will be added to the mixed video in the default style.
     * @return 0 Succeeded， <0 Failed
     */
     public final int setAudioOnlyStandardSreamUrl(String audioUrl, String lyricUrl);

     /**
    * he external video media stream is set as the standard stream for mixed video, which cannot be used through interface setAudioOnlyStandardSreamUrl simultaneously.
    * @param mediaUrl Standard video file url
    * @param layout  Layout information of video media stream in the mixed video.
    * @return 0 Succeeded， <0 Failed
    */
    public final int setMediaStandardSream(String mediaUrl,  MediaStreamLayout layout);
}
```

Used layout information configuration types include:

- [LiveTranscoding.TranscodingUser](#LiveTranscoding.TranscodingUser)
- [LiveTranscoding.MediaStreamLayout](#LiveTranscoding.MediaStreamLayout)

For the default configuration of video mixing and transcoding output bracket, refer to [ThunderRtcConstant.LiveTranscodingMode](#ThunderRtcConstant.LiveTranscodingMode) for details

--------------------------

### LiveTranscoding

#### LiveTranscoding.TranscodingUser

Layout configuration information participated in user’s mixed video stream

```java
public static class TranscodingUser {

        public String uid;
        public String roomId;
        public boolean bStandard;//Standard stream user or not
        public int layoutX;        //User's location x in video mixing canvas
        public int layoutY;        //User's location y in video mixing canvas
        public int layoutW;        //User's location w in video mixing canvas
        public int layoutH;        //User's location h in video mixing canvas
        public int zOrder;      //Layer number of the user's video frame on the live video. The value range is the integer in [0, 100], and the minimum value is 0 (default value), indicating that the image in this region is at the lowest level
        public boolean bCrop;   //How to crop the source stream when the video mixing service places it in the canvas (0: mend black edge, 1: crop)
        public int cropX;      //X coordinate of crop region
        public int cropY;      //Y coordinate of crop region
        public int cropW;      //Width of crop region
        public int cropH;      //Height of crop region
        public float alpha;      //Transparency of user video on the live video. The value range is [0.0, 1.0]. 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque. The default is 1.0
        public int audioRoom;//Not yet realized

    }
```

--------------------------

#### LiveTranscoding.MediaStreamLayout

Layout configuration information of video standard stream in video mixing.

```java
public static class MediaStreamLayout {

        public int layoutX = 0;        //Media's location x in video mixing canvas
        public int layoutY = 0;        //Media's location y in video mixing canvas
        public int layoutW = 0;        //Media's location w in video mixing canvas
        public int layoutH = 0;        //Media's location h in video mixing canvas
        public int zOrder = 0;      //Layer number of the media's video frame on the live video. The value range is the integer in [0, 100], and the minimum value is 0 (default value), indicating that the image in this region is at the lowest level
        public boolean bCrop = true;   //How to crop the source stream when the video mixing service places it in the canvas (0: mend black edge, 1: crop)
        public int cropX = 0;      //X coordinate of crop region
        public int cropY = 0;      //Y coordinate of crop region
        public int cropW = 0;      //Width of crop region
        public int cropH = 0;      //Height of crop region
        public float alpha = 0;      //Transparency of media video on the live video. The value range is [0.0, 1.0]. 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque. The default is 1.0

    }
```

--------------------------
