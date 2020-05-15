# Functional Interface

## Interface List

- 
   ### ThunderEngine

| Function | Function Name |
| ---:| :--- |
| instancetype _Nonnull | [createEngine:sceneId:delegate:](#ThunderEngine::createEngine:sceneId:delegate) |
| void | [destroyEngine](#ThunderEngine::destroyEngine) |
| NSString | [getVersion](#ThunderEngine::getVersion) |
| void | [setSceneId:](#ThunderEngine::setSceneId) |
| void | [setThunderEventDelegate:](#ThunderEngine::setThunderEventDelegate) |
| int | [setArea:](#ThunderEngine::setArea) |
| int | [joinRoom:roomName:uid:](#ThunderEngine::joinRoom:roomName:uid) |
| int | [leaveRoom](#ThunderEngine::leaveRoom) |
| int | [updateToken:](#ThunderEngine::updateToken) |
| int | [setLogFilePath:](#ThunderEngine::setLogFilePath) |
| int | [setLogCallback:](#ThunderEngine::setLogCallback) |
| int | [setLogLevel:](#ThunderEngine::setLogLevel) |
| int | [addPublishOriginStreamUrl](#ThunderEngine::addPublishOriginStreamUrl) |
| int | [removePublishOriginStreamUrl:](#ThunderEngine::removePublishOriginStreamUrl) |
| int | [setLiveTranscodingTask:transcoding:](#ThunderEngine::setLiveTranscodingTask:transcoding) |
| int | [addPublishTranscodingStreamUrl:url:](#ThunderEngine::addPublishTranscodingStreamUrl:url) |
| int | [removePublishTranscodingStreamUrl:url:](#ThunderEngine::removePublishTranscodingStreamUrl:url) |
| int | [removeLiveTranscodingTask:](#ThunderEngine::removeLiveTranscodingTask) |
| int | [addSubscribe:uid:](#ThunderEngine::addSubscribe:uid) |
| int | [removeSubscribe:uid:](#ThunderEngine::removeSubscribe:uid) |
| int | [setMediaMode:](#ThunderEngine::setMediaMode) |
| int | [setRoomMode:](#ThunderEngine::setRoomMode) |
| int | [enableWebSdkCompatibility:](#ThunderEngine::enableWebSdkCompatibility) |
| int | [setVideoEncoderConfig:](#ThunderEngine::setVideoEncoderConfig) |
| int | [setLocalVideoCanvas:](#ThunderEngine::setLocalVideoCanvas) |
| int | [setRemotePlayType:](#ThunderEngine::setRemotePlayType) |
| int | [setMultiVideoViewLayout:](#ThunderEngine::setMultiVideoViewLayout) |
| int | [setRemoteVideoCanvas:](#ThunderEngine::setRemoteVideoCanvas) |
| int | [setLocalCanvasScaleMode:](#ThunderEngine::setLocalCanvasScaleMode) |
| int | [setRemoteCanvasScaleMode:mode:](#ThunderEngine::setRemoteCanvasScaleMode:mode) |
| int | [startVideoPreview](#ThunderEngine::startVideoPreview) |
| int | [stopVideoPreview](#ThunderEngine::stopVideoPreview) |
| int | [enableLocalVideoCapture:](#ThunderEngine::enableLocalVideoCapture) |
| int | [stopLocalVideoStream:](#ThunderEngine::stopLocalVideoStream) |
| int | [stopAllRemoteVideoStreams:](#ThunderEngine::stopAllRemoteVideoStreams) |
| int | [stopRemoteVideoStream:stopped:](#ThunderEngine::stopRemoteVideoStream:stopped) |
| int | [setCustomVideoSource:](#ThunderEngine::setCustomVideoSource:) |
| int | [setVideoWatermark:](#ThunderEngine::setVideoWatermark) |
| int | [registerVideoDecodeFrameObserver:uid:](#ThunderEngine::registerVideoDecodeFrameObserver:uid) |
| int | [registerVideoCaptureFrameObserver:](#ThunderEngine::registerVideoCaptureFrameObserver) |
| int | [switchFrontCamera:](#ThunderEngine::switchFrontCamera) |
| int | [setVideoCaptureOrientation:](#ThunderEngine::setVideoCaptureOrientation) |
| int | [setLocalVideoMirrorMode:](#ThunderEngine::setLocalVideoMirrorMode) |
| int | [enableLoudspeaker:](#ThunderEngine::enableLoudspeaker:) |
| BOOL | [isLoudspeakerEnabled](#ThunderEngine::isLoudspeakerEnabled) |
| int | [setAudioConfig:commutMode:scenarioMode:](#ThunderEngine::setAudioConfig:commutMode:scenarioMode) |
| int | [setAudioVolumeIndication:moreThanThd:lessThanThd:smooth:](#ThunderEngine::setAudioVolumeIndication:moreThanThd:lessThanThd:smooth:) |
| int | [enableCaptureVolumeIndication:moreThanThd:lessThanThd:smooth:](#ThunderEngine::enableCaptureVolumeIndication:moreThanThd:lessThanThd:smooth:) |
| int | [stopLocalAudioStream:](#ThunderEngine::stopLocalAudioStream:) |
| int | [stopAllRemoteAudioStreams:](#ThunderEngine::stopAllRemoteAudioStreams:) |
| int | [stopRemoteAudioStream:stopped:](#ThunderEngine::stopRemoteAudioStream:stopped:) |
| int | [setLoudSpeakerVolume:](#ThunderEngine::setLoudSpeakerVolume:) |
| int | [setMicVolume:](#ThunderEngine::setMicVolume:) |
| int | [setPlayVolume:volume:](#ThunderEngine::setPlayVolume:volume:) |
| nullable [ThunderAudioFilePlayer](#ThunderAudioFilePlayer)* | [createAudioFilePlayer](#ThunderEngine::createAudioFilePlayer) |
| void | [destroyAudioFilePlayer:](#ThunderEngine::destroyAudioFilePlayer:) |
| int | [setEnableInEarMonitor:](#ThunderEngine::setEnableInEarMonitor:) |
| int | [setEnableEqualizer:](#ThunderEngine::setEnableEqualizer:) |
| int | [setEqGains:](#ThunderEngine::setEqGains:) |
| int | [setEnableReverb:](#ThunderEngine::setEnableReverb:) |
| int | [setReverbParam:](#ThunderEngine::setReverbParam:) |
| int | [setEnableCompressor:](#ThunderEngine::setEnableCompressor:) |
| int | [setCompressorParam:](#ThunderEngine::setCompressorParam:) |
| int | [setEnableLimiter:](#ThunderEngine::setEnableLimiter:) |
| int | [setLimiterParam:](#ThunderEngine::setLimiterParam:) |
| void | [enableAudioDataIndication:](#ThunderEngine::enableAudioDataIndication:) |
| void | [setAudioSourceType:](#ThunderEngine::setAudioSourceType:) |
| void | [enableAudioPlaySpectrum:](#ThunderEngine::enableAudioPlaySpectrum:) |
| void | [setAudioPlaySpectrumInfo:notifyIntervalMS:](#ThunderEngine::setAudioPlaySpectrumInfo:notifyIntervalMS:) |
| int | [sendUserAppMsgData:](#ThunderEngine::sendUserAppMsgData:) |
| int | [sendMediaExtraInfo:](#ThunderEngine::sendMediaExtraInfo:) |
| int | [setMediaExtraInfoDelegate:](#ThunderEngine::setMediaExtraInfoDelegate:) |
| int | [enableMixVideoExtraInfo:](#ThunderEngine::enableMixVideoExtraInfo:) |
| BOOL | [startAudioSaver:saverMode:fileMode:](#ThunderEngine::startAudioSaver:saverMode:fileMode:) |
| BOOL | [stopAudioSaver](#ThunderEngine::stopAudioSaver) |
| void | [setSoundEffect:](#ThunderEngine::setSoundEffect:) |
| void | [setVoiceChanger:](#ThunderEngine::setVoiceChanger:) |
| int | [setRecordingAudioFrameParameters:channel:mode:samplesPerCall:](#ThunderEngine::setRecordingAudioFrameParameters:channel:mode:samplesPerCall:) |
| int | [setPlaybackAudioFrameParameters:channel:mode:samplesPerCall:](#ThunderEngine::setPlaybackAudioFrameParameters:channel:mode:samplesPerCall:) |
| void | [enableCustomAudioSource:channelsPerFrame:](#ThunderEngine::enableCustomAudioSource:channelsPerFrame:) |
| void | [disableCustomAudioSource](#ThunderEngine::disableCustomAudioSource) |
| BOOL | [pushCustomAudioRawData:samples:timestamp:](#ThunderEngine::pushCustomAudioRawData:samples:timestamp:) |
| BOOL | [pushCustomAudioSampleBuffer:](#ThunderEngine::pushCustomAudioSampleBuffer:) |
| int | [enableVoicePosition:](#ThunderEngine::enableVoicePosition:) |
| int | [setRemoteUidVoicePosition:azimuth:gain:](#ThunderEngine::setRemoteUidVoicePosition:azimuth:gain:) |

- ### ThunderVideoFrameConsumer

| Function | Function Name |
| ---:| :--- |
| void | [consumePixelBuffer:withTimestamp:rotation:](#ThunderVideoFrameConsumer::consumePixelBuffer:withTimestamp:rotation) |
| void | [consumeRawData:withTimestamp:format:size:rotation:](#ThunderVideoFrameConsumer::consumeRawData:withTimestamp:format:size:rotation) |
| void | [consumeCMSampleBuffer:](#ThunderVideoFrameConsumer::consumeCMSampleBuffer) |

- ### ThunderAudioFilePlayer

| Function | Function Name |
| ---:| :--- |
| void | [setPlayerDelegate:](#ThunderAudioFilePlayer::setPlayerDelegate) |
| void | [open:](#ThunderAudioFilePlayer::open) |
| void | [close](#ThunderAudioFilePlayer::close) |
| void | [play](#ThunderAudioFilePlayer::play) |
| void | [Stop](#ThunderAudioFilePlayer::stop) |
| void | [pause](#ThunderAudioFilePlayer::pause) |
| void | [resume](#ThunderAudioFilePlayer::resume) |
| void | [seek:](#ThunderAudioFilePlayer::seek) |
| uint32_t | [getTotalPlayTimeMS](#ThunderAudioFilePlayer::getTotalPlayTimeMS) |
| uint32_t | [getCurrentPlayTimeMS](#ThunderAudioFilePlayer::getCurrentPlayTimeMS) |
| void | [setPlayVolume:](#ThunderAudioFilePlayer::setPlayVolume) |
| int | [setPlayerLocalVolume](#ThunderAudioFilePlayer::setPlayerLocalVolume) |
| int | [setPlayerPublishVolume](#ThunderAudioFilePlayer::setPlayerPublishVolume) |
| int | [getPlayerLocalVolume](#ThunderAudioFilePlayer::getPlayerLocalVolume) |
| int | [getPlayerPublishVolume](#ThunderAudioFilePlayer::getPlayerPublishVolume) |
| void | [setSemitone:](#ThunderAudioFilePlayer::setSemitone) |
| int | [setLooping:](#ThunderAudioFilePlayer::setLooping) |
| int | [selectAudioTrack:](#ThunderAudioFilePlayer::selectAudioTrack) |
| int | [getAudioTrackCount](#ThunderAudioFilePlayer::getAudioTrackCount) |
| void | [enablePublish:](#ThunderAudioFilePlayer::enablePublish) |
| void | [enableSpectrum:](#ThunderAudioFilePlayer::enableSpectrum) |
| void | [enableVolumeIndication:interval:](#ThunderAudioFilePlayer::enableVolumeIndication:interval) |
| void | [setMixStandard:](#ThunderAudioFilePlayer::setMixStandard) |
| BOOL | [isMixStandard](#ThunderAudioFilePlayer::isMixStandard) |
| int | [getCurrentSpectrum:len:](#ThunderAudioFilePlayer::getCurrentSpectrum:len) |

- 
   ### IMediaEngine

| Function | Function Name |
| ---:| :--- |
| bool | [registerAudioFrameObserver](#IMediaEngine::registerAudioFrameObserver) |

## activity operation

### ThunderEngine

#### ThunderEngine::createEngine:sceneId:delegate:

```objc
+ (instancetype _Nonnull)createEngine:(NSString * _Nonnull)appId
                              sceneId:(NSInteger)sceneId
                             delegate:(id<ThunderEventDelegate> _Nullable)delegate;
```

Create ThunderEngine and initialize ThunderEngine instance.

> **Note:**
>
> - Currently, SDK only supports one ThunderEngine instance and each application only creates one ThunderEngine object.
> - Unless otherwise specified, all interface functions of ThunderEngine are asynchronously called, and the interface is called in the same thread.
> - Users of the same AppId can communicate with each other.
> - SceneId is used to differentiate scenes of the same business, contributing to analyze data based on them.

##### Parameter[](#createEngine)

| Parameter | Description |
| :--- | :--- |
| appId | AppId signed for application developers |
| sceneId | The scene Id customized by the developer can subdivide business scenes; it unnecessary, fill 0 |
| delegate | Callback. For details, refer to [ThunderEventDelegate](notification.md#ThunderEventDelegate) |

##### Return[](#createEngine)

- Back to ThunderEngine object

--------------------------

#### ThunderEngine::destroyEngine

```objc
+ (void)destroyEngine;
```

Destroy ThunderEngine instance object

> **Note:**
>
> - This method releases all resources used by SDK.
> - Some applications only operate voice communication required by users. Resources can be released for other operations if they are not needed. This method may be applicable for such applications.
> - As long as [destroyEngine](#ThunderEngine::destroyEngine) is called, the user can no longer use or call back other methods in the SDK.
> - To use the communication function again, [createEngine](#ThunderEngine::createEngine:sceneId:delegate) must be called again to create a ThunderEngine instance.
> - The created file player object [ThunderAudioFilePlayer](#ThunderAudioFilePlayer) will also be released.

--------------------------

#### ThunderEngine::getVersion

```objc
+ (NSString * _Nonnull)getVersion;
```

Acquire the SDK version No.

> **Note:**
>
> - This method returns the string of SDK’s version No.

##### Return[](#getVersion)

- String of SDK’s version No.

--------------------------

#### ThunderEngine::setSceneId:

```objc
- (void)setSceneId:(NSInteger)sceneId;
```

Set scenario id.

##### Parameter[](#setSceneId)

| Parameter | Description |
| :--- |:--- |
| sceneId | The scene Id customized by the developer can subdivide business scenes; it unnecessary, fill 0 |

--------------------------

#### ThunderEngine::setThunderEventDelegate:

```objc
- (void)setThunderEventDelegate:(id<ThunderEventDelegate> _Nullable)delegate;
```

Set proxy interface.

##### Parameter[](#setThunderEventDelegate)

| Parameter | Description |
| :--- |:--- |
| delegate | For proxy interface, refer to[ThunderEventDelegate](notification.md#ThunderEventDelegate) |

--------------------------

#### ThunderEngine::setArea:

```objc
- (int)setArea:(ThunderRtcAreaType)area
```

Set country and area of users.

To accommodate to different laws and regulations at home and abroad, aivacom provides both domestic (by default) and international central systems. Set it by referring to the following points:

- If applications are mainly conducted abroad, this interface shall be called to set abroad area.
- The users in domestic and international central systems cannot communicate with each other. So make ensure that users in the same room shall be in the same system.
- The two systems are deployed globally, supporting global access.

> **Note:**
>
> - [Only call it before the joinRoom](#ThunderEngine::joinRoom:roomName:uid) can be valid. It is necessary for abroad users but not for domestic users.
> - Only the [ThunderRtcAreaType](#ThunderRtcAreaType) options listed in the file can be the parameter options.
> - It can only be reset when [destroyEngine](#ThunderEngine::destroyEngine) is performed.

| Parameter | Description |
| --- | --- |
| area | Region type is domestic by default. See [ThunderRtcAreaType for details](#ThunderRtcAreaType) |

##### Return[](#setArea)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::joinRoom:roomName:uid:

```objc
-(int)joinRoom:(NSString * _Nullable)token
      roomName:(NSString * _Nonnull)roomName
           uid:(NSString * _Nonnull)uid;
```

Join a room.

- This method lets users join the (audio/video) communication room. In the same room, users can communicate with each other, and group chat starts when multiple users join it.
- If during the call, users have to call [leaveRoom](#ThunderEngine::leaveRoom) to leave before joining the next one.

> **Note:**
>
> - Apps using different App IDs are not interoperable.
> - Function returned successfully only means successful implementation of request. Receiving the [onJoinRoomSuccess](notification.md#ThunderEventDelegate::thunderEngine:onJoinRoomSuccess:withUid:elapsed) callback marks successful entry into the room.
> - When appid mode is set for backstage, send a null token.

##### Parameter[](#joinRoom)

| Parameter | Description |
| :--- | :--- |
| token | For authentication, see [Authentication Access Manual for details](https://www.sunclouds.com/cloud/v2/developer/doc.htm?serviceId=103&typeCode=API_DOC&title=%E7%94%A8%E6%88%B7%E9%89%B4%E6%9D%83%E8%AF%B4%E6%98%8E&version=2.0) |
| roomName | Room name (unique for each AppId) only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_ , with the length of not more than 64 bytes. |
| uid | User ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |

##### Return[](#joinRoom)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::leaveRoom

```objc
- (int)leaveRoom;
```

Leaving room indicates hang off or exiting conversation.

> **Note:**
>
> - When [joinRoom](#ThunderEngine::joinRoom:roomName:uid) is called, you have to call [leaveRoom](#ThunderEngine::leaveRoom) to end conversation before starting the next one.
> - No matter whether the user is idle or in a call, [leaveRoom](#ThunderEngine::leaveRoom) can be called, without adverse effects. This method can release all resources related to conversation.

##### Return[](#leaveRoom)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::updateToken:

```objc
- (int)updateToken:(NSString * _Nonnull)token;
```

This method is used to update Token and authenticate service.

> **Note:**
>
> - Suggested token formats are listed below. See [Authentication Access Manual](https://www.sunclouds.com/cloud/v2/developer/doc.htm?serviceId=103&typeCode=API_DOC&title=%E7%94%A8%E6%88%B7%E9%89%B4%E6%9D%83%E8%AF%B4%E6%98%8E&version=2.0) for details.

| uint16 | uint32 | uint64 | uint64 | uint32 | uint16 | nBytes | 20 Bytes |
---|---|---|---|---|---|---|---
| TokenLen | AppId | uid | TimeStamp(ms) | ValidTime(s) | BizExtInfoLen | BizExtInfoData | DigitalSignature |

1. The multi-byte integer uses network byte order, generally Big Endian.
2. TokenLen: the length of the whole token includes its 2 bytes and abstract.
3. Token expiration time=Timestamp+ValidTime*1000, the UTC time in millisecond since 1970.
4. BizExtInfoData: Extension information that may be needed for service authentication is customized by the service.
5. DigitalSignature: Digital signature adopts the hmac-sha1 algorithm to calculate all data before DigitalSignature to get the [TokenLen,BizExtInfoData]. AppSecret distributed in application of appId is used as the key.
6. Token has to be transmitted by http, so the whole Token shall be encoded by url base64. Note that the url encode is not performed for the whole base64.

##### Parameter[](#updateToken)

| Parameter | Description |
| :--- | :--- |
| token | For authentication, see [Authentication Access Manual for details](https://www.sunclouds.com/cloud/v2/developer/doc.htm?serviceId=103&typeCode=API_DOC&title=%E7%94%A8%E6%88%B7%E9%89%B4%E6%9D%83%E8%AF%B4%E6%98%8E&version=2.0) |

##### Return[](#updateToken)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLogFilePath:

```objc
- (int)setLogFilePath:(NSString * _Nonnull)filePath;
```

Set directory for SDK to output log files. A directory with write permissions must be specified.

> **Note:**
>
> - For one of the two methods to output SDK logs, the application specifies the output directory and ensures the directory is writable, and SDK voluntarily exports logs to the directory.
> - Set log callback. When log callback is set, setLogFilePath is invalidated.


##### Parameter[](#setLogFilePath)

| Parameter | Description |
| :--- | :--- |
| filePath | Complete list of log files |

##### Return[](#setLogFilePath)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLogCallback:

```objc
- (int)setLogCallback:(nullable id<ThunderRtcLogDelegate>)delegate
```

Set output of log callback.

> **Note:**
>
> - For one of the two methods to output SDK logs, SDK calls back log messages to the application and the application ghostwrites.
> - After the log callback is set, the setLogFilePath will be invalid.

##### Parameter[](#setLogCallback)

| Parameter | Description |
| :--- | :--- |
| delegate | For log protocol, see [ThunderRtcLogDelegate for details](notification.md#ThunderRtcLogDelegate) |

##### Return[](#setLogCallback)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLogLevel:

```objc
- (int)setLogLevel:(ThunderRtcLogLevel)level;
```

Set filter level of log output.

> **Note:**
>
> - Set filtering level for log output, and call it before setLogFilePath or setLogCallback Without calling this interface, use the default level: THUNDER_LOG_LEVEL_INFO.

##### Parameter[](#setLogLevel)

| Parameter | Description |
| :--- | :--- |
| level | For log level, see [ThunderRtcLogLevel for details](#ThunderRtcLogLevel) |


##### Return[](#setLogLevel)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::addPublishOriginStreamUrl:

```objc
- (int)addPublishOriginStreamUrl:(NSString* _Nonnull)url;
```

Add address for bypass stream publishing of source streams.

> **Note:**
>
> - After this interface is called, the anchor's current audio/video stream will be pushed to the specified CDN address. To update url, first call the [removePublishOriginStreamUrl](#ThunderEngine::removePublishOriginStreamUrl), and add after removing the original address.
> - Only one-channel stream publishing address can be added each time by this method. If multi-channel streams need to be pushed, this method have to be called repeatedly. A maximum of 5 addresses are supported for stream publishing.
> - After playing, the server pushes source stream to corresponding URL. Enter the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid) for callback. Leaving the room[leaveRoom](#ThunderEngine::leaveRoom) will empty the configuration.

##### Parameter[](#addPublishOriginStreamUrl)

| Parameter | Description |
| :--- | :--- |
| url | CDN stream publishing address is in format RTMP. This character features a length of 512 bytes as maximum. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes |

##### Return[](#addPublishOriginStreamUrl)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::removePublishOriginStreamUrl:

```objc
- (int)removePublishOriginStreamUrl:(NSString* _Nonnull)url;
```

Remove address for bypass stream publishing of source streams.

> **Note:**
>
> - After this interface is called, the anchor's current audio/video stream will not be pushed to the specified CDN address.

##### Parameter[](#removePublishOriginStreamUrl)

| Parameter | Description |
| :--- | :--- |
| url | CDN stream publishing address is in format RTMP. This character features a length of 512 bytes as maximum. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes |

##### Return[](#removePublishOriginStreamUrl)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLiveTranscodingTask:transcoding:

```objc
- (int)setLiveTranscodingTask:(NSString* _Nonnull)taskId transcoding:(LiveTranscoding* _Nonnull)transcoding;
```

Add/Update stream mixing task[LiveTranscoding](#LiveTranscoding).

> **Note:**
>
> - After callback of this interface, stream mixing and transcoding task will be started at back stage of aivacom, and all source flows set up will be subjected to the video mixing and audio mixing. The application shall specify the stream mixing ID to differentiate different stream mixing tasks.
> - This interface can be called repeatedly to update stream mixing parameters in the mix process. Multiple stream mixing tasks can be set in the same room.
> - Join the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid) for callback. Leaving the room [leaveRoom](#ThunderEngine::leaveRoom) will empty the configuration.
> - The stream publishing address can be added into the stream mixing and transcoding tasks by [addPublishTranscodingStreamUrl](#ThunderEngine::addPublishTranscodingStreamUrl:url:) interface. The stream mixing and transcoding will be pushed to specified address after operating the stream mixing and transcoding.

##### Parameter[](#setLiveTranscodingTask)

| Parameter | Description |
| :--- | :--- |
| taskId | The stream mixing task ID is generated by the application. It shall be unique in the entire domain |
| transcoding | For information about stream mixing configuration, see [LiveTranscoding](#LiveTranscoding) |

##### Return[](#setLiveTranscodingTask)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::addPublishTranscodingStreamUrl:url:

```objc
- (int)addPublishTranscodingStreamUrl:(NSString* _Nonnull)taskId url:(NSString* _Nonnull)url;
```

Add address for bypass stream publishing of mixed streams.

> **Note:**
>
> - Call this interface after adding transcoding task by calling [setLiveTranscodingTask](#ThunderEngine::setLiveTranscodingTask:transcoding) interface.
> - After this interface is called, the specified stream mixing will be pushed to the specified CDN address. To update url, first call the [removePublishTranscodingStreamUrl](#ThunderEngine::removePublishTranscodingStreamUrl:url:) and add after removing the original address.
> - Add stream publishing address for specified transcoding task, and only one address can added by this method. If multiple-channel streams have to be pushed, call this method repeatedly. 5 stream publishing addresses can be supported at most in the same transcoding task.
> - Join the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid) for callback. Leaving the room [leaveRoom](#ThunderEngine::leaveRoom) will empty the configuration.

##### Parameter[](#addPublishTranscodingStreamUrl)

| Parameter | Description |
| :--- | :--- |
| taskId | Stream mixing task ID |
| url | CDN stream publishing address is in format RTMP. This character features a length of 512 bytes as maximum. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes |

##### Return[](#addPublishTranscodingStreamUrl)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::removePublishTranscodingStreamUrl:url:

```objc
- (int)removePublishTranscodingStreamUrl:(NSString* _Nonnull)taskId url:(NSString* _Nonnull)url;
```

Remove address for bypass stream publishing of mixed streams.
> **Note:**
>
> - After this interface is called, the specified mixed stream will not be pushed to the specified CDN address.
> - Only one-channel stream publishing address can be deleted each time by this method. If multi-channel streams need to be removed, this method have to be called repeatedly.
> - Join the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid) for callback.

##### Parameter[](#removePublishTranscodingStreamUrl)

| Parameter | Description |
| :--- | :--- |
| taskId | Stream mixing task ID |
| url | CDN stream publishing address is in format RTMP. This character features a length of 512 bytes as maximum. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes |

##### Return[](#removePublishTranscodingStreamUrl)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::removeLiveTranscodingTask:

```objc
- (int)removeLiveTranscodingTask:(NSString* _Nonnull)taskId;
```

Remove the stream mixing task.

> **Note:**
>
> - Upon callback of this interface, the stream mixing task will be deleted and stopped at backstage of aivacom, but url added at the [addPublishTranscodingStreamUrl](#ThunderEngine::addPublishTranscodingStreamUrl:url:) interface will not be removed.

##### Parameter[](#removeLiveTranscodingTask)

| Parameter | Description |
| :--- | :--- |
| taskId | The stream mixing task ID is generated by the application. It shall be unique in the entire domain |

##### Return[](#removeLiveTranscodingTask)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::addSubscribe:uid:

```objc
- (int)addSubscribe:(NSString* _Nonnull)roomId uid:(NSString* _Nonnull)uid;
```

Subscribe across the room.
> **Note:**
>
> - Subscribe audio/video stream of other rooms after joining the room. Namely, this function can be called after joining the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid). Leaving the room will empty the configuration.

##### Parameter[](#addSubscribe)

| Parameter | Description |
| :--- | :--- |
| roomId | Room No. |
| uid | User ID |

##### Return[](#addSubscribe)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::removeSubscribe:uid:

```objc
- (int)removeSubscribe:(NSString* _Nonnull)roomId uid:(NSString* _Nonnull)uid;
```

Cancel the trans-room subscription.
> **Note:**
>
> - Call this method to cancel subscription to audio and video stream of other rooms. It functions the opposite of [addSubscribe](#ThunderEngine::addSubscribe:uid:) interface. It also shall join the room[joinRoom](#ThunderEngine::joinRoom:roomName:uid) for callback.

##### Parameter[](#removeSubscribe)

| Parameter | Description |
| :--- | :--- |
| roomId | Room No. |
| uid | User ID |

##### Return[](#removeSubscribe)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setMediaMode:

```objc
- (int)setMediaMode:(ThunderRtcConfig)mode;
```

Set media mode of SDK.
> **Note:**
>
> - Media modes for SDK set by the user include audio and audio/video ones. Callback before joining the room is required, and invalidated after joining the room. In non-callback status, the audio/video mode is by default.

##### Parameter[](#setMediaMode)

| Parameter | Description |
| :--- | :--- |
| mode | For media mode, see [ThunderRtcConfig for details](#ThunderRtcConfig) |

##### Return[](#setMediaMode)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setRoomMode:

```objc
- (int)setRoomMode:(ThunderRtcRoomConfig)mode;
```

Set room scenario mode.

> **Note:**
>
> - This interface is for setting the room scenario mode by user. Live streaming mode is by default upon non-callback. It can be used before and after joining the room.
> - SDK can use different optimization methods by knowing usage scenes of applications (such as communication mode or live mode).

##### Parameter[](#setRoomMode)

| Parameter | Description |
| :--- | :--- |
| mode | For media mode, see [ThunderRtcRoomConfig for details](#ThunderRtcRoomConfig) |

##### Return[](#setRoomMode)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableWebSdkCompatibility:

```objc
- (int)enableWebSdkCompatibility:(BOOL)enabled;
```

Enable/Disable WebSDK compatibility.

> **Note:**
>
> - This method is applicable only to the live streaming scenario.
> - After enabling WebSDK compatibility, encoding B frame is prohibited internally. Because WebSDK cannot normally decode B frame, callback before living is required, which has nothing to do with forward/back channel.
> - Microphone connection is compatible with Web SDK by default, without calling this method.

##### Parameter[](#enableWebSdkCompatibility)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: compatible <br>NO: incompatible <br>Incompatible by default |

##### Return[](#enableWebSdkCompatibility)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setVideoEncoderConfig:

```objc
- (int)setVideoEncoderConfig:(ThunderVideoEncoderConfiguration* _Nonnull)config;
```

Set video encoder’s property.

> **Note:**
>
> - SDK will acquire specific video encoding parameters for video encoding from the configured server in accordance with parameter configuration. If the service entails special parameter demand for video encoding, contact Technical Support for personalized configuration.
> - If the video has been published, update the video encoding parameters. The updated video effect can be seen from local review and remote subscription.

##### Parameter[](#setVideoEncoderConfig)

| Parameter | Description |
| :--- | :--- |
| config | For encoding configuration, see [ThunderVideoEncoderConfiguration for details](#ThunderVideoEncoderConfiguration) |

##### Return[](#setVideoEncoderConfig)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLocalVideoCanvas:

```objc
- (int)setLocalVideoCanvas:(ThunderVideoCanvas *_Nullable)local;
```

Set local view.

> **Note:**
>
> - You can preview and publish without setting this window. You can see locally captured pictures by setting this window.

##### Parameter[](#setLocalVideoCanvas)

| Parameter | Description |
| :--- | :--- |
| local | For specific setting of rendering, see [ThunderVideoCanvas for details](#ThunderVideoCanvas) |

##### Return[](#setLocalVideoCanvas)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setRemotePlayType:

```objc
- (int)setRemotePlayType:(ThunderRtcRemotePlayType)remotePlayType;
```

Set the remote play type.

> **Note:**
>
> - Set the remote view whether multi-person microphone connecting is enabled. Call before entering the channel, after “initialization”.

##### Parameter[](#setRemotePlayType)

| Parameter | Description |
| :--- | :--- |
| remotePlayType | For view display mode, see [ThunderRtcRemotePlayType for details](#ThunderRtcRemotePlayType) |

##### Return[](#setRemotePlayType)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setMultiVideoViewLayout:

```objc
- (int)setMultiVideoViewLayout:(ThunderMultiVideoViewParam* _Nonnull)params;
```

Set multi-person microphone connection layout.

> **Note:**
>
> - For setting the multi-person microphone connection layout, call before entering the channel, after “initialization”.

##### Parameter[](#setMultiVideoViewLayout)

| Parameter | Description |
| :--- | :--- |
| params | For specific microphone connection layout, see [ThunderMultiVideoViewParam for details](#ThunderMultiVideoViewParam) |

##### Return[](#setMultiVideoViewLayout)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setRemoteVideoCanvas:

```objc
- (int)setRemoteVideoCanvas:(ThunderVideoCanvas *_Nonnull)remote;
```

Set remote user’s view.

> **Note:**
>
> - You can subscribe without setting this window. After setting of this window, you can see video view of corresponding user through remote subscription.

##### Parameter[](#setRemoteVideoCanvas)

| Parameter | Description |
| :--- | :--- |
| remote | For specific setting of view, see [ThunderVideoCanvas for details](#ThunderVideoCanvas) |

##### Return[](#setRemoteVideoCanvas)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLocalCanvasScaleMode:

```objc
- (int)setLocalCanvasScaleMode:(ThunderVideoRenderMode)mode;
```

Set local view display mode.

##### Parameter[](#setLocalCanvasScaleMode)

| Parameter | Description |
| :--- | :--- |
| mode | See [ThunderVideoRenderMode for details](#ThunderVideoRenderMode) |

##### Return[](#setLocalCanvasScaleMode)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setRemoteCanvasScaleMode:mode:

```objc
- (int)setRemoteCanvasScaleMode:(NSString* _Nonnull)uid mode:(ThunderVideoRenderMode)mode;
```

Set the remote play type.

##### Parameter[](#setRemoteCanvasScaleMode)

| Parameter | Description |
| :--- | :--- |
| uid | User id |
| mode | See [ThunderVideoRenderMode for details](#ThunderVideoRenderMode) |

##### Return[](#setRemoteCanvasScaleMode)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::startVideoPreview

```objc
- (int)startVideoPreview;
```

Enable video preview.

##### Return[](#startVideoPreview)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopVideoPreview

```objc
- (int)stopVideoPreview;
```

Stop video preview.

> **Note:**
>
> - Closing preview will trigger stop video

##### Return[](#stopVideoPreview)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableLocalVideoCapture:

```objc
- (int)enableLocalVideoCapture:(BOOL)enabled;
```

Enable/Disable local video capture.

##### Parameter[](#enableLocalVideoCapture)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Enable local video capture <br>NO: Close local video capture |

##### Return[](#enableLocalVideoCapture)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopLocalVideoStream:

```objc
- (int)stopLocalVideoStream:(BOOL)stopped;
```

Enable/Disable sending of local video stream.

##### Parameter[](#stopLocalVideoStream)

| Parameter | Description |
| :--- | :--- |
| stopped | YES: Disable sending of local video <br>NO: Enable sending of local video |

##### Return[](#stopLocalVideoStream)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopAllRemoteVideoStreams:

```objc
- (int)stopAllRemoteVideoStreams:(BOOL)stopped;
```

Stop or receive all video streams.

> **Note:**
>
> - After the setting of receiving all (stop=false), all video streams in the room will be subscribed automatically. You can specify one stream of not being subscribed by[stopRemoteVideoStream](#ThunderEngine::stopRemoteVideoStream:stopped).
> - After the setting of receiving nothing (stop=true), all video streams in the room will not be subscribed. You can specify one stream being subscribed by [stopRemoteVideoStream](#ThunderEngine::stopRemoteVideoStream:stopped).
> - This interface has no priority relationship with[stopRemoteVideoStream](#ThunderEngine::stopRemoteVideoStream:stopped), and the interface called later will be valid.

##### Parameter[](#stopAllRemoteVideoStreams)

| Parameter | Description |
| :--- | :--- |
| stopped | YES: Receive none <br>NO: Receive all <br>Receive all by default |

##### Return[](#stopAllRemoteVideoStreams)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopRemoteVideoStream:stopped:

```objc
- (int)stopRemoteVideoStream:(NSString* _Nonnull)uid stopped:(BOOL)stopped;
```

Receive/Stop receiving specified video stream.

> **Note:**
>
> - Upon stopping receiving specified audio stream, you can receive all audio streams via [stopAllRemoteVideoStreams](#ThunderEngine::stopAllRemoteVideoStreams), vice versa. 
>    <br>This interface has no priority relationship with[stopAllRemoteVideoStreams](#ThunderEngine::stopAllRemoteVideoStreams), and the interface called later will be valid.

##### Parameter[](#stopRemoteVideoStream)

| Parameter | Description |
| :--- | :--- |
| uid | User id |
| stopped | YES: Stop receiving remote video stream of specified user <br> NO: Start receiving remote video stream of specified user |

##### Return[](#stopRemoteVideoStream)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setCustomVideoSource:

```objc
- (void)setCustomVideoSource:(id<ThunderCustomVideoSourceProtocol> _Nullable)videoSource;
```

Set customized video source.

> **Note:**
>
> - In real-time communication, aivacom’ SDK usually will enable the default video input device, i.e. the built-in camera, for video pushing. To customize video device, the App can customize an object to realize [ThunderCustomVideoSourceProtocol](notification.md#ThunderCustomVideoSourceProtocol) protocol, and then call this method to add the customized video source to the SDK.

##### Parameter[](#setCustomVideoSource)

| Parameter | Description |
| :--- | :--- |
| videoSource | See [ThunderCustomVideoSourceProtocol for details](notification.md#ThunderCustomVideoSourceProtocol) |

--------------------------

#### ThunderEngine::setVideoWatermark:

```objc
- (int)setVideoWatermark:(ThunderImage *_Nonnull)watermark;
```

Set watermark of local video.

> **Note:**
>
> - Through this method, a PNG picture will be added to local video as a watermark to issue together with the local video.
> - If the size of picture in PNG format is inconsistent with settings in this method, SDK will make it coincident by clipping.
> - Only one watermark can be added into the live video, and the watermark added later will replace the last one.
> - The watermark will rotate with the rotation of screen.

##### Parameter[](#setVideoWatermark)

| Parameter | Description |
| :--- | :--- |
| watermark | Watermark name |

##### Return[](#setVideoWatermark)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::registerVideoDecodeFrameObserver:uid:

```objc
-(int)registerVideoDecodeFrameObserver:(nullable id<ThunderDecodeFrameObserver>)delegate uid:(nonnull NSString*)uid;
```

Customize decoding picture rendering.

##### Parameter[](#registerVideoDecodeFrameObserver)

| Parameter | Description |
| :--- | :--- | :--- |
| delegate | For capture of interface for decoding image, see [ThunderVideoDecodeFrameObserver for details](notification.md#ThunderVideoDecodeFrameObserver) |
| uid | Used to indicate the uid’s video stream to be acquired |

##### Return[](#registerVideoDecodeFrameObserver)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::registerVideoCaptureFrameObserver:

```objc
-(int)registerVideoCaptureFrameObserver:(nullable id<ThunderVideoCaptureObserver>)delegate;
```

Customize the image pre-processing function.

##### Parameter[](#registerVideoCaptureFrameObserver)

| Parameter | Description |
| :--- | :--- |
| delegate | For processing interface for local video frame, see [ThunderVideoCaptureFrameObserver for details](notification.md#ThunderVideoCaptureFrameObserver) |

##### Return[](#registerVideoCaptureFrameObserver)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::switchFrontCamera:

```objc
- (int)switchFrontCamera:(BOOL)bFront;
```

Switch to front/back camera.

> **Note:**
>
> - Upon calling of this method, the user can shift front/rear camera. After [startVideoPreview](#ThunderEngine::startVideoPreview) is started, the calling takes effect. When this method is not called, the engine will start the front camera by default.

##### Parameter[](#switchFrontCamera)

| Parameter | Description |
| :--- |:--- |
| bFront | YES: Enable front camera NO: Enable rear camera |

##### Return[](#switchFrontCamera)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setVideoCaptureOrientation:

```objc
- (int)setVideoCaptureOrientation:(ThunderVideoCaptureOrientation)orientation;
```

Set portrait and landscape.

> **Note:**
>
> - The user can call this method to set portrait and landscape. It can be called either before preview[startVideoPreview](#ThunderEngine::startVideoPreview), or during the publishing. If this method is not called, the portrait orientation is applied by default.

##### Parameter[](#setVideoCaptureOrientation)

| Parameter | Description |
| :--- | :--- |
| orientation | For portrait and landscape, see [ThunderVideoCaptureOrientation for details](#ThunderVideoCaptureOrientation) |

##### Return[](#setVideoCaptureOrientation)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLocalVideoMirrorMode:

```objc
- (int)setLocalVideoMirrorMode:(ThunderVideoMirrorMode)mode;
```

Setting camera mirroring.

> **Note:**
>
> - The user can call this method to set local video mirror mode. It can be called either before preview[startVideoPreview](#ThunderEngine::startVideoPreview), or during the publishing.
> - It only functions for front camera, not for rear camera.
> - Neither preview nor stream publishing of a rear camera is mirrored. For a front camera, preview is mirrored and stream publishing is not mirrored by default.

##### Parameter[](#setLocalVideoMirrorMode)

| Parameter | Description |
| :--- | :--- |
| mode | For the mirror mode, see [ThunderVideoMirrorMode](#ThunderVideoMirrorMode) |

##### Return[](#setLocalVideoMirrorMode)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableLoudspeaker:

```objc
- (int)enableLoudspeaker:(BOOL)enableSpeaker;
```

Enable/Disable loudspeaker.

> **Note:**
>
> - This method forces the voice routing to loudspeaker.

##### Parameter[](#enableLoudspeaker)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Play with loudspeaker<br> NO: Play with receiver |

##### Return[](#enableLoudspeaker)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::isLoudspeakerEnabled

```objc
- (BOOL)isLoudspeakerEnabled;
```

Query the enabled status of loudspeaker.

##### Return[](#isLoudspeakerEnabled)

- YES: Indicates output to loudspeaker
- NO: Indicates output to non-loudspeaker (receiver, earphone, etc.)

--------------------------

#### ThunderEngine::setAudioConfig:commutMode:scenarioMode:

```objc
- (int)setAudioConfig:(ThunderRtcAudioConfig)config
           commutMode:(ThunderRtcCommutMode)commutMode
         scenarioMode:(ThunderRtcScenarioMode)scenarioMode;
```

Set audio profiles.

> **Note:**
>
> - This method is used to set the audio parameters and application scenarios.

##### Parameter[](#setAudioConfig)

| Parameter | Description |
| :--- | :--- |
| config | See [ThunderRtcAudioConfig for details](#ThunderRtcAudioConfig) |
| commuMode | For setting of interaction mode, see [ThunderRtcCommutMode for details](#ThunderRtcCommutMode) |
| scenarioMode | For setting of scenario mode, see [ThunderRtcScenarioMode for details](#ThunderRtcScenarioMode) |

##### Return[](#setAudioConfig)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setAudioVolumeIndication:moreThanThd:lessThanThd:smooth

```objc
- (int)setAudioVolumeIndication:(NSInteger)interval
                    moreThanThd:(NSInteger)moreThanThd
                    lessThanThd:(NSInteger)lessThanThd
                         smooth:(NSInteger)smooth;
```

Enable volume indication for speaker.

> **Note:**
>
> - By using this method, SDK can feed current speaker and speaker’s volume back to an application periodically.
> - Return via [onPlayVolumeIndication](notification.md#ThunderEventDelegate::onPlayVolumeIndication:totalVolume) callback interface.
> - The voice volume collected by local microphone or playing file is not included.

##### Parameter[](#setAudioVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| interval | Callback interval =0 by default<br> <=0, The volume prompt is disabled,<br> >0, Callback interval (unit: millisecond) |
| moreThanThd | From >= moreThanThd to < moreThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| lessThanThd | From >= lessThanThd to < lessThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| smooth | Invalid momentarily |

##### Return[](#setAudioVolumeIndication)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableCaptureVolumeIndication:moreThanThd:lessThanThd:smooth:

```objc
- (int)enableCaptureVolumeIndication:(NSInteger)interval
                         moreThanThd:(NSInteger)moreThanThd
                         lessThanThd:(NSInteger)lessThanThd
                              smooth:(NSInteger)smooth;
```

Enable/Disable collected volume callback.

> **Note:**
>
> - By using this method, SDK can feed current microphone capture volume back to an application periodically.
> - Return from [onCaptureVolumeIndication](notification.md#ThunderEventDelegate::thunderEngine:onCaptureVolumeIndication:cpt:micVolume).

##### Parameter[](#enableCaptureVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| interval | Callback interval;<br> <=0, The volume prompt is disabled,<br> >0, Callback interval (unit: millisecond), <br>which is =0 by default |
| moreThanThd | From >= moreThanThd to < moreThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| lessThanThd | From >= lessThanThd to < lessThanThd, immediately call back once (is not restricted by interval) <br><= 0 invalid, default =0 |
| smooth | Invalid momentarily |

##### Return[](#enableCaptureVolumeIndication)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopLocalAudioStream:

```objc
- (int)stopLocalAudioStream:(BOOL)stopped;
```

Enabling/Disabling sending of local audio.

> **Note:**
>
> - This method is used to enable/disable sending local audio stream to the network.
> - Call this method after successful [joinRoom](#ThunderEngine::joinRoom:roomName:uid)

##### Parameter[](#stopLocalAudioStream)

| Parameter | Description |
| :--- | :--- |
| stopped | YES: Disable sending of local audio <br>NO: Enable sending of local audio |

##### Return[](#stopLocalAudioStream)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopAllRemoteAudioStreams:

```objc
- (int)stopAllRemoteAudioStreams:(BOOL)stopped;
```

Stop or receive all audio streams.

> **Note:**
>
> - Upon setting of receiving all (stop=NO), all audio streams in the room will be automatically subscribed. Afterwards, you can specify a stream not to be subscribed via [stopRemoteAudioStream](#ThunderEngine::stopRemoteAudioStream:stopped:).
> - Upon setting of receiving none (stop=YES), none audio streams in the room will be subscribed. Afterwards, you can specify a stream to be subscribed via [stopRemoteAudioStream](#ThunderEngine::stopRemoteAudioStream:stopped:).
> - This interface has no priority relationship with [stopRemoteAudioStream](#ThunderEngine::stopRemoteAudioStream:stopped:), and the interface called later will be valid.

##### Parameter[](#stopAllRemoteAudioStreams)

| Parameter | Description |
| :--- | :--- |
| stopped | YES: Receive none <br>NO: Receive all <br>Receive all by default |

##### Return[](#stopAllRemoteAudioStreams)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::stopRemoteAudioStream:stopped:

```objc
- (int)stopRemoteAudioStream:(nonnull NSString*)uid stopped:(BOOL)stopped;
```

Receive/Stop receiving specified audio stream.

> **Note:**
>
> - Upon stopping receiving specified audio stream, you can receive all audio streams via [stopAllRemoteAudioStreams](#ThunderEngine::stopAllRemoteAudioStreams), vice versa.
> - This interface has no priority relationship with [stopAllRemoteAudioStreams](#ThunderEngine::stopAllRemoteAudioStreams), and the interface called later will be valid.

##### Parameter[](#stopRemoteAudioStream)

| Parameter | Description |
| :--- | :--- |
| uid | User id |
| stopped | YES: Stop receiving remote audio stream of specified user <br>NO: Start receiving remote audio stream of specified user |

##### Return[](#stopRemoteAudioStream)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLoudSpeakerVolume:

```objc
- (int)setLoudSpeakerVolume:(NSInteger)volume;
```

Set loudspeaker volume.

##### Parameter[](#setLoudSpeakerVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Volume value [0-400] |

##### Return[](#setLoudSpeakerVolume)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setMicVolume:

```objc
- (int)setMicVolume:(NSInteger)volume;
```

Set microphone volume.

##### Parameter[](#setMicVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Volume value [0-400] |

##### Return[](#setMicVolume)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setPlayVolume:volume:

```objc
- (int)setPlayVolume:(nonnull NSString*)uid volume:(NSInteger)volume;
```

Set play volume for a single user.

##### Parameter[](#setPlayVolume:volume:)

| Parameter | Description |
| :--- | :--- |
| uid | Specified User ID |
| volume | Volume value [0-400] |

##### Return[](#setPlayVolume:volume:)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::createAudioFilePlayer

```objc
- (nullable ThunderAudioFilePlayer*)createAudioFilePlayer;
```

Create audio file player. See [ThunderAudioFilePlayer for details](#ThunderAudioFilePlayer)

--------------------------

#### ThunderEngine::destroyAudioFilePlayer:

```objc
- (void)destroyAudioFilePlayer:(nonnull ThunderAudioFilePlayer*)filePlayer;
```

Destroy audio file player.

##### Parameter[](#destroyAudioFilePlayer)

| Parameter | Description |
| :--- | :--- |
| filePlayer | For file player, see [ThunderAudioFilePlayer for details](#ThunderAudioFilePlayer) |

--------------------------

#### ThunderEngine::setEnableInEarMonitor:

```objc
- (int)setEnableInEarMonitor:(BOOL)enabled;
```

Enable/Disable in-ear monitor.

##### Parameter[](#setEnableInEarMonitor)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open<br> NO: Close |

##### Return[](#setEnableInEarMonitor)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setEnableEqualizer:

```objc
- (int)setEnableEqualizer:(BOOL)enabled;
```

Enable/Disable local voice equalizer.

##### Parameter[](#setEnableEqualizer)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open <br>NO: Close |

##### Return[](#setEnableEqualizer)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setEqGains:

```objc
- (int)setEqGains:(const _Nonnull ThunderEqGainsOc)gains;
```

Set equalizer parameters.

##### Parameter[](#setEqGains)

| Parameter | Description |
| :--- | :--- |
| gains | For parameters of an equalizer, see [ThunderEqGainsOc for details](#ThunderEqGainsOc) |

##### Return[](#setEqGains)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setEnableReverb:

```objc
- (int)setEnableReverb:(BOOL)enabled;
```

Enable/Disable local sound reverberation.

##### Parameter[](#setEnableReverb)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open<br> NO: Close |

##### Return[](#setEnableReverb)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setReverbParam:

```objc
- (int)setReverbParam:(ThunderReverbExParamOc)reverbParam;
```

Set reverb parameters.

##### Parameter[](#setReverbParam)

| Parameter | Description |
| :--- | :--- |
| reverbParam | For reverb parameters, see [ThunderReverbExParamOc for details](#ThunderReverbExParamOc) |

##### Return[](#setReverbParam)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setEnableCompressor:

```objc
- (int)setEnableCompressor:(BOOL)enabled;
```

Enable/Disable sound compressor.

##### Parameter[](#setEnableCompressor)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open<br> NO: Close |

##### Return[](#setEnableCompressor)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setCompressorParam:

```objc
- (int)setCompressorParam:(ThunderCprParamOc)parameter;
```

Set compressor parameters.

##### Parameter[](#setCompressorParam)

| Parameter | Description |
| :--- | :--- |
| parameter | For compressor parameters, see [ThunderCprParamOc for details](#ThunderCprParamOc) |

##### Return[](#setCompressorParam)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setEnableLimiter:

```objc
- (int)setEnableLimiter:(BOOL)enabled;
```

Enable/Disable pressure limiter.

##### Parameter[](#setEnableLimiter)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open<br>NO: Close<br> |

##### Return[](#setEnableLimiter)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setLimiterParam:

```objc
- (int)setLimiterParam:(ThunderLimiterParamOc)parameter;
```

Set pressure limiter parameters.

##### Parameter[](#setLimiterParam)

| Parameter | Description |
| :--- | :--- |
| parameter | For pressure limiter parameters, see [ThunderLimiterParamOc for details](#ThunderLimiterParamOc) |

##### Return[](#setLimiterParam)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableAudioDataIndication:

```objc
- (void)enableAudioDataIndication:(BOOL)enabled
```

Enable/Disable data callback on audio playing.

> **Note:**
>
> - When enabled, it will call back via [onAudioPlayData](notification.md#ThunderEventDelegate::thunderEngine:onAudioPlayData:duration:cpt:pts:data:) function.

##### Parameter[](#enableAudioDataIndication)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open <br>NO: Close |

--------------------------

#### ThunderEngine::setAudioSourceType:

```objc
- (void)setAudioSourceType:(ThunderSourceType)sourceType;
```

Set audio publishing mode.

##### Parameter[](#setAudioSourceType)

| Parameter | Description |
| :--- | :--- |
| sourceType | For audio publishing type, see [ThunderSourceType for details](#ThunderSourceType) |

--------------------------

#### ThunderEngine::enableAudioPlaySpectrum:

```objc
- (void)enableAudioPlaySpectrum:(Boolean)enable;
```

Enable/Disable data callback on audio play spectrum.

##### Parameter[](#enableAudioPlaySpectrum)

| Parameter | Description |
| :--- | :--- |
| enable | YES: Open NO: Close<br> |

--------------------------

#### ThunderEngine::setAudioPlaySpectrumInfo:notifyIntervalMS:

```objc
- (void)setAudioPlaySpectrumInfo:(UInt32)spectrumLen notifyIntervalMS:(UInt32)notifyIntervalMS;
```

Set audio play spectrum information.

##### Parameter[](#setAudioPlaySpectrumInfo)

| Parameter | Description |
| :--- | :--- |
| spectrumLen | Spectrum length, scope: 12-256, 256 by default |
| notifyIntervalMS | Callback interval (unit: millisecond) of spectrum information must be multiples of 10, which is 30MS by default |

--------------------------

#### ThunderEngine::sendUserAppMsgData:

```objc
- (int)sendUserAppMsgData:(NSData * _Nonnull)msgData
```

Send custom broadcast message of service.

> **Note:**
>
> - Send user app message data in the room. This interface sends messages via media UDP channel with features of low-lantency and unreliability. Specified constraints are as follows:
> - 1. Sender must enter the room.
> - 2. Call when microphone is opened successfully (unavailable for pure audience or upon failure of live authentication).
> - 3. Calling frequency of this interface not to exceed twice a second, size of msgData of 200Byte as maximum.
> - 4. Failing to meet any of the said conditions, msg will be discarded.
> - 5. Not guaranteed to send to all online users in the room, or send by order.
> - For user app message data sent by other users, call back to the application via [onRecvUserAppMsgData](notification.md#ThunderEventDelegate::thunderEngine:onRecvUserAppMsgData:uid) callback interface.
> - Acquire reasons of failing to send the msg via callback interface [onSendAppMsgDataFailedStatus](notification.md#ThunderEventDelegate::thunderEngine:onSendAppMsgDataFailedStatus).

##### Parameter[](#sendUserAppMsgData)

| Parameter | Description |
| :--- | :--- |
| msgData | Message sent |

##### Return[](#sendUserAppMsgData)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::sendMediaExtraInfo:

```objc
- (int)sendMediaExtraInfo:(NSData * _Nonnull)data;
```

Send media extra information. Use video channel when uploading video, otherwise use audio channel.

> **Note:**
>
> - The sender must join the room, and call it after successfully publishing audio.
> - The fastest call frequency is 100 ms one time in audio publishing (publishing in a pure audio mode or only audio publishing in an audio/video mode). If video is also published at audio/video mode, the call frequency shall not exceed the frame rate. Suppose the stream publishing is conducted at the frame rate of 15fps by default, namely, the call frequency does not exceed 1000/15=66.7 ms/time
> - The size of media extra information shall not exceed 200 bytes in audio publishing (publishing in a pure audio mode or only audio publishing in an audio/video mode). If video is also published at audio/video mode, the size of extra information shall not exceed 2048 bytes.
> - Packet loss may occur

> - Acquire reasons for failure to send media extra information via [onSendMediaExtraInfoFailedStatus](notification.md#ThunderMediaExtraInfoDelegate::onSendMediaExtraInfoFailedStatus:) under proxy of ThunderMediaExtraInfoDelegate.
> - Media extra information sent by other users is called back to the application via [onRecvMediaExtraInfo](notification.md#ThunderMediaExtraInfoDelegate::onRecvMediaExtraInfo:ofUid) under proxy of ThunderMediaExtraInfoDelegate.

##### Parameter[](#sendMediaExtraInfo)

| Parameter | Description |
| :--- | :--- |
| Date | Media extra information data to be transmitted |

##### Return[](#sendMediaExtraInfo)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setMediaExtraInfoDelegate:

```objc
- (int)setMediaExtraInfoDelegate:(nullable id<ThunderMediaExtraInfoDelegate>)delegate;
```

Set callback monitoring of media extra information.

##### Parameter[](#setMediaExtraInfoDelegate)

| Parameter | Description |
| :--- | :--- |
| delegate | See [ThunderMediaExtraInfoDelegate for details](notification.md#ThunderMediaExtraInfoDelegate) |

##### Return[](#setMediaExtraInfoDelegate)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableMixVideoExtraInfo:

```objc
- (int)enableMixVideoExtraInfo:(BOOL)enable;
```

Enable/Disable mixed video with extra information. For example: Mixed video with layout information.

When enabled, you can receive [onRecvMixVideoInfo](notification.md#ThunderMediaExtraInfoDelegate::onRecvMixVideoInfo:ofUid) callback during playing of mixed video stream at audience end

##### Parameter[](#enableMixVideoExtraInfo)

| Parameter | Description |
| :--- | :--- |
| enable | Whether to enable mixed video with media extra information. <br>YES: Enable <br>NO: Close |

##### Return[](#enableMixVideoExtraInfo)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::startAudioSaver:saverMode:fileMode:

```objc
- (BOOL)startAudioSaver:(NSString* _Nonnull)fileName saverMode:(ThunderSaverMode)saverMode fileMode:(ThunderFileMode)fileMode
```

Start saving audio data in aac format.

##### Parameter[](#startAudioSaver)

| Parameter | Description |
| :--- | :--- |
| fileName | Absolute path of the file, containing file name, suffixed with .aac |
| saverMode | For save mode, see [ThunderSaverMode for details](#ThunderSaverMode) |
| fileMode | For write data mode, see [ThunderFileMode for details](#ThunderFileMode) |

##### Return[](#startAudioSaver)

- YES: Success
- NO: Failure

--------------------------

#### ThunderEngine::stopAudioSaver

```objc
- (BOOL)stopAudioSaver
```

Stop saving audio files in acc format.

##### Return[](#stopAudioSaver)

- YES: Success
- NO: Failure

--------------------------

#### ThunderEngine::setSoundEffect:

```objc
-(void)setSoundEffect:(NSInteger)mode
```

Set sound effect mode.

##### Parameter[](#setSoundEffect)

| Parameter | Description |
| :--- | :--- |
| mode | Audio saving mode THUNDER_SOUND_EFFECT_MODE_NONE(0)：Close mode <br>THUNDER_SOUND_EFFECT_MODE_VALLEY(1): VALLEY mode <br>THUNDER_SOUND_EFFECT_MODE_RANDB(2)：R&B mode <br>THUNDER_SOUND_EFFECT_MODE_KTV(3)：KTV mode <br>THUNDER_SOUND_EFFECT_MODE_CHARMING(4)：CHARMING mode <br>THUNDER_SOUND_EFFECT_MODE_POP(5): Pop mode <br>THUNDER_SOUND_EFFECT_MODE_HIPHOP(6): Hiphop mode <br>THUNDER_SOUND_EFFECT_MODE_ROCK(7): Rock mode <br>THUNDER_SOUND_EFFECT_MODE_CONCERT(8): Concert mode <br>THUNDER_SOUND_EFFECT_MODE_STUDIO(9): Studio mode |

--------------------------

#### ThunderEngine::setVoiceChanger:

```objc
- (void)setVoiceChanger:(int32_t)mode;
```

Set voice change mode.

##### Parameter[](#setVoiceChanger)

| Parameter | Description |
| :--- | :--- |
| mode | Audio saving mode THUNDER_SOUND_EFFECT_MODE_NONE(0)：Close mode <br>THUNDER_SOUND_EFFECT_MODE_VALLEY(1): VALLEY mode <br>THUNDER_SOUND_EFFECT_MODE_RANDB(2)：R&B mode <br>THUNDER_SOUND_EFFECT_MODE_KTV(3)：KTV mode <br>THUNDER_SOUND_EFFECT_MODE_CHARMING(4)：CHARMING mode <br>THUNDER_SOUND_EFFECT_MODE_POP(5): Pop mode <br>THUNDER_SOUND_EFFECT_MODE_HIPHOP(6): Hiphop mode <br>THUNDER_SOUND_EFFECT_MODE_ROCK(7): Rock mode <br>THUNDER_SOUND_EFFECT_MODE_CONCERT(8): Concert mode <br>THUNDER_SOUND_EFFECT_MODE_STUDIO(9): Studio mode |

--------------------------

#### ThunderEngine::setRecordingAudioFrameParameters:channel:mode:samplesPerCall:

```objc
- (int)setRecordingAudioFrameParameters:(NSInteger)sampleRate
                                channel:(NSInteger)channel
                                   mode:(ThunderAudioRawFrameOperationMode)mode
                         samplesPerCall:(NSInteger)samplesPerCall;
```

Set format of recording audio.

##### Parameter[](#setRecordingAudioFrameParameters)

| Parameter | Description |
| :--- | :--- |
| sampleRate | Sampling rate |
| channel | Audio track; 1: Single track; 2: dual track |
| mode | For use mode of onRecordAudioFrame, see [ThunderAudioRawFrameOperationMode for details](#ThunderAudioRawFrameOperationMode) |
| samplesPerCall | Specify sampling point number for data return in onRecordAudioFrame, e.g. 1024 in transcoding publish stream. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setRecordingAudioFrameParameters)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setPlaybackAudioFrameParameters:channel:mode:samplesPerCall:

```objc
- (int)setPlaybackAudioFrameParameters:(NSInteger)sampleRate
                               channel:(NSInteger)channel
                                  mode:(ThunderAudioRawFrameOperationMode)mode
                        samplesPerCall:(NSInteger)samplesPerCall;
```

Set format of playing audio.

##### Parameter[](#setPlaybackAudioFrameParameters)

| Parameter | Description |
| :--- | :--- |
| sampleRate | Sampling rate |
| channel | Audio track; 1: Single track; 2: dual track |
| mode | For use mode of onRecordAudioFrame, see [ThunderAudioRawFrameOperationMode for details](#ThunderAudioRawFrameOperationMode) |
| samplesPerCall | Specify sampling point number for data return in onRecordAudioFrame, e.g. 1024 in transcoding publish stream. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setPlaybackAudioFrameParameters)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::enableCustomAudioSource:channelsPerFrame:

```objc
- (void)enableCustomAudioSource:(NSUInteger)sampleRate channelsPerFrame:(NSUInteger)channelsPerFrame;
```

Set parameters for external audio capture.

> **Note:**
>
> - Call this interface before playing the audio.

##### Parameter[](#enableCustomAudioSource)

| Parameter | Description |
| :--- | :--- |
| sampleRate | The sampling rate of external audio source can be 8000, 16000, 32000, 44100 or 48000 |
| channelsPerFrame | Number of channels for external audio source (support two at most) |

--------------------------

#### ThunderEngine::disableCustomAudioSource

```objc
- (void)disableCustomAudioSource;
```

Disable external audio sampling parameters.

> **Note:**
>
> - Call this interface after disabling the audio playing.

--------------------------

#### ThunderEngine::pushCustomAudioRawData:samples:timestamp:

```objc
- (BOOL)pushCustomAudioRawData:(void *_Nonnull)data samples:(NSUInteger)samples timestamp:(NSTimeInterval)timestamp;
```

Push external audio stream.

##### Parameter[](#pushCustomAudioRawData)

| Parameter | Description |
| :--- | :--- |
| Date | External audio data |
| samples | Sample quantity of corresponding audio data |
| timeStamp | Timestamp of external audio data is used for synchronization with external video source |

##### Return[](#pushCustomAudioRawData)

- YES Method called successfully
- NO Method calling failed

--------------------------

#### ThunderEngine::pushCustomAudioSampleBuffer:

```objc
- (BOOL)pushCustomAudioSampleBuffer:(CMSampleBufferRef _Nonnull)sampleBuffer;
```

Push external audio frame.

##### Parameter[](#pushCustomAudioSampleBuffer)

| Parameter | Description |
| :--- | :--- |
| sampleBuffer | External audio frame |

##### Return[](#pushCustomAudioSampleBuffer)

- YES Method called successfully
- NO Method calling failed

--------------------------

#### ThunderEngine::enableVoicePosition:

```objc
- (int)enableVoicePosition:(BOOL)enabled;
```

Enable/Disable voice stereo of remote users.

> **Note:**
>
> - Make sure to call this method before calling the [joinRoom](#ThunderEngine::joinRoom:roomName:uid) method.

##### Parameter[](#enableVoicePosition)

| Parameter | Description |
| :--- | :--- |
| enabled | YES: Open <br>NO: Close |

##### Return[](#enableVoicePosition)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderEngine::setRemoteUidVoicePosition:azimuth:gain:

```objc
- (int)setRemoteUidVoicePosition(nonnull NSString*)uid azimuth:(NSInteger)azimuth gain:(NSInteger)gain
```

Set spatial location and volume of remote user's voice.

##### Parameter[](#setRemoteUidVoicePosition)

| Parameter | Description |
| :--- | :--- |
| uid | Remote user id |
| azimuth | Set the position where the remote user’s voice appears, with value range of [-90,90]. 0: (by default) voice appears in the right ahead. -90: voice appears in the left side. 90: voice appears in the right side. |
| gain | Set the voice volume of remote users, with value range of [0,100]. The default value is 100.0, indicating user’s original volume. The smaller the value, the lower the volume |

##### Return[](#setRemoteUidVoicePosition)

- 0: Return after successful calling of the method
- < 0: Return upon failure

--------------------------

### ThunderVideoFrameConsumer

#### ThunderVideoFrameConsumer::consumePixelBuffer:withTimestamp:rotation:

```objc
- (void)consumePixelBuffer:(CVPixelBufferRef _Nonnull)pixelBuffer
             withTimestamp:(CMTime)timestamp
                  rotation:(ThunderVideoRotation)rotation;
```

Interface for pushing video frame.

##### Parameter[](#consumePixelBuffer)

| Parameter | Description |
| :--- | :--- |
| pixelBuffer | Video original data (a frame) |
| timestamp | The current frame displays the system time, in unit of ms. The developer must set a timestamp for each video frame. |
| rotation | For clockwise rotation angle of the video, see [ThunderVideoRotation for details](#ThunderVideoRotation) |

--------------------------

#### ThunderVideoFrameConsumer::consumeRawData:withTimestamp:format:size:rotation

```objc
- (void)consumeRawData:(void *_Nonnull)rawData
         withTimestamp:(CMTime)timestamp
                format:(ThunderVideoPixelFormat)format
                  size:(CGSize)size
              rotation:(ThunderVideoRotation)rotation;
```

Interface for pushing raw video data.

##### Parameter[](#consumeRawData)

| Parameter | Description |
| :--- | :--- |
| rawData | Video original data (a frame) |
| timestamp | The current frame displays the system time, in unit of ms. The developer must set a timestamp for each video frame. |
| format | Image format |
| size | For video naked data, see [CGSize for details](#CGSize) |
| rotation | For clockwise rotation angle of the video, see [ThunderVideoRotation for details](#ThunderVideoRotation) |

--------------------------

#### ThunderVideoFrameConsumer::consumeCMSampleBuffer:

```objc
- (void)consumeCMSampleBuffer:(CMSampleBufferRef _Nonnull)sampleBuffer;
```

Interface for pushing raw video data.

##### Parameter[](#consumeCMSampleBuffer)

| Parameter | Description |
| :--- | :--- |
| sampleBuffer | Video original data (a frame) |

--------------------------

### ThunderAudioFilePlayer

#### ThunderAudioFilePlayer::setPlayerDelegate:

```objc
- (void)setPlayerDelegate:(nullable id<ThunderAudioFilePlayerDelegate>)delegate;
```

Callback on setting audio playback event.

##### Parameter[](#setPlayerDelegate)

| Parameter | Description |
| :--- | :--- |
| delegate | For event callback, see [ThunderAudioFilePlayerDelegate for details](notification.md#ThunderAudioFilePlayerDelegate) |

--------------------------

#### ThunderAudioFilePlayer::open:

```objc
- (void)open:(nonnull NSString*)path;
```

Open audio file, formats supported: mp3, aac, wav.

##### Parameter[](#open)

| Parameter | Description |
| :--- | :--- |
| path | File path |

--------------------------

#### ThunderAudioFilePlayer::close

```objc
- (void)close;
```

Close audio file.

--------------------------

#### ThunderAudioFilePlayer::play

```objc
- (void)play;
```

Start playing.

--------------------------

#### ThunderAudioFilePlayer::stop

```objc
- (void)stop;
```

Stop playing.

--------------------------

#### ThunderAudioFilePlayer::pause

```objc
- (void)pause;
```

Pause playing.

--------------------------

#### ThunderAudioFilePlayer::resume

```objc
- (void)resume;
```

Continue to play.

--------------------------

#### ThunderAudioFilePlayer::seek:

```objc
- (void)seek:(uint32_t)timeMS;
```

Skip to specified play time.

##### Parameter[](#seek)

| Parameter | Description |
| :--- | :--- |
| timeMS | Play time |

--------------------------

#### ThunderAudioFilePlayer::getTotalPlayTimeMS

```objc
- (uint32_t)getTotalPlayTimeMS;
```

Get the total play time of files.
> **Note:**
>
> - Return the total playing time (unit: millisecond)

--------------------------

#### ThunderAudioFilePlayer::getCurrentPlayTimeMS

```objc
- (uint32_t)getCurrentPlayTimeMS;
```

Get the time which has been played. Return the played time (unit: millisecond)

--------------------------

#### ThunderAudioFilePlayer::setPlayVolume:

```objc
- (void)setPlayVolume:(uint32_t)volume;
```

Set the playing volume of current file.

##### Parameter[](#setPlayVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-400] |

--------------------------

#### ThunderAudioFilePlayer::setPlayerLocalVolume:

```objc
- (int)setPlayerLocalVolume:(uint32_t)volume;
```

Adjust volume of music file in mixed video being played locally.
> **Note:**
>
> - Please call this method in channels.

##### Parameter[](#setPlayerLocalVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-100] |

##### Return[](#setPlayerLocalVolume)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderAudioFilePlayer::setPlayerPublishVolume:

```objc
- (int)setPlayerPublishVolume:(uint32_t)volume;
```

Adjust volume of music file in mixed video being played remotely.
> **Note:**
>
> - Please call this method in channels.

##### Parameter[](#setPlayerPublishVolume)

| Parameter | Description |
| :--- | :--- |
| volume | Play volume [0-100] |

##### Return[](#setPlayerPublishVolume)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderAudioFilePlayer::getPlayerLocalVolume

```objc
- (int)getPlayerLocalVolume;
```

Get the local volume of music files.

##### Return[](#getPlayerLocalVolume)

- [0-100]: Upon successful calling of the method, return the volume, range as [0-100]
- < 0: Method calling failed

--------------------------

#### ThunderAudioFilePlayer::getPlayerPublishVolume

```objc
- (int)getPlayerPublishVolume;
```

Get the remote volume of music files.

##### Return[](#getPlayerPublishVolume)

- [0-100]: Upon successful calling of the method, return the volume, range as [0-100]
- < 0: Method calling failed

--------------------------

#### ThunderAudioFilePlayer::setSemitone:

```objc
- (void)setSemitone:(int)val;
```

Set a tone for audio playing.

##### Parameter[](#setSemitone)

| Parameter | Description |
| :--- | :--- |
| val | Volume -5, -4, -3, -2, -1, 0(normal), 1, 2, 3, 4, 5 |

--------------------------

#### ThunderAudioFilePlayer::setLooping:

```objc
- (int)setLooping:(int)cycle;
```

Sets times of loop playbacks.

##### Parameter[](#setLooping)

| Parameter | Description |
| :--- | :--- |
| cycle | Positive integer: Circulation times<br> 0: Cancel circulation -1: Infinite circulation<br> |

##### Return[](#setLooping)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderAudioFilePlayer::selectAudioTrack:

```objc
- (int)selectAudioTrack:(int)trackIndex;
```

Select an audio track.

##### Parameter[](#selectAudioTrack)

| Parameter | Description |
| :--- | :--- |
| trackIndex | Audio track index |

##### Return[](#selectAudioTrack)

- 0: Success.
- For other errors, refer to [ThunderRet](code.md#ThunderRet)

--------------------------

#### ThunderAudioFilePlayer::getAudioTrackCount

```objc
-(int)getAudioTrackCount;
```

Acquire quantity of audio tracks. Return the quantity of file audio track.

--------------------------

#### ThunderAudioFilePlayer::enablePublish:

```objc
- (void)enablePublish:(BOOL)enable;
```

Whether to use a currently played file as a live accompaniment.

##### Parameter[](#enablePublish)

| Parameter | Description |
| :--- | :--- |
| enable | Enable or disable, disable by default |

--------------------------

#### ThunderAudioFilePlayer::enableSpectrum:

```objc
- (void)enableSpectrum:(BOOL)enable;
```

Enable the spectrum or not.

##### Parameter[](#enableSpectrum)

| Parameter | Description |
| :--- | :--- |
| enable | YES: Open<br>NO: Close<br>Close by default<br> |

--------------------------

#### ThunderAudioFilePlayer::enableVolumeIndication:interval:

```objc
- (void)enableVolumeIndication:(BOOL)enable interval:(int)interval;
```

Enable the volume callback or not.

##### Parameter[](#enableVolumeIndication)

| Parameter | Description |
| :--- | :--- |
| enable | YES: Open <br>NO: Close |
| interval | Callback interval |

--------------------------

#### ThunderAudioFilePlayer::setMixStandard:

```objc
-(void)setMixStandard:(BOOL)standard;
```

Set whether the accompaniment is a standard stream for video mixing.

##### Parameter[](#setMixStandard)

| Parameter | Description |
| :--- | :--- |
| standard | YES: Standard stream<br> NO: Non-standard stream <br>NO by default |

--------------------------

#### ThunderAudioFilePlayer::isMixStandard

```objc
-(BOOL)isMixStandard;
```

Query whether the accompaniment is a standard stream for video mixing.

##### Return[](#isMixStandard)

- YES: Standard stream
- NO: Non-standard stream

--------------------------

#### ThunderAudioFilePlayer::getCurrentSpectrum:len:

```objc
-(int)getCurrentSpectrum:(float* _Nonnull)buffer len:(int)len;
```

Acquire spectrum information;
> **Note:**
>
> - Return the effective data length, ranging from[0 to 1].

##### Parameter[](#getCurrentSpectrum)

| Parameter | Description |
| :--- | :--- |
| buffer | Spectrum buffer |
| len | Length of spectrum buffer |

--------------------------

### IMediaEngine

#### IMediaEngine::registerAudioFrameObserver

```c++
  static bool registerAudioFrameObserver(IAudioFrameObserver* observer);
```

Register an audio frame observer.

##### Parameter[](#registerAudioFrameObserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | Audio observer object |

--------------------------

## Enumerated values & structure definition

### ThunderEngine

#### ThunderRtcConfig

```objc
typedef NS_ENUM(NSInteger, ThunderRtcConfig);
```

Set operation mode of SDK

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_CONFIG_DEFAULT(0) | Default mode |
| THUNDER_CONFIG_NORMAL(1) | Audio/video mode |
| THUNDER_CONFIG_ONLY_AUDIO(2) | Pure voice mode; optimize for pure audio |

--------------------------

#### ThunderRtcRoomConfig

```objc
typedef NS_ENUM(NSInteger, ThunderRtcRoomConfig);
```

Set room profile

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_ROOM_CONFIG_LIVE(0) | Live (high quality, without interaction mode) (shifted to medium quality and strong interaction mode when connecting microphones) |
| THUNDER_ROOM_CONFIG_COMMUNICATION(1) | Communication (medium quality and strong interaction mode) |
| THUNDER_ROOM_CONFIG_GAME(3) | Game (low quality and strong interaction mode) |
| THUNDER_ROOM_CONFIG_MULTIAUDIOROOM(4) | Multi-person voice room (medium quality, economic traffic and strong interaction mode) |
| THUNDER_ROOM_CONFIG_CONFERENCE(5) | Conference (medium quality, strong interaction mode, applicable to frequent enabling/disabling of microphones, with smooth sound in enabling/disabling microphones) |

--------------------------

#### ThunderRtcLogLevel

```objc
typedef NS_ENUM(NSInteger, ThunderRtcLogLevel);
```

Set log level

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_LOG_LEVEL_TRACE(0) | //TRACE |
| THUNDER_LOG_LEVEL_DEBUG(1) | //DEBUG |
| THUNDER_LOG_LEVEL_INFO(2) | //INFO |
| THUNDER_LOG_LEVEL_WARN(3) | //WARN |
| THUNDER_LOG_LEVEL_ERROR(4) | //ERROR |

--------------------------

#### LiveTranscoding

```objc
@interface LiveTranscoding : NSObject

@property(nonatomic, strong)NSString *mAudioUrl;
@property(nonatomic, strong)NSString *mLyricUrl;
@property(nonatomic, strong)NSString *mMediaUrl;
@property(nonatomic, strong)MediaStreamLayoutObj* mMediaStreamLayout;

/**
 @brief Add a user to the mixed video layout
 @param [IN] user 见TranscodingUser
 @return 0 Succeeded
 */
- (int)addUser:(TranscodingUserObj*)user;

/**
 @brief Set user mixed video layout in batches
        In this method, the user sets all users participating in the combined picture. This method replaces the original data with new User data.
 @param [IN] users All mixed video users in channel
 */
- (void)setUsers:(NSMutableArray*)users;

/**
 @brief Get current user location information
 @return Get information of all users in mixed video canvas in channel
 */
- (NSMutableArray*)getUsers;

/**
 @brief Remove users joining video mixing
 @param [IN] uid User ID to be removed
 @return 0 Succeede
 */
- (int)removeUserWithUid:(NSString*)uid;

/**
 @brief Remove the mixed video of this channel. That is, the user will not use the mixed video
 @return 0 Succeede
 */
- (int)removeAllUsers;

/**
 @brief Get the number of users joining video mixing
 @return Number of users
 */
- (int)getUserCount;

/**
 @brief Set the bracket of mixed video outputted
 @param [IN] transCodingMode mode
 */
- (void)setTransCodingMode:(ThunderTranscodingModeType)transCodingMode;

/**
 @brief Get the bracket of mixed video outputted
 @return mode
 */
- (ThunderTranscodingModeType)getTransCodingMode;

/**
 @brief Whether to open the mixed video with media extra information
 @return true open, false closed
*/
- (BOOL)isEnableMixVideoExtraInfo;

/**
 @brief Set the external pure audio url as the standard stream for this mixed video. Because the progress of the standard stream playback is required internally for synchronization of mixed video, it cannot be used simultaneously through the interface setMediaStandardSream.
   So, the client should use ThunderAudioFilePlayer to play this audio and call setMixStandard in ThunderAudioFilePlayer to set the standard stream.
   If the user wants to use a customized style lyrics in the mixed video, the anchor can use the sendMediaExtraInfo interface to send the lyrics progress, and call setAudioOnlyStandardSreamUrl to set the lyricUrl parameter to null,
   the audience will receive the onRecvMediaExtraInfo callback of IThunderMediaExtraInfoCallback when playing this mixed video stream, then read out the corresponding lyrics progress, and draw the lyrics according to the progress. 
 @param [IN] audioUrl Standard video file url
 @param [IN] lyricUrl url of the lyrics file corresponding to the audio. The bank indicates no lyrics, otherwise the lyrics will be added to the mixed video in the default style.
 @return 0 Succeeded， <0 Failed
*/
- (int)setAudioOnlyStandardSreamUrl:(NSString*)audioUrl lyricUrl:(NSString*)lyricUrl;

/**
 @brief The external video media stream is set as the standard stream for mixed video, which cannot be used through interface setAudioOnlyStandardSreamUrl simultaneously.
 @param [IN] mediaUrl Standard video file url
 @param [IN] layout   Layout information of video media stream in the mixed video.
 @return 0 Succeeded， <0 Failed
*/
- (int)setMediaStandardSream:(NSString*) mediaUrl layout:(MediaStreamLayoutObj*) layout;

- (NSString*)description;

@end
````

--------------------------

#### ThunderVideoRotation

```objc
typedef NS_ENUM(NSInteger, ThunderVideoRotation);
```

Screen rotation angle.

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_ROTAION_NONE(0) | Rotate 0 degree clockwise |
| THUNDER_VIDEO_ROTAION_90(1) | Rotate 90 degree clockwise |
| THUNDER_VIDEO_ROTAION_180(2) | Rotate 180 degree clockwise |
| THUNDER_VIDEO_ROTAION_270(3) | Rotate 270 degree clockwise |

--------------------------

#### ThunderRtcRemotePlayType

```objc
typedef NS_ENUM(NSInteger, ThunderRtcRemotePlayType);
```

For local display mode of remote video, one person for singular view or multiple persons for singular view

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_REMOTE_PLAY_NORMAL(0) | common audience view |
| THUNDER_REMOTE_PLAY_MULTI(1) | Multiple interaction view |

--------------------------

#### ThunderMultiVideoViewParam

```objc
__attribute__((visibility("default"))) @interface ThunderMultiVideoViewParam: NSObject
@property(strong, nonatomic)NSArray<ThunderMultiVideoViewCoordinate*>* _Nonnull videoPositions;
@property(strong, nonatomic)ThunderMultiVideoViewCoordinate* _Nullable bgCoordinate;
@property(copy, nonatomic)NSString* _Nullable bgImageName;
@end
```

| Parameter | Meaning |
| :--- | :--- |
| videoPositions | For video/view layout parameters, see [ThunderMultiVideoViewCoordinate for details](#ThunderMultiVideoViewCoordinate) |
| bgCoordinate | For video/view background layout parameters, see [ThunderMultiVideoViewCoordinate for details](#ThunderMultiVideoViewCoordinate) |
| bgImageName | Video/view background picture |

--------------------------

#### ThunderMultiVideoViewCoordinate

```objc
__attribute__((visibility("default"))) @interface ThunderMultiVideoViewCoordinate: NSObject
@property(assign, nonatomic)int x;
@property(assign, nonatomic)int y;
@property(assign, nonatomic)int width;
@property(assign, nonatomic)int height;
@property(assign, nonatomic)int index;
@end
```

Multi-person microphone connection setting layout

| Parameter | Meaning |
| :--- | :--- |
| x | X coordinate at upper left corner of the single video/view layout |
| y | Y coordinate at upper left corner of the single video/view layout |
| width | Width of the single video/view layout |
| height | Height of the single video/view layout |
| index | Seat No. of the single video/view layout, starting from 0 |

--------------------------

#### ThunderVideoCanvas

```objc
__attribute__((visibility("default"))) @interface ThunderVideoCanvas : NSObject
@property(strong, nonatomic) UIView* _Nullable view;
@property(assign, nonatomic) ThunderVideoRenderMode renderMode;
@property(copy, nonatomic) NSString* _Nullable uid;
@property(assign, nonatomic)int seatIndex;
@end
```

| Parameter | Meaning |
| :--- | :--- |
| view | UIView |
| renderMode | See [ThunderVideoRenderMode for details](#ThunderVideoRenderMode) |
| uid | User ID |
| seatIndex | Set user’s display position during multi-person microphone connection |

--------------------------

#### ThunderVideoRenderMode

```objc
typedef NS_ENUM(NSInteger, ThunderAudioRawFrameOperationMode );
```

Use mode of original audio/video data

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_ONLY(1) | Read only mode. The user only acquires original data from AudioFrame |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_WRITE_ONLY(2) | Write only mode. The user replaces data in AudioFrame for encoding transmission of SDK |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_WRITE(3) | Read-write mode. The user obtains data from AudioFrame and modifies data. Then the data is returned to SDK for encoding and transmission. |

--------------------------

#### ThunderVideoMirrorMode

```objc
typedef NS_ENUM(NSInteger, ThunderVideoMirrorMode);
```

Mirroring

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_MIRROR_PUBLISH_NO_MIRROR(0) | The preview other than stream publishing is mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_MIRROR(1) | Both preview and stream publishing are not mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_NO_MIRROR(2) | Neither preview and stream publishing is not mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_NO_MIRROR_PUBLISH_MIRROR(3) | Preview is not mirrored, but publish is mirrored |

--------------------------

#### ThunderRtcAudioConfig

```objc
typedef NS_ENUM(NSInteger, ThunderRtcAudioConfig);
```

Audio Profiles

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_CONFIG_DEFAULT(0) | Default settings. which is 1 in communication mode, and 2 in live mode. |
| THUNDER_AUDIO_CONFIG_SPEECH_STANDARD(1) | Specify the sampling rate of 16 KHz, voice encoding, single track, and encoding rate of around 18 kbps |
| THUNDER_AUDIO_CONFIG_MUSIC_STANDARD_STEREO(2) | Specify the sampling rate of 44.1 KHz, voice encoding, dual track, encoding rate of around 24 kbps, and high delay in encoding |
| THUNDER_AUDIO_CONFIG_MUSIC_STANDARD(3) | Specify the sampe rate of 44.1 KHz, music encoding, dual track, encoding rate of around 40 kbps, and low delay in encoding |
| THUNDER_AUDIO_CONFIG_MUSIC_HIGH_QUALITY_STEREO(4) | Specify the sampling rate of 44.1KHz, music encoding, dual track, and encoding rate of around 128 kbps |
| THUNDER_AUDIO_CONFIG_MUSIC_HIGH_QUALITY_STEREO_192(5) | Specify the sampling rate of 44.1KHz, music encoding, dual track, and encoding rate of around 192kbps |

--------------------------

#### ThunderRtcCommutMode

```objc
typedef NS_ENUM(NSInteger, ThunderRtcCommutMode);
```

Interactive mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_COMMUT_MODE_DEFAULT(0) | =1 by default |
| THUNDER_COMMUT_MODE_DEFAULT(1) | High interactive mode |
| THUNDER_COMMUT_MODE_DEFAULT(2) | Low interactive mode |

--------------------------

#### ThunderRtcScenarioMode

```objc
typedef NS_ENUM(NSInteger, ThunderRtcScenarioMode);
```

Scenario mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SCENARIO_MODE_DEFAULT(0) | =1 by default |
| THUNDER_SCENARIO_MODE_STABLE_FIRST(1) | Fluent priority: applicable for stable education |
| THUNDER_SCENARIO_MODE_QUALITY_FIRST(2) | Fluent priority: applicable for stable education |

--------------------------

#### ThunderEqGainsOc

```objc
typedef float ThunderEqGainsOc[11];
```

Equalizer parameter, -12 <= gains[i] <= 12, where i shall be 0<= i <=10

--------------------------

#### ThunderReverbExParamOc

```objc
struct ThunderReverbExParamOc;
```

Reverberation parameters

| Parameter | Type | Value |
| :--- | :--- | :--- |
| mRoomSize | double | 0~100 |
| mPreDelay | double | 0~200 |
| mReverberance | double | 0~100 |
| mHfDamping | double | 0~100 |
| mToneLow | double | 0~100 |
| mToneHigh | double | 0~100 |
| mWetGain | double | -20~10 |
| mDryGain | double | -20~10 |
| mStereoWidth | double | 0~100 |

--------------------------

#### ThunderCprParamOc

```objc
typedef struct CG_BOXABLE ThunderCprParamOc ThunderCprParamOc;
```

Compressor parameters

| Parameter | Type | Value |
| :--- | :--- | :--- |
| threshold | int | Threshold; range: [-40~0] |
| makeupGain | int | Gain |
| ratio | int | Scale |
| knee | int | Slope |
| releaseTime | int | Release time; range: Over 0 |
| attackTime | int | Launch time; range: Over 0 |

--------------------------

#### ThunderLimiterParamOc

```objc
struct ThunderLimiterParamOc;
typedef struct CG_BOXABLE ThunderLimiterParamOc ThunderLimiterParamOc;
```

| Parameter | Type | Value |
| :--- | :--- | :--- |
| fCeiling | float | (-30 ~ 0) |
| fThreshold | float | (-10 ~ 0) |
| fPreGain | float | (0~30) |
| fRelease | float | (0~1000) |
| fAttack | float | (0~1000) |
| fLookahead | float | (0~8) |
| fLookaheadRatio | float | (0.5~2) |
| fRMS | float | (0~100) |
| fStLink | float | (0~1) |

--------------------------

#### ThunderSourceType

```objc
typedef NS_ENUM(NSInteger, ThunderSourceType);
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_MIC(0) | Only microphone |
| THUNDER_AUDIO_FILE(1) | Only file |
| THUNDER_AUDIO_MIX(2) | Microphone and file |
| THUNDER_SOURCE_TYPE_NONE(10) | Stop all upstream audio data |

--------------------------

#### ThunderSaverMode

```objc
typedef NS_ENUM(NSInteger, ThunderSaverMode);
```

Save mode.

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_SAVER_ONLY_CAPTURE(0) | Only save all uplink audio data in the room. Uplink audio data: Audio data of the anchor and accompany that have been set as uplink |
| THUNDER_AUDIO_SAVER_ONLY_RENDER(1) | Save audio data beyond the anchor in the room, e.g. audio/video data of the accompany and audience |
| THUNDER_AUDIO_SAVER_BOTH(2) | Save all audio data in the room |

--------------------------

#### ThunderFileMode

```objc
typedef NS_ENUM(NSInteger, ThunderFileMode);
```

Write data mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_SAVER_FILE_APPEND(0) | Open a text file, and the data written will override the file |
| THUNDER_AUDIO_SAVER_FILE_OVERRIDE(1) | Open another text file and write data at end of the file |

--------------------------

#### ThunderAudioRawFrameOperationMode

```objc
typedef NS_ENUM(NSInteger, ThunderAudioRawFrameOperationMode );
```

Write data mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_ONLY(1) | Read only mode. The user only acquires original data from AudioFrame |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_WRITE_ONLY(2) | Open another text file and write data at end of the file |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_WRITE(3) | Read and write mode and write only mode. The user replaces data in AudioFrame for encoding transmission of SDK |

--------------------------

#### CGSize

```objc
struct CGSize {
    CGFloat width;
    CGFloat height;
};
```

| Field | Meaning |
| :--- | :--- |
| width | Width |
| height | High |

--------------------------

#### AudioFrame

```c++
struct IAudioFrameObserver::AudioFrame;
```

Detailed information of audio data

| Parameter | Meaning |
| :--- | :--- |
| type | For audio frame type, see [AUDIO_FRAME_TYPE for details](#AUDIO_FRAME_TYPE) |
| samples | Sample quantity of the frame |
| bytesPerSample | Bytes per sample: PCM (16 digits) contains two types |
| channels | Number of channels (crossed data for stereo); 1: single track, 2: dual track |
| samplesPerSec | Sampling rate |
| buffer | data buffer |
| renderTimeMs | Not used momentarily |
| avsync_type | Not used momentarily |

--------------------------

#### TranscodingUserObj

```objc
@interface TranscodingUserObj : NSObject

@property(copy, nonatomic) NSString* uid; // Anchor ID
@property(copy, nonatomic) NSString* roomId; // Anchor’s current publish room
@property(assign, nonatomic) BOOL bStandard; // Standard stream user or not, default to false, competition stream is generally regarded as standard stream in a competition scenario
@property(assign, nonatomic) int layoutX; // User’s x coordinate of the begin point in video mixing canvas
@property(assign, nonatomic) int layoutY; // User’s y coordinate of the begin point in video mixing canvas
@property(assign, nonatomic) int layoutW; // User’s width in video mixing canvas
@property(assign, nonatomic) int layoutH; // User’s height in video mixing canvas
@property(assign, nonatomic) int zOrder; // Layer number of user frame on the live video.
                                         // The value range is the integer in [0, 100], and the minimum value is 0 (default value), indicating that the image in this region is at the lowest level
@property(assign, nonatomic) BOOL bCrop; // The way in which the source stream adapts to the video mixing window
                                         // true: crop extra parts after zooming; false: mend black edge after zooming; this is applied to the crop region if such a region is set.
@property(assign, nonatomic) int cropX; // X coordinate of the begin point in the crop region of current anchor’s source video
@property(assign, nonatomic) int cropY; // Y coordinate of the begin point in the crop region of current anchor’s source video
@property(assign, nonatomic) int cropW; // Width of the crop region of current anchor’s source video
@property(assign, nonatomic) int cropH; // Height of the crop region of current anchor’s source video
@property(assign, nonatomic) float alpha; // Transparency of user video on the live video. The value range is [0.0, 1.0].
                                          // 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque. The default is 1.0
@property(assign, nonatomic) int audioChannel; // Not yet realized

- (NSString*)description;
- (BOOL)isEqual:(id)obj;

@end
```

--------------------------

#### ThunderTranscodingModeType

```objc
typedef NS_ENUM(NSInteger, ThunderTranscodingModeType);
```

Video mixing bracket

| Enumerated values | Meaning |
| :--- | :--- |
| TRANSCODING_MODE_NON(0) | //Retain bracket |
| TRANSCODING_MODE_320X180(1) | "encode":100,"bitrate": 150, "fps": 15, "gop": 30, "width": 320, "height": 180 |
| TRANSCODING_MODE_320X240(2) | "encode": 100,"bitrate": 200, "fps": 15, "gop": 30, "width": 320, "height": 240 |
| TRANSCODING_MODE_640X360(3) | "encode": 100,"bitrate": 500, "fps": 15, "gop": 30, "width": 640, "height": 360 |
| TRANSCODING_MODE_640X480(4) | "encode": 100,"bitrate": 500, "fps": 15, "gop": 30, "width": 640, "height": 480 |
| TRANSCODING_MODE_960X544(5) | "encode": 100,"bitrate": 1000, "fps": 24, "gop": 48, "width": 960, "height": 544 |
| TRANSCODING_MODE_1280X720(6) | "encode": 100,"bitrate": 1600, "fps": 24, "gop": 48, "width": 1280, "height": 720 |
| TRANSCODING_MODE_1920X1080(7) | "encode": 100,"bitrate": 4500, "fps": 24, "gop": 48, "width": 1920, "height": 1080 |

--------------------------

#### MediaStreamLayoutObj

```objc
@interface MediaStreamLayoutObj : NSObject

@property(assign, nonatomic) int layoutX; // X coordinate of begin point of the media in video mixing canvas
@property(assign, nonatomic) int layoutY; // Y coordinate of begin point of the media in video mixing canvas
@property(assign, nonatomic) int layoutW; // Width of the media in video mixing canvas
@property(assign, nonatomic) int layoutH; // Height of the media in video mixing canvas
@property(assign, nonatomic) int zOrder; // Layer number of the media video frame on the live video. The value range is the integer in [0, 100],
                                         // and the minimum value is 0 (default value), indicating that the image in this region is at the lowest level
@property(assign, nonatomic) BOOL bCrop; // The way in which the source stream adapts to the video mixing window, true: crop extra parts after zooming;
                                         // false: mend black edge after zooming; this is applied to the crop region if such a region is set.
@property(assign, nonatomic) int cropX; // X coordinate of the begin point in the crop region of current anchor’s source video
@property(assign, nonatomic) int cropY; // Y coordinate of the begin point in the crop region of current anchor’s source video
@property(assign, nonatomic) int cropW; // Width of the crop region of current anchor’s source video
@property(assign, nonatomic) int cropH; // Height of the crop region of current anchor’s source video
@property(assign, nonatomic) float alpha; // Transparency of media video on the live video. The value range is [0.0, 1.0].
                                          // 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque. The default is 1.0
@property(assign, nonatomic) int audioChannel; // Not yet realized

- (NSString*)description;
- (BOOL)isEqual:(id)obj;

@end
```

--------------------------

#### ThunderVideoEncoderConfiguration

```objc
__attribute__((visibility("default"))) @interface ThunderVideoEncoderConfiguration : NSObject
@property(assign, nonatomic) ThunderPublishPlayType playType;
@property(assign, nonatomic) int publishMode;
@end
```

Publishing profile of video

| Parameter | Meaning |
| :--- | :--- |
| playType | For publishing methods, see [ThunderPublishPlayType for details](#ThunderPublishPlayType) |
| publishMode | For video encoding type, see [ThunderPublishVideoMode for details](#ThunderPublishVideoMode) |

--------------------------

#### ThunderVideoEncodeParam

```objc
__attribute__((visibility("default"))) @interface ThunderVideoEncodeParam : NSObject
@property(assign, nonatomic) NSUInteger width; // width
@property(assign, nonatomic) NSUInteger height; // height
@property(assign, nonatomic) NSUInteger frameRate; // frame rate
@property(assign, nonatomic) NSUInteger codeRate; // code rate
@end
```

--------------------------

#### ThunderPublishPlayType

```objc
typedef enum ThunderPublishPlayType;
```

Publish play type

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDERPUBLISH_PLAY_SINGLE(0) | Single publishing |
| THUNDERPUBLISH_PLAY_INTERACT(1) | Microphone-connection video publishing |
| THUNDERPUBLISH_PLAY_SCREENCAP(2) | Screen recording publishing |
| THUNDERPUBLISH_PLAY_MULTI_INTERACT(3) | Multi-person microphone connection publishing |

--------------------------

#### ThunderPublishVideoMode

```objc
typedef enum ThunderPublishVideoMode;
```

Video encoding type

| Enumerated values | Meaning | Resolution（wide*high） | Encoding rate | Frame rate |
| ---- | :--- | :--- | ---- | ---- |
| THUNDERPUBLISH_VIDEO_MODE_NORMAL(1) | Ordinary | 320*240(landscape) | 200Kbps | 15fps |
| THUNDERPUBLISH_VIDEO_MODE_HIGHQULITY(2) | High definition | 368*640(portrait) | 500Kbps | 15fps |
| THUNDERPUBLISH_VIDEO_MODE_SUPERQULITY(3) | Ultra definition | 544*960(portrait) | 1000Kbps | 24fps |
| THUNDERPUBLISH_VIDEO_MODE_BLUERAY_2M(4) | Blue ray 2M | 720*1280(portrait) | 1500Kbps | 24fps |
| THUNDERPUBLISH_VIDEO_MODE_BLUERAY_4M(5) | Blue ray 4M | 1080*1920(portrait) | 3000Kbps | 24fps |

--------------------------

#### ThunderRtcAreaType

```objc
typedef NS_ENUM(NSInteger, ThunderRtcAreaType);
```

Geographic area

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AREA_DEFAULT(0) | Default (domestic) |
| THUNDER_AREA_FOREIGN(1) | Overseas |
| THUNDER_AREA_RESERVED(2) | thunder-reserved |

--------------------------

#### ThunderVideoCaptureOrientation

```objc
typedef NS_ENUM(NSInteger, ThunderVideoCaptureOrientation);
```

Portrait and landscape

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_ORIENTATION_PORTRAIT(0) | Portrait |
| THUNDER_VIDEO_CAPTURE_ORIENTATION_LANDSCAPE(1) | Landscape |

--------------------------

#### AUDIO_FRAME_TYPE

```c++
enum AUDIO_FRAME_TYPE;
```

Audio/video data frame type.

| Enumerated values | Meaning |
| :--- | :--- |
| FRAME_TYPE_PCM16(0) | PCM 16bit little endian |

--------------------------


