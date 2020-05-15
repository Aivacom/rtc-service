# Functional Interface

## Interface List

- 
   ### IThunderEngine

| Global Function | Function Name |
| ---:| :--- |
| Thunder::IThunderEngine* | [createEngine](#IThunderEngine::createEngine)() |

| public member functions | Function Name |
| ---:| :--- |
| virtual void | [destroyEngine](#IThunderEngine::destroyEngine)() = 0 |
| virtual int | [initialize](#IThunderEngine::initialize)(const char* appId, int sceneId, [IThunderEventHandler](notification.md#IThunderEventHandler)* pHandler) = 0 |
| virtual int | [setArea](#IThunderEngine::setArea)([AREA_TYPE](#AREA_TYPE) area) = 0 |
| virtual int | [joinRoom](#IThunderEngine::joinRoom)(const char* token, int tokenLen, const char* roomId, const char* uid) = 0 |
| virtual int | [leaveRoom](#IThunderEngine::leaveRoom)() = 0 |
| virtual int | [updateToken](#IThunderEngine::updateToken)(const char* token, int tokenLen) = 0 |
| virtual int | [setMediaMode](#IThunderEngine::setMediaMode)([THUNDER_PROFILE](#THUNDER_PROFILE) mode) = 0 |
| virtual int | [setRoomMode](#IThunderEngine::setRoomMode)([ROOM_CONFIG_TYPE](#ROOM_CONFIG_TYPE) mode) = 0 |
| virtual int | [setAudioConfig](#IThunderEngine::setAudioConfig)([AUDIO_PROFILE_TYPE](#AUDIO_PROFILE_TYPE) profile, [COMMUT_MODE](#COMMUT_MODE) commutMode, [SCENARIO_MODE](#SCENARIO_MODE) scenarioMode) = 0 |
| virtual int | [setAudioSourceType](#IThunderEngine::setAudioSourceType)([ThunderSourceType](#ThunderSourceType) sourceType) = 0 |
| virtual int | [stopLocalAudioStream](#IThunderEngine::stopLocalAudioStream)(bool stop) = 0 |
| virtual int | [stopAllRemoteAudioStreams](#IThunderEngine::stopAllRemoteAudioStreams)(bool stop) = 0 |
| virtual int | [stopRemoteAudioStream](#IThunderEngine::stopRemoteAudioStream)(const char* uid, bool stop) = 0 |
| virtual int | [setAudioVolumeIndication](#IThunderEngine::setAudioVolumeIndication)(int interval, int smooth) = 0 |
| virtual int | [enableLoopbackRecording](#IThunderEngine::enableLoopbackRecording)(bool enabled) = 0 |
| virtual int | [startAudioRecording](#IThunderEngine::startAudioRecording)(const char* fileName, [AUDIO_RECORDING_FILE_TYPE](#AUDIO_RECORDING_FILE_TYPE) fileType, [AUDIO_RECORDING_QUALITY_TYPE](#AUDIO_RECORDING_QUALITY_TYPE) quality) = 0 |
| virtual int | [stopAudioRecording](#IThunderEngine::stopAudioRecording)() = 0 |
| virtual int | [adjustRecordingSignalVolume](#IThunderEngine::adjustRecordingSignalVolume)(int volume) = 0 |
| virtual int | [adjustPlaybackSignalVolume](#IThunderEngine::adjustPlaybackSignalVolume)(int volume) = 0 |
| virtual [IAudioDeviceManager](#IAudioDeviceManager)* | [getAudioDeviceMgr](#IThunderEngine::getAudioDeviceMgr)() = 0 |
| virtual bool | [registerAudioFrameObserver](#IThunderEngine::registerAudioFrameObserver)([IAudioFrameObserver](#IAudioDeviceManager)* observer) = 0 |
| virtual int | [setRecordingAudioFrameParameters](#IThunderEngine::setRecordingAudioFrameParameters)(int sampleRate, int channel, [ThunderAudioRawFrameOperationMode](#ThunderAudioRawFrameOperationMode) mode, int samplesPerCall) = 0 |
| virtual int | [setPlaybackAudioFrameParameters](#IThunderEngine::setPlaybackAudioFrameParameters)(int sampleRate, int channel, [ThunderAudioRawFrameOperationMode](#ThunderAudioRawFrameOperationMode) mode, int samplesPerCall) = 0 |
| virtual int | [setLogFilePath](#IThunderEngine::setLogFilePath)(const char* filePath) = 0 |
| virtual int | [setLogLevel](#IThunderEngine::setLogLevel)([LOG_FILTER](#LOG_FILTER) filter) = 0 |
| virtual int | [registerVideoFrameObserver](#IThunderEngine::registerVideoFrameObserver)([IVideoFrameObserver](#IVideoFrameObserver)* observer) = 0 |
| virtual [IVideoDeviceManager](#IVideoDeviceManager)* | [getVideoDeviceMgr](#IThunderEngine::getVideoDeviceMgr)() = 0 |
| virtual int | [setVideoEncoderConfig](#IThunderEngine::setVideoEncoderConfig)(const [VideoEncoderConfiguration](#VideoEncoderConfiguration)& config) = 0 |
| virtual int | [setLocalVideoCanvas](#IThunderEngine::setLocalVideoCanvas)(const [VideoCanvas](#VideoCanvas)& canvas) = 0 |
| virtual int | [setRemoteVideoCanvas](#IThunderEngine::setRemoteVideoCanvas)(const [VideoCanvas](#VideoCanvas)& canvas) = 0 |
| virtual int | [setLocalCanvasScaleMode](#IThunderEngine::setLocalCanvasScaleMode)([VideoRenderMode](#VideoRenderMode) mode) = 0 |
| virtual int | [setRemoteCanvasScaleMode](#IThunderEngine::setRemoteCanvasScaleMode)([VideoRenderMode](#VideoRenderMode) mode) = 0 |
| virtual int | [startVideoPreview](#IThunderEngine::startVideoPreview)() = 0 |
| virtual int | [stopVideoPreview](#IThunderEngine::stopVideoPreview)() = 0 |
| virtual int | [enableLocalVideoCapture](#IThunderEngine::enableLocalVideoCapture)(bool enabled) = 0 |
| virtual int | [stopLocalVideoStream](#IThunderEngine::stopLocalVideoStream)(bool stop) = 0 |
| virtual int | [stopRemoteVideoStream](#IThunderEngine::stopRemoteVideoStream)(const char* uid, bool stop) = 0 |
| virtual int | [stopAllRemoteVideoStreams](#IThunderEngine::stopAllRemoteVideoStreams)(bool stop) = 0 |
| virtual int | [setLocalVideoMirrorMode](#IThunderEngine::setLocalVideoMirrorMode)([ThunderVideoMirrorMode](#ThunderVideoMirrorMode) mode) = 0 |
| virtual int | [setVideoWatermark](#IThunderEngine::setVideoWatermark)(const [ThunderBoltImage](#ThunderBoltImage)& watermark) = 0 |
| virtual int | [removeVideoWatermarks](#IThunderEngine::removeVideoWatermarks)() = 0 |
| virtual int | [setCustomAudioSource](#IThunderEngine::setCustomAudioSource)(bool bEnable, [CustomAudioOptions](#CustomAudioOptions)& option) = 0 |
| virtual int | [pushCustomAudioFrame](#IThunderEngine::pushCustomAudioFrame)(const char* pData, unsigned dataLen, unsigned timeStamp) = 0 |
| virtual int | [setCustomVideoSource](#IThunderEngine::setCustomVideoSource)(bool bEnable, [CustomVideoOptions](#CustomVideoOptions)& option) = 0 |
| virtual int | [pushCustomVideoFrame](#IThunderEngine::pushCustomVideoFrame)(const unsigned char* yuv[3], int linesize[3], unsigned timestamp) = 0 |
| virtual int | [addPublishOriginStreamUrl](#IThunderEngine::addPublishOriginStreamUrl)(const char* url) = 0 |
| virtual int | [removePublishOriginStreamUrl](#IThunderEngine::removePublishOriginStreamUrl)(const char* url) = 0 |
| virtual int | [setLiveTranscodingTask](#IThunderEngine::setLiveTranscodingTask)(const char* taskId, const [LiveTranscoding](#LiveTranscoding)& transcodingCfg) = 0 |
| virtual int | [removeLiveTranscodingTask](#IThunderEngine::removeLiveTranscodingTask)(const char* taskId) = 0 |
| virtual int | [addPublishTranscodingStreamUrl](#IThunderEngine::addPublishTranscodingStreamUrl)(const char* taskId, const char* url) = 0 |
| virtual int | [removePublishTranscodingStreamUrl](#IThunderEngine::removePublishTranscodingStreamUrl)(const char* taskId, const char* url) = 0 |
| virtual int | [addSubscribe](#IThunderEngine::addSubscribe)(const char* roomId, const char* uid) = 0 |
| virtual int | [removeSubscribe](#IThunderEngine::removeSubscribe)(const char* roomId, const char* uid) = 0 |
| virtual int | [enableWebSdkCompatibility](#IThunderEngine::enableWebSdkCompatibility)(bool enabled) = 0 |
| virtual int | [sendUserAppMsgData](#IThunderEngine::sendUserAppMsgData)(const char* msgData) = 0 |
| virtual int | [sendMediaExtraInfo](#IThunderEngine::sendMediaExtraInfo)(const char* extraData) = 0 |
| virtual int | [enableMixVideoExtraInfo](#IThunderEngine::enableMixVideoExtraInfo)(bool enabled) = 0 |
| virtual int | [startScreenCaptureForHwnd](#IThunderEngine::startScreenCaptureForHwnd)(HWND hWnd, const RECT* pRect) = 0 |
| virtual int | [startScreenCaptureForScreen](#IThunderEngine::startScreenCaptureForScreen)(int screenId, const RECT* pRect) = 0 |
| virtual int | [updateScreenCaptureRect](#IThunderEngine::updateScreenCaptureRect)(const RECT* pRect) = 0 |
| virtual int | [stopScreenCapture](#IThunderEngine::stopScreenCapture)() = 0 |
| virtual int | [pauseScreenCapture](#IThunderEngine::pauseScreenCapture)() = 0 |
| virtual int | [resumeScreenCapture](#IThunderEngine::resumeScreenCapture)() = 0 |
| virtual int | [registerVideoCaptureObserver](#IThunderEngine::registerVideoCaptureObserver)([IVideoCaptureObserver](#IVideoCaptureObserver)* observer) = 0 |
| virtual int | [registerMediaExtraInfoObserver](#IThunderEngine::registerMediaExtraInfoObserver)([IThunderMediaExtraInfoObserver](notification.md#IThunderMediaExtraInfoObserver)* observer) = 0 |
| virtual [IThunderAudioPlayer](#IThunderAudioPlayer)* | [createThunderAudioPlayer](#IThunderEngine::createThunderAudioPlayer)() = 0 |
| virtual void | [destroyThunderAudioPlayer](#IThunderEngine::destroyThunderAudioPlayer)([IThunderAudioPlayer](#IThunderAudioPlayer)* player) = 0 |

- 
   ### IAudioDeviceManager

| public member functions | Function Name |
| ---:| :--- |
| virtual int | [enumInputDevices](#IAudioDeviceManager::enumInputDevices)([AudioDeviceList](#AudioDeviceList)& devices) = 0 |
| virtual int | [setInputtingDevice](#IAudioDeviceManager::setInputtingDevice)(GUID& id) = 0 |
| virtual int | [getInputtingDevice](#IAudioDeviceManager::getInputtingDevice)(GUID& id) = 0 |
| virtual int | [setInputtingVolume](#IAudioDeviceManager::setInputtingVolume)(int volume) = 0 |
| virtual int | [getInputtingVolume](#IAudioDeviceManager::getInputtingVolume)(int& volume) = 0 |
| virtual int | [setInputtingMute](#IAudioDeviceManager::setInputtingMute)(bool mute) = 0 |
| virtual int | [getInputtingMute](#IAudioDeviceManager::getInputtingMute)(bool& mute) = 0 |
| virtual int | [startInputDeviceTest](#IAudioDeviceManager::startInputDeviceTest)(int indicationInterval) = 0 |
| virtual int | [stopInputDeviceTest](#IAudioDeviceManager::stopInputDeviceTest)() = 0 |
| virtual int | [enumOutputDevices](#IAudioDeviceManager::enumOutputDevices)([AudioDeviceList](#AudioDeviceList)& devices) = 0 |
| virtual int | [setOutputtingDevice](#IAudioDeviceManager::setOutputtingDevice)(GUID& id) = 0 |
| virtual int | [getOutputtingDevice](#IAudioDeviceManager::getOutputtingDevice)(GUID& id) = 0 |
| virtual int | [setOuttingVolume](#IAudioDeviceManager::setOuttingVolume)(int volume) = 0 |
| virtual int | [getOuttingVolume](#IAudioDeviceManager::getOuttingVolume)(int& volume) = 0 |
| virtual int | [setOutputtingMute](#IAudioDeviceManager::setOutputtingMute)(bool mute) = 0 |
| virtual int | [getOutputtingMute](#IAudioDeviceManager::getOutputtingMute)(bool& mute) = 0 |
| virtual int | [startOutputDeviceTest](#IAudioDeviceManager::startOutputDeviceTest)(int indicationInterval, const char* audioFileName) = 0 |
| virtual int | [stopOutputDeviceTest](#IAudioDeviceManager::stopOutputDeviceTest)() = 0 |
| virtual int | [enableMicEnhancement](#IAudioDeviceManager::enableMicEnhancement)(bool enabled) = 0 |
| virtual int | [enableMicDenoise](#IAudioDeviceManager::enableMicDenoise)(bool enabled) = 0 |
| virtual int | [enableAEC](#IAudioDeviceManager::enableAEC)(bool enabled) = 0 |
| virtual int | [enableAGC](#IAudioDeviceManager::enableAGC)(bool enabled) = 0 |

- 
   ### IThunderAudioPlayer

| public member functions | Function Name |
| ---:| :--- |
| virtual bool | [open](#IThunderAudioPlayer::open)(const char* path) = 0 |
| virtual void | [close](#IThunderAudioPlayer::close)() = 0 |
| virtual void | [play](#IThunderAudioPlayer::play)() = 0 |
| virtual void | [stop](#IThunderAudioPlayer::stop)() = 0 |
| virtual void | [pause](#IThunderAudioPlayer::pause)() = 0 |
| virtual void | [resume](#IThunderAudioPlayer::resume)() = 0 |
| virtual void | [seek](#IThunderAudioPlayer::seek)(unsigned int timeMS) = 0 |
| virtual unsigned int | [getTotalPlayTimeMS](#IThunderAudioPlayer::getTotalPlayTimeMS)() = 0 |
| virtual unsigned int | [getCurrentPlayTimeMS](#IThunderAudioPlayer::getCurrentPlayTimeMS)() = 0 |
| virtual int | [setPlayerLocalVolume](#IThunderAudioPlayer::setPlayerLocalVolume)(int volume) = 0 |
| virtual int | [setPlayerPublishVolume](#IThunderAudioPlayer::setPlayerPublishVolume)(int volume) = 0 |
| virtual int | [getPlayerLocalVolume](#IThunderAudioPlayer::getPlayerLocalVolume)() = 0 |
| virtual int | [getPlayerPublishVolume](#IThunderAudioPlayer::getPlayerPublishVolume)() = 0 |
| virtual int | [setLooping](#IThunderAudioPlayer::setLooping)(int cycle) = 0 |
| virtual void | [SetFilePlayerNotify](#IThunderAudioPlayer::SetFilePlayerNotify)([IThunderAudioPlayerNotify](notification.md#IThunderAudioPlayerNotify)* notify) = 0 |

- 
   ### IVideoDeviceManager

| public member functions | Function Name |
| ---:| :--- |
| virtual int | [enumVideoDevices](#IVideoDeviceManager::enumVideoDevices)([VideoDeviceList](#VideoDeviceList)& devices) = 0 |
| virtual int | [startVideoDeviceCapture](#IVideoDeviceManager::startVideoDeviceCapture)(int deviceIdx) = 0 |
| virtual int | [stopVideoDeviceCapture](#IVideoDeviceManager::stopVideoDeviceCapture)() = 0 |
| virtual int | [enumMonitorDevices](#IVideoDeviceManager::enumMonitorDevices)([MonitorDeviceList](#MonitorDeviceList)& devices) = 0 |

## Detailed Introduction for Interfaces

### IThunderEngine

#### IThunderEngine::createEngine

```c++
EXTERN_C
{
 __declspec(dllimport) Thunder::IThunderEngine* createEngine();
};
```

Create the Thunder::IThunderEngine instance.

> **Note:**
>
> - It is recommended to call the IThunderEngine::[initialize](#IThunderEngine::initialize) interface immediately after createEngine is called.
> - Currently, SDK supports only one IThunderEngine instance, that is, each process can only create one IThunderEngine object.
> - Unless otherwise specified, all interfaces in the IThunderEngine class are called asynchronously. It is recommended that interfaces are called on the same thread.

##### Return[](#createEngine)

Pointer to the Thunder::IThunderEngine object

--------------------------

#### IThunderEngine::destroyEngine

```c++
virtual void Thunder::IThunderEngine::destroyEngine();
```

Destroy the Thunder::IThunderEngine instance.

##### Description[](#destroyEngine)

- This method releases all resources used by SDK.
- Some applications only operate voice communication required by users. Resources can be released for other operations if they are not in need. This method may be applicable for such applications.
- Once [destroyEngine](#IThunderEngine::destroyEngine) is called, the user will be no longer able to use functions of this instance and event notification will not be triggered any more.
- To use communication function again, [createEngine](#IThunderEngine::createEngine) must be called again to create another IThunderEngine instance.

--------------------------

#### IThunderEngine::initialize

```c++
virtual int Thunder::IThunderEngine::initialize(const char* appId, int sceneId, IThunderEventHandler* pHandler);
```

Initialize the engine.

> **Note:**
>
> - Only users with the same appId can communicate with each other.
> - Call this interface after an instance has been created. This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.

##### Parameter[](#initialize)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| appId | IN | appId assigned for application program developers. It can be requested in the official website. |
| sceneId | IN | Id for scenarios customized by developers. It details service scenarios and can be collected with more details based on scenarios. If not required, set it to 0. |
| pHandler | IN | [Pointer of the IThunderEventHandler](./notification.md#IThunderEventHandler) object. SDK calls back various events for application programs through this abstract class during SDK running. |

##### Return[](#initialize)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setArea

```c++
virtual int Thunder::IThunderEngine::setArea(AREA_TYPE area);
```

Set country and area of users.

To accommodate to different laws and regulations at home and abroad, CS2 NETWORK provides both domestic (by default) and international central systems. Set it by referring to the following points:

- If applications are mainly conducted abroad, this interface shall be called to set abroad area.
- The users in domestic and international central systems cannot communicate with each other. So make ensure that users in the same room shall be in the same system.
- The two systems are deployed globally, supporting global access.

> **Note:**
>
> - This interface takes effect only if it is called before the calling of [joinRoom](#IThunderEngine::joinRoom).
> - It is necessary for abroad users but not for domestic users.
> - It can only be reset when [destroyEngine](#IThunderEngine::destroyEngine) is performed.

##### Parameter[](#setArea)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| area | IN | Region type is domestic by default. For details about the parameter value, see [AREA_TYPE.](#AREA_TYPE) |

##### Return[](#setArea)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::joinRoom

```c++
virtual int Thunder::IThunderEngine::joinRoom(const char* token, int tokenLen, const char* roomName, const char* uid);
```

Join a room.

This method lets users join the (audio/video) communication room. In the same room, users can communicate with each other, and group chat starts when multiple users join it.

If during the call, users have to call [leaveRoom](#IThunderEngine::leaveRoom) to leave before joining the next one.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - The applications using different appId cannot communicate with each other.
> - Success returned by the function only indicates request execution success. You have joined a room successfully only if you receive the [onJoinRoomSuccess](notification.md#IThunderEventHandler::onJoinRoomSuccess) notification.

##### Parameter[](#joinRoom)

| Parameter | Type | Description |
| --- | --- | --- |
| token | IN | Required for authentication. For details, see User Authentication Description on official website. |
| tokenLen | IN | Token length |
| roomName | IN | Room Id (unique for AppId) only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| uid | IN | User ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |

##### Return[](#joinRoom)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::leaveRoom

```c++
virtual int Thunder::IThunderEngine::leaveRoom();
```

Leaving room indicates hang off or exiting conversation.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - When [joinRoom](#IThunderEngine::joinRoom) is called, you have to call [leaveRoom](#IThunderEngine::leaveRoom) to end conversation before starting the next one. No matter whether the user is idle or in a call, [leaveRoom](#IThunderEngine::leaveRoom) can be called, without adverse effects. This method can release all resources related to conversation.

##### Return[](#leaveRoom)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::updateToken

```c++
virtual int Thunder::IThunderEngine::updateToken(const char* token, int tokenLen);
```

Update token.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - Success returned by the function only indicates request execution success. You have joined a room successfully only if you receive the [onJoinRoomSuccess](notification.md#IThunderEventHandler::onJoinRoomSuccess) notification.

Token is used for authentication. Recommended token format is as follows. For details, see [Authentication Access Manual](#TODO:?).

| uint16 | uint32 | uint64 | uint64 | uint32 | uint16 | nBytes | 20 Bytes |
| -------- | ------ | ------ | ------------- | ------------ | ------------- | -------------- | ---------------- |
| TokenLen | AppId | uid | TimeStamp(ms) | ValidTime(s) | BizExtInfoLen | BizExtInfoData | DigitalSignature |

Refer to the following descriptions:

1. The multi-byte integer uses network byte order, generally Big Endian.
2. TokenLen: the length of the whole token includes its 2 bytes and abstract.
3. Token expiration time=Timestamp+ValidTime*1000, the UTC time in millisecond since 1970.
4. BizExtInfoData: Extension information that may be needed for service authentication is customized by the service.
5. DigitalSignature: Digital signature adopts the hmac-sha1 algorithm to calculate all data before DigitalSignature to get the [TokenLen,BizExtInfoData]. AppSecret distributed in application of appId is used as the key.
6. Token has to be transmitted by http, so the whole Token shall be encoded by url base64. Note that the url encode is not performed for the whole base64.

##### Parameter[](#updateToken)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| token | IN | Required for authentication. For details, see [User Authentication Description](#TODO:). |
| tokenLen | IN | Token length |

##### Return[](#updateToken)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setMediaMode

```c++
virtual int Thunder::IThunderEngine::setMediaMode(THUNDER_PROFILE mode);
```

Set media format. [PROFILE_NORMAL](#THUNDER_PROFILE) is used by SDK by default.

> **Note:**
>
> - This interface should be called after initialization ([initialize](#IThunderEngine::initialize)) and before joining a room ([joinRoom](#IThunderEngine::joinRoom)).
> - It can only be reset when [destroyEngine](#IThunderEngine::destroyEngine) is performed.

##### Parameter[](#setMediaMode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Media mode. For details about the parameter value, see Thunder::[THUNDER_PROFILE.](#THUNDER_PROFILE) |

##### Return[](#setMediaMode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setRoomMode

```c++
virtual int Thunder::IThunderEngine::setRoomMode(ROOM_CONFIG_TYPE mode);
```

Set room mode. [ROOM_CONFIG_LIVE](#ROOM_CONFIG_TYPE) is used by SDK by default.

> **Note:**
>
> - This interface should be called after initialization ([initialize](#IThunderEngine::initialize)) and before joining a room ([joinRoom](#IThunderEngine::joinRoom)).
> - It can only be reset when [destroyEngine](#IThunderEngine::destroyEngine) is performed.

##### Parameter[](#setRoomMode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Room mode. For details about the parameter value, see Thunder::[ROOM_CONFIG_TYPE.](#ROOM_CONFIG_TYPE) |

##### Return[](#setRoomMode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setAudioConfig

```c++
virtual int Thunder::IThunderEngine::setAudioConfig(AUDIO_PROFILE_TYPE profile, COMMUT_MODE commutMode, SCENARIO_MODE scenarioMode);
```

Set audio parameters and application scenarios.

> **Note:**
>
> - Call it before playing audio [stopLocalAudioStream](#IThunderEngine::stopLocalAudioStream) .
> - It can only be reset when [destroyEngine](#IThunderEngine::destroyEngine) is performed.

##### Parameter[](#setAudioConfig)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| profile | IN | Audio type. For details about the parameter value, see Thunder::[AUDIO_PROFILE_TYPE.](#AUDIO_PROFILE_TYPE) |
| commuMode | IN | Communication mode. For details about the parameter value, see Thunder::[COMMUT_MODE.](#COMMUT_MODE) |
| scenarioMode | IN | Scenario mode. For details about the parameter value, see Thunder::[SCENARIO_MODE.](#SCENARIO_MODE) |

##### Return[](#setAudioConfig)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setAudioSourceType

```c++
virtual int Thunder::IThunderEngine::setAudioSourceType(ThunderSourceType sourceType);
```

Set audio publishing type.

> **Note:**
>
> - It can only be reset when [destroyEngine](#IThunderEngine::destroyEngine) is performed.

##### Parameter[](#setAudioSourceType)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sourceType | IN | Audio publishing mode. For details about the parameter value, see Thunder::[ThunderSourceType.](#ThunderSourceType) |

##### Return[](#setAudioSourceType)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopLocalAudioStream

```c++
virtual int Thunder::IThunderEngine::stopLocalAudioStream(bool stop);
```

Stop broadcasting/Publish audio (including starting capture, encoding, and stream publishing).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#stopLocalAudioStream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Close local audio; false: Open local audio |

##### Return[](#stopLocalAudioStream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopAllRemoteAudioStreams

```c++
virtual int Thunder::IThunderEngine::stopAllRemoteAudioStreams(bool stop);
```

Stop/Receive all audio data. Process this interface based on the following rules:

- By default, SDK receives all audio data.
- After the setting of receiving all (stop=false), all audio stream in the room will be subscribed automatically. You can specify one stream of not being subscribed by [stopRemoteAudioStream](#IThunderEngine::stopRemoteAudioStream).
- After the setting of receiving nothing (stop=true), all audio stream in the room will not be subscribed. You can specify one stream being subscribed by [stopRemoteAudioStream](#IThunderEngine::stopRemoteAudioStream).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.
> - Determine whether to receive or disable remote users. Check the value of [stopRemoteAudioStream](#IThunderEngine::stopRemoteAudioStream) first. If no value is found, use the value of this function.

##### Parameter[](#stopAllRemoteAudioStreams)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Close local audio; false: Open local audio |

##### Return[](#stopAllRemoteAudioStreams)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopRemoteAudioStream

```c++
virtual int Thunder::IThunderEngine::stopRemoteAudioStream(const char* uid, bool stop);
```

Stop/Receive audio data of specified users.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.
> - Determine whether to receive or disable remote users. Check the value of this function first. If no value is found, use the value of [stopRemoteAudioStream](#IThunderEngine::stopAllRemoteAudioStreams).

##### Parameter[](#stopRemoteAudioStream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | IN | User UID |
| Stop | IN | true: Stop user audio, false: Receive user audio |

##### Return[](#stopRemoteAudioStream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setAudioVolumeIndication

```c++
virtual int Thunder::IThunderEngine::setAudioVolumeIndication(int interval, int smooth);
```

Enable volume indication for speaker. 
This method allows SDK to return current speaker and speaker volume to application programs regularly.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.
> - After this method is called, an [onPlayVolumeIndication](notification.md#IThunderEventHandler::onPlayVolumeIndication) notification will be received once anyone speaks in the room
> - The volume carried in the notification does not include sound volume collected by the local microphone or played by files.

##### Parameter[](#setAudioVolumeIndication)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| interval | IN | Notification interval. The default value is 0 <br><=0: The volume prompt is disabled<br> >0: Notification interval, unit: ms (a value greater than 200 is recommended) |
| smooth | IN | Smooth coefficient, not realized currently |

##### Return[](#setAudioVolumeIndication)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::enableLoopbackRecording

```c++
virtual int Thunder::IThunderEngine::enableLoopbackRecording(bool enabled);
```

Enable/Disable graphic card collection.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.

##### Parameter[](#enableLoopbackRecording)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Start graphic card collection; false: Stop graphic card collection |

##### Return[](#enableLoopbackRecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::startAudioRecording

```c++
virtual int Thunder::IThunderEngine::startAudioRecording(const char* fileName,
                                                         AUDIO_RECORDING_FILE_TYPE fileType,
                                                         AUDIO_RECORDING_QUALITY_TYPE quality);
```

Start audio recording.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#startAudioRecording)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| fileName | IN | Recording file name (complete path, not including filename extension, the filename extension is generated based on fileType) |
| fileType | IN | File format. For details about the parameter value, see Thunder::[AUDIO_RECORDING_FILE_TYPE.](#AUDIO_RECORDING_FILE_TYPE) |
| quality | IN | Recording quality. For details about the parameter value, see Thunder::[AUDIO_RECORDING_QUALITY_TYPE.](#AUDIO_RECORDING_QUALITY_TYPE) |

##### Return[](#startAudioRecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopAudioRecording

```c++
virtual int Thunder::IThunderEngine::stopAudioRecording();
```

Stop audio recording.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#stopAudioRecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::adjustRecordingSignalVolume

```c++
virtual int Thunder::IThunderEngine::adjustRecordingSignalVolume(int volume);
```

Set recording volume.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#adjustRecordingSignalVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume range, which is [0--400.] |

##### Return[](#adjustRecordingSignalVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::adjustPlaybackSignalVolume

```c++
virtual int Thunder::IThunderEngine::adjustPlaybackSignalVolume(int volume);
```

Set playing volume.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#adjustPlaybackSignalVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume range, which is [0--400.] |

##### Return[](#adjustPlaybackSignalVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::getAudioDeviceMgr

```c++
virtual Thunder::IAudioDeviceManager* Thunder::IThunderEngine::getAudioDeviceMgr();
```

Obtain the instance object of the audio device management interface.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#getAudioDeviceMgr)

- Object pointer of the audio device management interface [IAudioDeviceManager](#IAudioDeviceManager).
- Null

--------------------------

#### IThunderEngine::registerAudioFrameObserver

```c++
virtual int Thunder::IThunderEngine::registerAudioFrameObserver(IAudioFrameObserver* observer);
```

Register audio frame data observer [IAudioFrameObserver](notification.md#IAudioFrameObserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - The user must inherit the [IAudioFrameObserver](notification.md#IAudioFrameObserver) interface class and implement the virtual methods. These methods will be used to call related original audio data.

##### Parameter[](#registerAudioFrameObserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IAudioFrameObserver](notification.md#IAudioFrameObserver) interface class Registration is canceled if it is set to null. |

##### Return[](#registerAudioFrameObserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setRecordingAudioFrameParameters

```c++
virtual int Thunder::IThunderEngine::setRecordingAudioFrameParameters(int sampleRate,
 int channel,
 ThunderAudioRawFrameOperationMode mode,
 int samplesPerCall);
```

Set the mode for using raw audio recording data during callback [onRecordAudioFrame](notification.md#IAudioFrameObserver::onRecordAudioFrame)

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setRecordingAudioFrameParameters)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sampleRate | IN | Sampling rate |
| channel | IN | Audio track; 1: Single track; 2: dual track |
| mode | IN | [Mode of using onRecordAudioFrame](notification.md#IAudioFrameObserver::onRecordAudioFrame). For details about the parameter value, see Thunder::[ThunderAudioRawFrameOperationMode.](#ThunderAudioRawFrameOperationMode) |
| samplesPerCall | IN | Specify sampling point number for data return in [onRecordAudioFrame](notification.md#IAudioFrameObserver::onRecordAudioFrame) , e.g. 1024 in transcoding publish stream. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setRecordingAudioFrameParameters)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setPlaybackAudioFrameParameters

```c++
virtual int Thunder::IThunderEngine::setPlaybackAudioFrameParameters(int sampleRate,
 int channel,
 ThunderAudioRawFrameOperationMode mode,
 int samplesPerCall);
```

Set the mode for using raw audio playback data during callback [onPlaybackAudioFrame](notification.md#IAudioFrameObserver::onPlaybackAudioFrame)

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setPlaybackAudioFrameParameters)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sampleRate | IN | Sampling rate |
| channel | IN | Audio track; 1: Single track; 2: dual track |
| mode | IN | [Mode of using onPlaybackAudioFrame](notification.md#IAudioFrameObserver::onPlaybackAudioFrame). For details about the parameter value, see Thunder::[ThunderAudioRawFrameOperationMode.](#ThunderAudioRawFrameOperationMode) |
| samplesPerCall | IN | Sampling number of returned data in specified [onPlaybackAudioFrame](notification.md#IAudioFrameObserver::onPlaybackAudioFrame). For example, the value is 1024 in transcoding and stream publishing. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setPlaybackAudioFrameParameters)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLogFilePath

```c++
virtual int Thunder::IThunderEngine::setLogFilePath(const char* filePath);
```

Set directory for SDK to output log files.

> **Note:**
>
> - Ensure that the specified directory has write permission.

##### Parameter[](#setLogFilePath)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| filePath | IN | Complete list of log files |

##### Return[](#setLogFilePath)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLogLevel

```c++
virtual int Thunder::IThunderEngine::setLogLevel(LOG_FILTER filter);
```

Set the log storage level. Logs with lower level (LogLevel) will be filtered. Only logs with the log level indicated by this value or higher than this value are recorded.

##### Parameter[](#setLogLevel)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| filter | IN | For details about the log filtering level, see Thunder::[LOG_FILTER.](#LOG_FILTER) |

##### Return[](#setLogLevel)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::registerVideoFrameObserver

```c++
virtual int Thunder::IThunderEngine::registerVideoFrameObserver(IVideoFrameObserver* observer);
```

Register video frame data observer [IVideoFrameObserver](notification.md#IVideoFrameObserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - The user must inherit the [IVideoFrameObserver](notification.md#IVideoFrameObserver) interface class and implement the virtual methods. These methods will be used to call related original video data.

##### Parameter[](#registerVideoFrameObserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IVideoFrameObserver](notification.md#IVideoFrameObserver) interface class Registration is canceled if it is set to null. |

##### Return[](#registerVideoFrameObserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::getVideoDeviceMgr

```c++
virtual Thunder::IVideoDeviceManager* Thunder::IThunderEngine::getVideoDeviceMgr();
```

Register video frame data observer [IVideoFrameObserver](notification.md#IVideoFrameObserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#getVideoDeviceMgr)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setVideoEncoderConfig

```c++
virtual int Thunder::IThunderEngine::setVideoEncoderConfig(const VideoEncoderConfiguration& config);
```

Set video encoding configuration. Detailed description:

- SDK will acquire specific video encoding parameters for video encoding from the configured server in accordance with parameter configuration. If the service entails special parameter demand for video encoding, contact Technical Support for personalized configuration.
- If the video has been published, update the video encoding parameters. The updated video effect can be seen from local review and remote subscription.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setVideoEncoderConfig)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| config | IN | Specific code configuration. For details about the parameter value, see Thunder::[VideoEncoderConfiguration.](#VideoEncoderConfiguration) |

##### Return[](#setVideoEncoderConfig)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLocalVideoCanvas

```c++
virtual int Thunder::IThunderEngine::setLocalVideoCanvas(const VideoCanvas& canvas);
```

Set the rendering view of the local video.

- You can preview and publish without setting this window.
- You can see locally captured pictures by setting this window.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setLocalVideoCanvas)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| canvas | IN | Reference of rendering object [VideoCanvas](#VideoCanvas) |

##### Return[](#setLocalVideoCanvas)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setRemoteVideoCanvas

```c++
virtual int Thunder::IThunderEngine::setRemoteVideoCanvas(const VideoCanvas& canvas);
```

Set the rendering view of the remote video.

- You can subscribe without setting this window.
- After setting of this window, you can see video view of corresponding user through remote subscription.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setRemoteVideoCanvas)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| canvas | IN | Reference of rendering object [VideoCanvas](#VideoCanvas) |

##### Return[](#setRemoteVideoCanvas)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLocalCanvasScaleMode

```c++
virtual int Thunder::IThunderEngine::setLocalCanvasScaleMode(VideoRenderMode mode);
```

Set local view display mode.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setLocalCanvasScaleMode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#VideoRenderMode) |

##### Return[](#setLocalCanvasScaleMode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setRemoteCanvasScaleMode

```c++
virtual int Thunder::IThunderEngine::setRemoteCanvasScaleMode(VideoRenderMode mode);
```

Set the remote play type.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setRemoteCanvasScaleMode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#VideoRenderMode) |

##### Return[](#setRemoteCanvasScaleMode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::startVideoPreview

```c++
virtual int Thunder::IThunderEngine::startVideoPreview();
```

Start camera video preview.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#startVideoPreview)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#VideoRenderMode) |

##### Return[](#startVideoPreview)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopVideoPreview

```c++
virtual int Thunder::IThunderEngine::stopVideoPreview();
```

Stop camera video preview.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#stopVideoPreview)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#VideoRenderMode) |

##### Return[](#stopVideoPreview)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::enableLocalVideoCapture

```c++
virtual int Thunder::IThunderEngine::enableLocalVideoCapture(bool enabled);
```

Enable/Disable local video capture.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#enableLocalVideoCapture)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable local video capture; <br>false: Disable local video capture |

##### Return[](#enableLocalVideoCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopLocalVideoStream

```c++
virtual int Thunder::IThunderEngine::stopLocalVideoStream(bool stop);
```

Enable/Disable local video sending.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#stopLocalVideoStream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | True: Disable local video sending; false: Enable local video sending<br> |

##### Return[](#stopLocalVideoStream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopRemoteVideoStream

```c++
virtual int Thunder::IThunderEngine::stopRemoteVideoStream(const char* uid, bool stop);
```

Stop/Receive designated remote video.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called
> - Determine whether to receive or disable remote users. Check the value of this function first. If no value is found, use the value of [stopAllRemoteVideoStreams](#IThunderEngine::stopAllRemoteVideoStreams)

##### Parameter[](#stopRemoteVideoStream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | IN | User id |
| Stop | IN | true: Stop remote video of a specified user; false: Receive remote video of a specified user<br> |

##### Return[](#stopRemoteVideoStream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopAllRemoteVideoStreams

```c++
virtual int Thunder::IThunderEngine::stopAllRemoteVideoStreams(bool stop);
```

Stop/Receive all remote videos.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.
> - Determine whether to receive or disable remote users. Check the value of [stopRemoteVideoStream](#IThunderEngine::stopRemoteVideoStream) first. If no value is found, use the value of this function

##### Parameter[](#stopAllRemoteVideoStreams)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Stop all remote video; false; Receive all remote video. The default value is false<br><br> |

##### Return[](#stopAllRemoteVideoStreams)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLocalVideoMirrorMode

```c++
virtual int Thunder::IThunderEngine::setLocalVideoMirrorMode(ThunderVideoMirrorMode mode);
```

Set local video mirror mode

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called.
> - Set the mirror mode for local preview and that visible to viewers respectively.

##### Parameter[](#setLocalVideoMirrorMode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Mirror mode. For details about the parameter value, see Thunder::[ThunderVideoMirrorMode](#ThunderVideoMirrorMode) |

##### Return[](#setLocalVideoMirrorMode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setVideoWatermark

```c++
virtual int Thunder::IThunderEngine::setVideoWatermark(const Thunder::ThunderBoltImage& watermark);
```

Add local video watermark.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - Currently, only one watermark is supported. A newly added watermark will replace the existing one.
> - Only 24-bit and 32-bit pictures are supported. SDK will transform the pictures to the configured width.

##### Parameter[](#setVideoWatermark)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| watermark | IN | Reference of watermark picture object to be added to local live streaming push. For details about the picture format, see Thunder::[ThunderBoltImage](#ThunderBoltImage) |

##### Return[](#setVideoWatermark)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::removeVideoWatermarks

```c++
virtual int Thunder::IThunderEngine::removeVideoWatermarks();
```

Remove the local video watermark added.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#removeVideoWatermarks)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setCustomAudioSource

```c++
virtual int Thunder::IThunderEngine::setCustomAudioSource(bool bEnable, CustomAudioOptions& option);
```

Set parameters for external audio capture.

> **Note:**
>
> - This interface should be called after you perform initialization ([initialize](#IThunderEngine::initialize)) and before you call ([stopLocalAudioStream(false)](#IThunderEngine::stopLocalAudioStream) to publish audio.

##### Parameter[](#setCustomAudioSource)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| bEnable | IN | true: enable external audio capture <br>false: disable external audio capture (by default) |
| option | IN | External audio capture parameter. It is the reference of [CustomAudioOptions](#CustomAudioOptions) |

##### Return[](#setCustomAudioSource)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::pushCustomAudioFrame

```c++
virtual int Thunder::IThunderEngine::pushCustomAudioFrame(const char* pData, unsigned dataLen, unsigned timeStamp);
```

Push external audio frame.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#pushCustomAudioFrame)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| pData | IN | PCM audio frame data |
| dataLen | IN | Data length |
| timeStamp | IN | Capture timestamp |

##### Return[](#pushCustomAudioFrame)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setCustomVideoSource

```c++
virtual int Thunder::IThunderEngine::setCustomVideoSource(bool bEnable, CustomVideoOptions& option)
```

Set parameters for external video capture.

> **Note:**
>
> - This interface should be called after you perform initialization ([initialize](#IThunderEngine::initialize)) and before you call ([stopLocalVideoStream(false)](#IThunderEngine::stopLocalVideoStream)) to publish video.

##### Parameter[](#setCustomVideoSource)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| bEnable | IN | true: enable external audio capture <br>false: disable external audio capture (by default) |
| option | IN | External video capture parameter. It is the reference of [CustomVideoOptions](#CustomVideoOptions) |

##### Return[](#setCustomVideoSource)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::pushCustomVideoFrame

```c++
virtual int Thunder::IThunderEngine::pushCustomVideoFrame(const unsigned char* yuv[3], int linesize[3], unsigned timestamp);
```

Push external video frame.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#pushCustomVideoFrame)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| yuv | IN | YUV video data |
| linesize | IN | Line size of the buffer zone in YUV data |
| timestamp | IN | Capture timestamp |

##### Return[](#pushCustomVideoFrame)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::addPublishOriginStreamUrl

```c++
virtual int Thunder::IThunderEngine::addPublishOriginStreamUrl(const char* url);
```

Add the source stream publishing address.

- After this interface is called, the server will push source streams to the matching URL after publishing starts. Only one-channel stream publishing address can be added each time by this method. If multi-channel streams need to be pushed, this method have to be called repeatedly.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.
> - A maximum of 5 addresses are supported for stream publishing

##### Parameter[](#addPublishOriginStreamUrl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#addPublishOriginStreamUrl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::removePublishOriginStreamUrl

```c++
virtual int Thunder::IThunderEngine::removePublishOriginStreamUrl(const char* url);
```

Remove the source stream publishing address.

##### Parameter[](#removePublishOriginStreamUrl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#removePublishOriginStreamUrl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::setLiveTranscodingTask

```c++
virtual int Thunder::IThunderEngine::setLiveTranscodingTask(const char* taskId, const LiveTranscoding& transcodingCfg);
```

Add/update transcoding task.

- After this interface is called, the server will perform transcoding and push streams (if any) according to the configured canvas. Application programs must specify taskIds to distinguish different transcoding tasks.
- During transcoding, this interface can be repeatedly called to update transcoding parameters.
- One room supports a maximum of 5 transcoding tasks.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#setLiveTranscodingTask)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID, which is unique in a room and is managed by users |
| transcodingCfg | IN | Specific transcoding layout. For details, see Thunder::[LiveTranscoding](#LiveTranscoding) |

##### Return[](#setLiveTranscodingTask)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::removeLiveTranscodingTask

```c++
virtual int Thunder::IThunderEngine::removeLiveTranscodingTask(const char* taskId);
```

Remove a transcoding task.

- After this interface is called, AIVACOM background will terminate and delete stream mixing tasks.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removeLiveTranscodingTask)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID, which is unique in a room and is managed by users |

##### Return[](#removeLiveTranscodingTask)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::addPublishTranscodingStreamUrl

```c++
virtual int Thunder::IThunderEngine::addPublishTranscodingStreamUrl(const char* taskId, const char* url);
```

Add a stream publishing address of a transcoding stream.

- After this interface is called, the specified stream mixing will be pushed to the specified CDN address. Only one-channel stream publishing address can be added each time by this method. If multi-channel streams need to be pushed, this method have to be called repeatedly.
- One transcoding task supports a maximum of 5 addresses for stream publishing

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#addPublishTranscodingStreamUrl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#addPublishTranscodingStreamUrl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::removePublishTranscodingStreamUrl

```c++
virtual int Thunder::IThunderEngine::removePublishTranscodingStreamUrl(const char* taskId, const char* url);
```

Remove stream publishing address for transcoding stream.

- After this interface is called, the specified mixed stream will not be pushed to the specified CDN address.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removePublishTranscodingStreamUrl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#removePublishTranscodingStreamUrl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::addSubscribe

```c++
virtual int Thunder::IThunderEngine::addSubscribe(const char* roomId, const char* uid);
```

Subscribe to specific streams (cross-room).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#addSubscribe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#addSubscribe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::removeSubscribe

```c++
virtual int Thunder::IThunderEngine::removeSubscribe(const char* roomId, const char* uid);
```

Unsubscribe specified streams.

- After this interface is called, the specified mixed stream will not be pushed to the specified CDN address.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removeSubscribe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#removeSubscribe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::enableWebSdkCompatibility

```c++
virtual int Thunder::IThunderEngine::enableWebSdkCompatibility(bool enabled);
```

Enable/Disable WebSDK compatibility.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called
> - This method is applicable only to the live streaming scenario. Microphone connection is compatible with Web SDK by default, without calling this method.
> - Enable compatibility with WebSDK in live streaming. This interface must be called before publishing, which is irrelevant with entering or leaving the room.

##### Parameter[](#enableWebSdkCompatibility)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | Whether compatibility is enabled. Disabled by default |

##### Return[](#enableWebSdkCompatibility)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::sendUserAppMsgData

```c++
virtual int Thunder::IThunderEngine::sendUserAppMsgData(const char* msgData);
```

Send custom broadcast message of service.

This interface sends messages via media UDP channel with features of low-lantency and unreliability. Specified constraints are as follows:

- The sender must join the room.
- Call the interface after successfully opening microphone (messages cannot be sent if there are only audiences or broadcast authentication is failed).
- This interface should be called with a frequency of less than twice each second. msgData should not exceed 200 bytes.
- msg will be dropped if any of the conditions above is not met.
- The messages cannot be guaranteed to be delivered to all online users in room, and cannot be guaranteed be delivered in order.
- Monitor and notify causes for failure in sending customized broadcast messages through [onSendAppMsgDataFailedStatus](notification.md#IThunderEventHandler::onSendAppMsgDataFailedStatus).
- Monitor customized broadcast messages sent from other users through [onRecvUserAppMsgData](notification.md#IThunderEventHandler::onRecvUserAppMsgData).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#sendUserAppMsgData)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| msgData | IN | Service customized broadcast message |

##### Return[](#sendUserAppMsgData)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::sendMediaExtraInfo

```c++
virtual int Thunder::IThunderEngine::sendMediaExtraInfo(const char* extraData);
```

Send media extra information (audio/video has been published). Usage description:

- The sender must join the room, and call it after successfully publishing audio.
- Audio publishing only: This interface is called every 100 ms at best. The media extra information cannot exceed 200 bytes.
- Video publishing: The call frequency cannot exceed the frame rate. The media extra information cannot exceed 2048 bytes.
- For example: Stream publishing applies default frame rate of 15 FPS, that is, the calling frequency cannot exceed 66.7 ms/time (1000/15).
- Packet loss may occur.
- SDK will try to call back media data at the time when related frames are played.
- Monitor causes for failure in sending media extra information through [onSendMediaExtraInfoFailedStatus](notification.md#IThunderMediaExtraInfoObserver::onSendMediaExtraInfoFailedStatus).
- Monitor media extra information sent from other users through [onRecvMediaExtraInfo](notification.md#IThunderMediaExtraInfoObserver::onRecvMediaExtraInfo).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#sendMediaExtraInfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| extraData | IN | Media extra information |

##### Return[](#sendMediaExtraInfo)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::enableMixVideoExtraInfo

```c++
virtual int Thunder::IThunderEngine::enableMixVideoExtraInfo(bool enabled);
```

Enable video mixing with media extra information.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#IThunderEngine::joinRoom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#enableMixVideoExtraInfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | The default value is false. true: Enable video mixing with media extra information; false: Disable video mixing with media extra information. |

##### Return[](#enableMixVideoExtraInfo)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::startScreenCaptureForHwnd

```c++
virtual int Thunder::IThunderEngine::startScreenCaptureForHwnd(HWND hWnd, const RECT* pRect);
```

Start capturing specific screen.

##### Parameter[](#startScreenCaptureForHwnd)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| hWnd | IN | Window handle |
| pRect | IN | Sub region captured from a window. The coordinates are relative values. The coordinate of the point in the upper left corner is (0,0). The entire window is captured if the value is NULL. |

##### Return[](#startScreenCaptureForHwnd)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::startScreenCaptureForScreen

```c++
virtual int Thunder::IThunderEngine::startScreenCaptureForScreen(int screenId = 0, const RECT* pRect);
```

Start capturing specific region on desktop.

##### Parameter[](#startScreenCaptureForScreen)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| screenId | IN | Monitor ID |
| pRect | IN | Sub region specified for capturing. The coordinate is a relative value of the monitor. The entire monitor screen is captured when this parameter is set to NULL. |

##### Return[](#startScreenCaptureForScreen)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::updateScreenCaptureRect

```c++
virtual int Thunder::IThunderEngine::updateScreenCaptureRect(const RECT* pRect);
```

Update the displayed region for capturing.

##### Parameter[](#updateScreenCaptureRect)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| pRect | IN | Sub region specified for capturing. The coordinate is a relative value of the monitor or screen. The entire monitor screen or window is captured when this parameter is set to NULL. |

##### Return[](#updateScreenCaptureRect)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::stopScreenCapture

```c++
virtual int Thunder::IThunderEngine::stopScreenCapture();
```

Stop capturing the desktop or window.

##### Return[](#stopScreenCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::pauseScreenCapture

```c++
virtual int Thunder::IThunderEngine::pauseScreenCapture();
```

Pause capturing the desktop or window.

##### Return[](#pauseScreenCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::resumeScreenCapture

```c++
virtual int Thunder::IThunderEngine::resumeScreenCapture(const char* roomId, const char* uid);
```

Resume capturing the desktop or window.

##### Return[](#resumeScreenCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::registerVideoCaptureObserver

```c++
virtual int Thunder::IThunderEngine::registerVideoCaptureObserver(IVideoCaptureObserver* observer);
```

Register observer object for collecting data of camera.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#registerVideoCaptureObserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IVideoCaptureObserver](notification.md#IVideoCaptureObserver) object. If observer is NULL, monitoring is canceled. |

##### Return[](#registerVideoCaptureObserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::registerMediaExtraInfoObserver

```c++
virtual int Thunder::IThunderEngine::registerMediaExtraInfoObserver(IThunderMediaExtraInfoObserver* observer);
```

Register the observer object of media extra information.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#registerMediaExtraInfoObserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IThunderMediaExtraInfoObserver](notification.md#IThunderMediaExtraInfoObserver) object. If observer is NULL, monitoring is canceled. |

##### Return[](#registerMediaExtraInfoObserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderEngine::createThunderAudioPlayer

```c++
virtual IThunderAudioPlayer* Thunder::IThunderEngine::createThunderAudioPlayer();
```

Create an object for audio file player. For details, see [IThunderAudioPlayer](#IThunderAudioPlayer).

##### Return[](#createThunderAudioPlayer)

- IThunderAudioPlayer*: Pointer of the audio file player object
- NULL: Creating audio file player failed.

--------------------------

#### IThunderEngine::destroyThunderAudioPlayer

```c++
virtual int Thunder::IThunderEngine::destroyThunderAudioPlayer(IThunderAudioPlayer* player);
```

Destroy audio file player.

##### Parameter[](#destroyThunderAudioPlayer)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| player | IN | [Pointer of the IThunderAudioPlayer](#IThunderAudioPlayer) object |

##### Return[](#destroyThunderAudioPlayer)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

### IAudioDeviceManager

#### IAudioDeviceManager::enumInputDevices

```c++
virtual int Thunder::IAudioDeviceManager::enumInputDevices(AudioDeviceList& devices);
```

Enumerate audio input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#enumInputDevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | Information about the audio device. For details, see [AudioDeviceList.](#AudioDeviceList) |

##### Return[](#enumInputDevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setInputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingDevice(GUID& id);
```

Set audio input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setInputtingDevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | IN | Unique descriptor for a device |

##### Return[](#setInputtingDevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getInputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingDevice(GUID& id);
```

Obtain the currently selected input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getInputtingDevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | OUT | Unique descriptor for a device |

##### Return[](#getInputtingDevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setInputtingVolume

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingVolume(int volume);
```

Set the volume of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setInputtingVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume value [0-400] |

##### Return[](#setInputtingVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getInputtingVolume

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingVolume(int volume);
```

Obtain the volume of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getInputtingVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-400] |

##### Return[](#getInputtingVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setInputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingMute(bool mute);
```

Mute the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setInputtingMute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | IN | true: mute; false: unmute<br> |

##### Return[](#setInputtingMute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getInputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingMute(bool& mute);
```

Obtain the mute status of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getInputtingMute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | OUT | true: mute; false: unmute<br> |

##### Return[](#getInputtingMute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::startInputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::startInputDeviceTest(int indicationInterval);
```

Start testing the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - After calling this interface, you will receive an [onInputVolume](notification.md#IThunderEventHandler::onInputVolume) notification.

##### Parameter[](#startInputDeviceTest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| indicationInterval | IN | Check interval. The default value is 0. |

##### Return[](#startInputDeviceTest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::stopInputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::stopInputDeviceTest();
```

Stop testing the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#stopInputDeviceTest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::enumOutputDevices

```c++
virtual int Thunder::IAudioDeviceManager::enumOutputDevices(AudioDeviceList& devices);
```

Enumerate audio playback devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#enumOutputDevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | List of audio playback devices. For details, see [AudioDeviceList.](#AudioDeviceList) |

##### Return[](#enumOutputDevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setOutputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::setOutputtingDevice(GUID& id);
```

Specify the audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setOutputtingDevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | IN | Unique descriptor for a device |

##### Return[](#setOutputtingDevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getOutputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::getOutputtingDevice(GUID& id);
```

Obtain the current audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getOutputtingDevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | OUT | Unique descriptor for a device |

##### Return[](#getOutputtingDevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setOuttingVolume

```c++
virtual int Thunder::IAudioDeviceManager::setOuttingVolume(int volume);
```

Set the volume of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setOuttingVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume value [0-400] |

##### Return[](#setOuttingVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getOuttingVolume

```c++
virtual int Thunder::IAudioDeviceManager::getOuttingVolume(int& volume);
```

Obtain the volume of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getOuttingVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-400] |

##### Return[](#getOuttingVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::setOutputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::setOutputtingMute(bool mute);
```

Mute/Unmute the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#setOutputtingMute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | IN | true: mute; false: unmute<br> |

##### Return[](#setOutputtingMute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::getOutputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::getOutputtingMute(bool& mute);
```

Obtain the mute status of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#getOutputtingMute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | OUT | true: mute; <br>false: unmute |

##### Return[](#getOutputtingMute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::startOutputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::startOutputDeviceTest(int indicationInterval, const char* audioFileName);
```

Start testing the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).
> - Calling the [setOutputtingDevice](#IAudioDeviceManager::setOutputtingDevice) interface will also terminate the test.

##### Parameter[](#startOutputDeviceTest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| indicationInterval | IN | Check interval. The default value is 0. |
| audioFileName | IN | Full path of the audio file that is played. Win7 and higher support mp3, aac, and wave formats while versions earlier than Win7 support only the wav format. |

##### Return[](#startOutputDeviceTest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::stopOutputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::stopOutputDeviceTest();
```

Stop testing the current audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#stopOutputDeviceTest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#stopOutputDeviceTest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::enableMicEnhancement

```c++
virtual int Thunder::IAudioDeviceManager::enableMicEnhancement(bool enabled);
```

Enable/Disable microphone enhancement.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called

##### Parameter[](#enableMicEnhancement)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable microphone enhancement; false: Disable microphone enhancement. The default value is false. |

##### Return[](#enableMicEnhancement)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::enableMicDenoise

```c++
virtual int Thunder::IAudioDeviceManager::enableMicDenoise(bool enabled);
```

Enable/Disable microphone noise reduction.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called

##### Parameter[](#enableMicDenoise)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable microphone noise reduction; false: Disable microphone noise reduction. The default value is false. |

##### Return[](#enableMicDenoise)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::enableAEC

```c++
virtual int Thunder::IAudioDeviceManager::enableAEC(bool enabled);
```

Enable/Disable AEC.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called

##### Parameter[](#enableAEC)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable AEC; false: Disable AEC. The default value is false. |

##### Return[](#enableAEC)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IAudioDeviceManager::enableAGC

```c++
virtual int Thunder::IAudioDeviceManager::enableAGC(bool enabled);
```

Enable/Disable Automatic Gain Control (AGC).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)). This interface is reset only when [destroyEngine](#IThunderEngine::destroyEngine) is called

##### Parameter[](#enableAGC)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable AEC; false: Disable AEC. The default value is false. |

##### Return[](#enableAGC)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

### IThunderAudioPlayer

#### IThunderAudioPlayer::open

```c++
virtual bool Thunder::IThunderAudioPlayer::open(const char* path);
```

Open a specified file.

##### Parameter[](#open)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| path | Absolute file path |

##### Return[](#open)

- true: Opening file succeeded
- false: Opening file failed

--------------------------

#### IThunderAudioPlayer::close

```c++
virtual void Thunder::IAudioDeviceManager::close();
```

Close the current file.

--------------------------

#### IThunderAudioPlayer::play

```c++
virtual void Thunder::IAudioDeviceManager::play();
```

Play a file that has been opened.

> **Note:**
>
> - Before playing a file, call IThunderAudioPlayer::[open](#IThunderAudioPlayer::open) to open it first.

--------------------------

#### IThunderAudioPlayer::stop

```c++
virtual void Thunder::IAudioDeviceManager::stop();
```

Stop playing.

--------------------------

#### IThunderAudioPlayer::pause

```c++
virtual void Thunder::IAudioDeviceManager::pause();
```

Pause playing a file that has been opened.

--------------------------

#### IThunderAudioPlayer::resume

```c++
virtual void Thunder::IAudioDeviceManager::resume();
```

Pause playing a file that has been opened.

--------------------------

#### IThunderAudioPlayer::seek

```c++
virtual void Thunder::IAudioDeviceManager::seek(unsigned int timeMS);
```

Jump to a specified time for play.

> **Note:**
>
> - Ensure that the file is in playback state.
> - The value cannot be greater than that obtained by [getTotalPlayTimeMS](#IThunderAudioPlayer::getTotalPlayTimeMS).

##### Parameter[](#seek)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| timeMS | IN | Specified time, unit: ms |

--------------------------

#### IThunderAudioPlayer::getTotalPlayTimeMS

```c++
virtual unsigned int Thunder::IAudioDeviceManager::getTotalPlayTimeMS();
```

Get the total play time of files.

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#IThunderAudioPlayer::open) to open the file first.

##### Return[](#getTotalPlayTimeMS)

- Total duration for playing a file

--------------------------

#### IThunderAudioPlayer::getCurrentPlayTimeMS

```c++
virtual unsigned int Thunder::IAudioDeviceManager::getCurrentPlayTimeMS();
```

Get the time which has been played.

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#IThunderAudioPlayer::open) to open the file and play it.

##### Return[](#getCurrentPlayTimeMS)

- Played duration

--------------------------

#### IThunderAudioPlayer::setPlayerLocalVolume

```c++
virtual int Thunder::IAudioDeviceManager::setPlayerLocalVolume(int volume);
```

Adjusts volume size when music files are played on local end.

##### Parameter[](#setPlayerLocalVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Play volume [0-100] |

##### Return[](#setPlayerLocalVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderAudioPlayer::setPlayerPublishVolume

```c++
virtual int Thunder::IAudioDeviceManager::setPlayerPublishVolume(int volume);
```

Adjust the publish volume of the music file.

##### Parameter[](#setPlayerPublishVolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Play volume [0-100] |

##### Return[](#setPlayerPublishVolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderAudioPlayer::getPlayerLocalVolume

```c++
virtual int Thunder::IAudioDeviceManager::getPlayerLocalVolume();
```

Get the local volume of music files. The value matches that configured by setPlayerLocalVolume. The range is [0-100].

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#IThunderAudioPlayer::open) to open the file and play it.

##### Return[](#getPlayerLocalVolume)

- Volume of the music file when played locally

--------------------------

#### IThunderAudioPlayer::getPlayerPublishVolume

```c++
virtual int Thunder::IAudioDeviceManager::getPlayerPublishVolume();
```

Obtain the publish volume of the music file. The value matches that configured by setPlayerPublishVolume. The range is [0-100].

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#IThunderAudioPlayer::open) to open the file and play it.

##### Return[](#getPlayerPublishVolume)

- Publish volume of the music file

--------------------------

#### IThunderAudioPlayer::setLooping

```c++
virtual int Thunder::IAudioDeviceManager::setLooping(int cycle);
```

Sets times of loop playbacks.

##### Parameter[](#setLooping)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| cycle | IN | -1: indicates infinite loop; 0: No loop (default value); Positive integer: Loop times |

##### Return[](#setLooping)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IThunderAudioPlayer::SetFilePlayerNotify

```c++
virtual void Thunder::IAudioDeviceManager::void SetFilePlayerNotify(IThunderAudioPlayerNotify* notify);
```

Set playback callback.

##### Parameter[](#SetFilePlayerNotify)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| notify | IN | Interface class of the playback callback. For details, see [IThunderAudioPlayerNotify.](#IThunderAudioPlayerNotify) |

--------------------------

### IVideoDeviceManager

#### IVideoDeviceManager::enumVideoDevices

```c++
virtual int Thunder::IVideoDeviceManager::enumVideoDevices(VideoDeviceList& devices);
```

Enumerate video input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#enumVideoDevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | List of video input devices. For details, see [VideoDeviceList.](#VideoDeviceList) |

##### Return[](#enumVideoDevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IVideoDeviceManager::startVideoDeviceCapture

```c++
virtual int Thunder::IVideoDeviceManager::startVideoDeviceCapture(int index);
```

Start the video input device and initiate collection.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#startVideoDeviceCapture)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| index | IN | Device index |

##### Return[](#startVideoDeviceCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IVideoDeviceManager::stopVideoDeviceCapture

```c++
virtual int Thunder::IVideoDeviceManager::stopVideoDeviceCapture();
```

Stop video device capture.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Return[](#stopVideoDeviceCapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

#### IVideoDeviceManager::enumMonitorDevices

```c++
virtual int Thunder::IVideoDeviceManager::enumMonitorDevices(MonitorDeviceList& devices);
```

Enumerate monitor input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#IThunderEngine::initialize)).

##### Parameter[](#enumMonitorDevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | Returned list of video input devices. For details, see [MonitorDeviceList.](#MonitorDeviceList) |

##### Return[](#enumMonitorDevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](./code.md#ThunderRet)

--------------------------

## Enumerated values & structure definition

#### AREA_TYPE

```c++
enum Thunder::AREA_TYPE
```

Area type

| Enumerated values | Meaning |
| :--- | :--- |
| AREA_DEFAULT(0) | Domestic, default value |
| AREA_FOREIGN(1) | Overseas |
| AREA_RESERVED(2) | Reserved |

--------------------------

#### THUNDER_PROFILE

```c++
enum Thunder::THUNDER_PROFILE
```

Media mode

| Enumerated values | Meaning |
| :--- | :--- |
| PROFILE_DEFAULT(0) | Default mode (audio/video mode) |
| PROFILE_NORMAL(1) | Audio/video mode |
| PROFILE_ONLY_AUDIO(2) | Audio-only mode, applicable to audio-only optimization |

--------------------------

#### ROOM_CONFIG_TYPE

```c++
enum Thunder::ROOM_CONFIG_TYPE
```

Media mode

| Enumerated values | Meaning |
| :--- | :--- |
| ROOM_CONFIG_LIVE(0) | Live streaming mode, where quality is prioritized and delay is large. Applicable to viewer or audience scenario. When audience publishes audio/video and becomes anchors, the value changes to communication mode. |
| ROOM_CONFIG_COMMUNICATION(1) | Communication mode is applicable for 1v1 communication and group conversation due to its short time delay and fluent communication. |
| ROOM_CONFIG_MultiAudioRoom(4) | Audio room mode is applicable for group audio room due to its low time delay and low bandwidth occupied |

--------------------------

#### AUDIO_PROFILE_TYPE

```c++
enum Thunder::AUDIO_PROFILE_TYPE
```

Audio type

| Enumerated values | Meaning |
| :--- | :--- |
| AUDIO_PROFILE_DEFAULT(0) | Default type, which is AUDIO_PROFILE_SPEECH_STANDARD. |
| AUDIO_PROFILE_SPEECH_STANDARD(1) | Specify the sampling rate of 16 KHz. Speech encoding, single sound track, encoding rate of about 18 kbps |
| AUDIO_PROFILE_MUSIC_STANDARD_STEREO(2) | Specify the sampling rate of 44.1 KHz. Music encoding, dual sound tracks, encoding rate of about 24 kbps, high encoding delay |
| AUDIO_PROFILE_MUSIC_STANDARD(3) | Specify the sampling rate of 44.1 KHz. Music encoding, dual sound tracks, encoding rate of about 48 kbps, low encoding delay |
| AUDIO_PROFILE_MUSIC_HIGH_QUALITY_STEREO(4) | Specify the sampling rate of 44.1KHz, music encoding, dual track, and encoding rate of around 128kbps |
| AUDIO_PROFILE_MUSIC_HIGHER_QUALITY = 5 | Specify the sampling rate of 44.1KHz, music encoding, dual track, and encoding rate of around 192kbps |

--------------------------

#### COMMUT_MODE

```c++
enum Thunder::COMMUT_MODE
```

Interactive mode

| Enumerated values | Meaning |
| :--- | :--- |
| COMMUT_MODE_DEFAULT(0) | Default type, which is COMMUT_MODE_DEFAULT. |
| COMMUT_MODE_HIGH(1) | High interactive mode |
| COMMUT_MODE_LOW(2) | Low interactive mode |

--------------------------

#### SCENARIO_MODE

```c++
enum Thunder::SCENARIO_MODE
```

Scenario mode

| Enumerated values | Meaning |
| :--- | :--- |
| SCENARIO_MODE_DEFAULT(0) | Default type, which is SCENARIO_MODE_STABLE_FIRST. |
| SCENARIO_MODE_STABLE_FIRST(1) | Smooth is prioritized. Recommended for use in education scenarios that require high stability. |
| SCENARIO_MODE_QUALITY_FIRST(2) | Tone quality is prioritized. Recommended for use in show scenarios where microphone connection is seldom required. |

--------------------------

#### ThunderSourceType

```c++
enum Thunder::ThunderSourceType
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_MIC(0) | Only microphone |
| THUNDER_AUDIO_FILE(1) | Only file |
| THUNDER_AUDIO_MIX(2) | Microphone and file |
| THUNDER_AUDIO_TYPE_NONE(10) | Stop all upstream audio data |

--------------------------

#### AUDIO_RECORDING_FILE_TYPE

```c++
enum Thunder::AUDIO_RECORDING_FILE_TYPE
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| AUDIO_RECORDING_WAV(0) | wav format |
| AUDIO_RECORDING_AAC(1) | aac format |
| AUDIO_RECORDING_MP3(2) | mp3 format |

--------------------------

#### AUDIO_RECORDING_QUALITY_TYPE

```c++
enum Thunder::AUDIO_RECORDING_QUALITY_TYPE
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| AUDIO_RECORDING_QUALITY_LOW(0) | Low tone quality |
| AUDIO_RECORDING_QUALITY_MEDIUM(1) | Mediocre tone quality |
| AUDIO_RECORDING_QUALITY_HIGH(2) | High tone quality |

--------------------------

#### ThunderAudioRawFrameOperationMode

```c++
enum Thunder::ThunderAudioRawFrameOperationMode
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_ONLY(1) | Read only mode. The user only acquires original data from AudioFrame |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_WRITE_ONLY(2) | Write only mode. The user replaces data in AudioFrame for encoding transmission of SDK |
| THUNDER_AUDIO_RAW_FRAME_OPERATION_MODE_READ_WRITE(3) | Read-write mode. The user obtains data from AudioFrame and modifies data. Then the data is returned to SDK for encoding and transmission. |

--------------------------

#### LOG_FILTER

```c++
enum Thunder::LOG_FILTER
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| LOG_LEVEL_TRACE(0) | TRACE |
| LOG_LEVEL_DEBUG(1) | DEBUG |
| LOG_LEVEL_INFO(2) | INFO |
| LOG_LEVEL_WARN(3) | WARN |
| LOG_LEVEL_ERROR(4) | ERROR |
| LOG_LEVEL_RELEASE (10) | RELEASE |

--------------------------

#### VideoEncoderConfiguration

```c++
struct Thunder::VideoEncoderConfiguration
{
 VideoPublishPlayType playType;
 VideoPublishMode publishMode;
};
```

Video encoding configuration

| Member | Meaning |
| :--- | :--- |
| [VideoPublishPlayType](#VideoPublishPlayType) | Publishing type |
| [VideoPublishMode](#VideoPublishMode) | Publishing bracket |

--------------------------

#### VideoPublishPlayType

```c++
enum Thunder::VideoPublishPlayType
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| VIDEO_PUBLISH_PLAYTYPE_SINGLE(0) | Single publishing |
| VIDEO_PUBLISH_PLAYTYPE_INTERACT(1) | Microphone-connection video publishing |
| VIDEO_PUBLISH_PLAYTYPE_SCREENCAP(2) | Screen recording publishing |

--------------------------

#### VideoPublishMode

```c++
enum Thunder::VideoPublishMode
```

Audio publishing mode

| Enumerated values | Meaning |
| :--- | :--- |
| VIDEO_PUBLISH_MODE_DEFAULT(-1) | Undefined. The publishing definition is determined by configuration |
| VIDEO_PUBLISH_MODE_SMOOTH_DEFINITION(1) | Fluent |
| VIDEO_PUBLISH_MODE_NORMAL_DEFINITION(2) | Standard definition |
| VIDEO_PUBLISH_MODE_HIGH_DEFINITION(3) | High definition |
| VIDEO_PUBLISH_MODE_SUPER_DEFINITION(4) | Ultra definition |
| VIDEO_PUBLISH_MODE_BLUERAY(5) | Blue light |

--------------------------

#### VideoCanvas

```c++
#define MAX_THUNDER_UID_LEN 65 // UID length

struct Thunder::VideoCanvas
{
 HWND hWnd;
 VideoRenderMode renderMode;
 char uid[MAX_THUNDER_UID_LEN];
};
```

Video encoding configuration

| Member | Meaning |
| :--- | :--- |
| HWND | Video rendering window |
| [VideoRenderMode](#VideoRenderMode) | Video rendering mode |
| char uid[MAX_THUNDER_UID_LEN] | User id |

--------------------------

#### VideoRenderMode

```c++
enum Thunder::VideoRenderMode
```

Video rendering mode

| Enumerated values | Meaning |
| :--- | :--- |
| VIDEO_RENDER_MODE_FILL(0) | Pull to full screen |
| VIDEO_RENDER_MODE_ASPECT_FIT(1) | Adapt to window |
| VIDEO_RENDER_MODE_CLIP_TO_BOUNDS(2) | Tailed to full screen |

--------------------------

#### ThunderVideoMirrorMode

```c++
enum Thunder::ThunderVideoMirrorMode
```

Mirror mode for local preview video and stream publishing video

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_MIRROR_PUBLISH_NO_MIRROR(0) | The preview other than stream publishing is mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_MIRROR(1) | Both the preview and stream publishing are mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_PUBLISH_BOTH_NO_MIRROR(2) | Neither the preview nor stream publishing is mirrored |
| THUNDER_VIDEO_MIRROR_MODE_PREVIEW_NO_MIRROR_PUBLISH_MIRROR(3) | The preview other than stream publishing is mirrored |

--------------------------

#### ThunderBoltImage

```c++
#define MAX_THUNDER_URL_LEN 512 // url length

struct Thunder::ThunderBoltImage
{
  int x; // Take the upper left corner as the original point, horizontal coordinate
  int y; // Take the upper left corner as the original point, vertical coordinate
  int width; // Width
  int height; // Height
  char url[MAX_THUNDER_URL_LEN]; // Absolute path address or http, https address of local picture
};
```

Picture information

--------------------------

#### CustomAudioOptions

```c++
struct CustomAudioOptions
{
  int sampleRate; // Sampling rate (48k,44.1,16k,8k)
  int channels; // Audio channel
  int bitpersample; // Bit width of sampling point (currently only 16 available)
  bool bMixSdkCapture; // Whether to synthesize the capture of SDK itself
};
```

External audio capture parameters

--------------------------

#### CustomVideoOptions

```c++
struct CustomVideoOptions
{
  enum CustomVideoSrcDataType
  {
    DATA_TYPE_I420 = 0,
    DATA_TYPE_NV12 = 1,
    DATA_TYPE_BGR24 = 2,
    DATA_TYPE_BGRA = 3,
  };

  int srcWidth; // Width and height of input source [dynamic update not available]
  int srcHeight; // Height of input source [dynamic update not available]
  int destWidth; // Width and height of output stream [this parameter has been deprecated and needs to be set according to the interface setVideoEncoderConfig]
  int destHeight; // Width and height of output stream [this parameter has been deprecated and needs to be set according to the interface setVideoEncoderConfig]
  int codeRate; // Specific value of bit rate (unit: kbps) [this parameter has been deprecated and needs to be set according to the interface setVideoEncoderConfig]
  CustomVideoSrcDataType srcDataType; // Data type of source stream
};
```

External video capture parameters.

--------------------------

#### LiveTranscoding

```c++
#define MAX_THUNDER_TRANSCODINGUSER_COUNT 9 // Number of users with maximum image transcoding
#define MAX_THUNDER_ROOMID_LEN 65 // roomId length
#define MAX_THUNDER_UID_LEN 65 // uid length

struct LiveTranscoding
{
  // Audio is unified by default to "encode": 1,"bitrate":128,"sample":44100,"channel":2
  enum TranscodingMode
  {
    TRANSCODING_MODE_320X180 = 1, // "encode":100,"bitrate":150,"fps":15,"gop":30,"height":180,"width":320
    TRANSCODING_MODE_320X240 = 2, // "encode":100,"bitrate":200,"fps":15,"gop":30,"height":240,"width":320
    TRANSCODING_MODE_640X360 = 3, // "encode":100,"bitrate":500,"fps":15,"gop":30,"height":360,"width":640
    TRANSCODING_MODE_640X480 = 4, // "encode":100,"bitrate":500,"fps":15,"gop":30,"height":480,"width":640
    TRANSCODING_MODE_960X544 = 5, // "encode":100,"bitrate":1000,"fps":24,"gop":48,"height":544,"width":960
    TRANSCODING_MODE_1280X720 = 6, // "encode":100,"bitrate":1600,"fps":24,"gop":48,"height":720,"width":1280
    TRANSCODING_MODE_1920X1080 = 7, // "encode":100,"bitrate":4500,"fps":24,"gop":48,"height":1080,"width":1920
  };

  LiveTranscoding() : transcodingMode(0), userCount(0) {}

  int transcodingMode; // Transcoding bracket (enum TranscodingMode)
  int userCount;
  TranscodingUser userList[MAX_THUNDER_TRANSCODINGUSER_COUNT];
  };

struct TranscodingUser
{
 TranscodingUser()
 : bStandard(false)
 , layoutX(0)
 , layoutY(0)
 , layoutW(0)
 , layoutH(0)
 , zOrder(0)
 , bCrop(false)
 , cropX(0)
 , cropY(0)
 , cropW(0)
 , cropH(0)
 , alpha(0)
 , audioChannel(0)
 {
 }

 bool bStandard; // Standard stream user or not
 int layoutX; // User's location x in video mixing canvas
 int layoutY; // User's location y in video mixing canvas
 int layoutW; // User’s width in video mixing canvas
 int layoutH; // User’s height in video mixing canvas
 int zOrder; // Layer number of the user’s video frame on the live video. The value range is the integer in [0, 100] (0 = lowest layer, 1 = first layer from bottom to top, and so on)
 bool bCrop; // 0: display in the middle after zooming, mend black edges on the upper and lower / left and right sides; 1: crop in the middle after zooming, and crop the upper and lower / left and right extra regions
 int cropX; // X coordinate of crop region, left blank means default to center cropping
 int cropY; // Y coordinate of crop region
 int cropW; // Width of crop region
 int cropH; // Height of crop region
 float alpha; // Transparency of user video on the live video. The value range is [0.0, 1.0]. 0.0 indicates that the image in this region is completely transparent, while 1.0
 // indicates completely opaque. The default is 1.0
 int audioChannel; // Not yet realized
 char uid[MAX_THUNDER_UID_LEN];
 char roomId[MAX_THUNDER_ROOMID_LEN];
};
```

Video mixing parameters

--------------------------

#### AudioDeviceList

```c++
#define MAX_DEVICE_NAME_LEN 512 // Device name
#define MAX_DEVICE_DESC_LEN 512 // Device description
#define MAX_DEVICE_COUNT 16 // Maximum quantity of devices

struct GUID
{
 unsigned long Data1;
 unsigned short Data2;
 unsigned short Data3;
 unsigned char Data4[8];
};

struct AudioDeviceInfo // Information about audio device
{
 GUID id; // Identification of audio device
 char name[MAX_DEVICE_NAME_LEN]; // Name of audio device
 char desc[MAX_DEVICE_DESC_LEN]; // Description of audio device
};

struct AudioDeviceList
{
 AudioDeviceInfo device[MAX_DEVICE_COUNT]; // List of audio devices
 int count; // Number of video devices
};
```

List of audio devices

--------------------------

#### MonitorDeviceList

```c++
#define MAX_DEVICE_NAME_LEN 512 // Device name
#define MAX_DEVICE_COUNT 16 // Maximum quantity of devices

struct RECT
{
 long left;
 long top;
 long right;
 long bottom;
};

struct MonitorDeviceInfo
{
 int index; // Acquired device number
 int flags; // Flags for screen attributes. The following table lists the possible values:
 // 0: This screen is not the home screen.
 // 1: This screen is the home screen, can also be identified by the macro MONITORINFOF_PRIMARY came with Windows
 void* handle; // pHandler to display monitor <==> HMONITOR
 RECT rcWork; // Rectangular working area of specified screen, represented in virtual screen coordinates
 RECT rcMonitor; // Rectangular specified screen, represented in virtual screen coordinates
 char name[MAX_DEVICE_NAME_LEN]; // Device name
};

struct MonitorDeviceList
{
 int count; // Number of video devices
 MonitorDeviceInfo device[MAX_DEVICE_COUNT]; // List of video devices
};

List of displayer information.

```

--------------------------

#### VideoDeviceList

```c++
struct VideoDeviceList
{
  VideoDeviceInfo device[MAX_DEVICE_COUNT]; // List of video devices
  int count; // Number of video devices
};
```

List of video devices

--------------------------

#### VideoDeviceInfo

```c++
struct VideoDeviceInfo
{
  char name[MAX_DEVICE_NAME_LEN]; // Name of video device
  int index; // Index of video device
};
```

Video device information

--------------------------
