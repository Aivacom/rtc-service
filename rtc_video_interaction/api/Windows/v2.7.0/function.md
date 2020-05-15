# Functional Interface

## Interface List

- 
   ### IThunderEngine

| Global Function | Function Name |
| ---:| :--- |
| Thunder::IThunderEngine* | [createEngine](#ithunderenginecreateengine)() |

| public member functions | Function Name |
| ---:| :--- |
| virtual void | [destroyEngine](#ithunderenginedestroyengine)() = 0 |
| virtual int | [initialize](#ithunderengineinitialize)(const char* appId, int sceneId, [IThunderEventHandler](notification.md#ithundereventhandler)* pHandler) = 0 |
| virtual int | [setArea](#ithunderenginesetarea)([AREA_TYPE](#area-type) area) = 0 |
| virtual int | [joinRoom](#ithunderenginejoinroom)(const char* token, int tokenLen, const char* roomId, const char* uid) = 0 |
| virtual int | [leaveRoom](#ithunderengineleaveroom)() = 0 |
| virtual int | [updateToken](#ithunderengineupdatetoken)(const char* token, int tokenLen) = 0 |
| virtual int | [setMediaMode](#ithunderenginesetmediamode)([THUNDER_PROFILE](#thunder-profile) mode) = 0 |
| virtual int | [setRoomMode](#ithunderenginesetroommode)([ROOM_CONFIG_TYPE](#room-config-type) mode) = 0 |
| virtual int | [setAudioConfig](#ithunderenginesetaudioconfig)([AUDIO_PROFILE_TYPE](#audio-profile-type) profile, [COMMUT_MODE](#commut-mode) commutMode, [SCENARIO_MODE](#scenario-mode) scenarioMode) = 0 |
| virtual int | [setAudioSourceType](#ithunderenginesetaudiosourcetype)([ThunderSourceType](#thundersourcetype) sourceType) = 0 |
| virtual int | [stopLocalAudioStream](#ithunderenginestoplocalaudiostream)(bool stop) = 0 |
| virtual int | [stopAllRemoteAudioStreams](#ithunderenginestopallremoteaudiostreams)(bool stop) = 0 |
| virtual int | [stopRemoteAudioStream](#ithunderenginestopremoteaudiostream)(const char* uid, bool stop) = 0 |
| virtual int | [setAudioVolumeIndication](#ithunderenginesetaudiovolumeindication)(int interval, int smooth) = 0 |
| virtual int | [enableLoopbackRecording](#ithunderengineenableloopbackrecording)(bool enabled) = 0 |
| virtual int | [startAudioRecording](#ithunderenginestartaudiorecording)(const char* fileName, [AUDIO_RECORDING_FILE_TYPE](#audio-recording-file-type) fileType, [AUDIO_RECORDING_QUALITY_TYPE](#audio-recording-quality-type) quality) = 0 |
| virtual int | [stopAudioRecording](#ithunderenginestopaudiorecording)() = 0 |
| virtual int | [adjustRecordingSignalVolume](#ithunderengineadjustrecordingsignalvolume)(int volume) = 0 |
| virtual int | [adjustPlaybackSignalVolume](#ithunderengineadjustplaybacksignalvolume)(int volume) = 0 |
| virtual [IAudioDeviceManager](#iaudiodevicemanager)* | [getAudioDeviceMgr](#ithunderenginegetaudiodevicemgr)() = 0 |
| virtual bool | [registerAudioFrameObserver](#ithunderengineregisteraudioframeobserver)([IAudioFrameObserver](#iaudiodevicemanager)* observer) = 0 |
| virtual int | [setRecordingAudioFrameParameters](#ithunderenginesetrecordingaudioframeparameters)(int sampleRate, int channel, [ThunderAudioRawFrameOperationMode](#thunderaudiorawframeoperationmode) mode, int samplesPerCall) = 0 |
| virtual int | [setPlaybackAudioFrameParameters](#ithunderenginesetplaybackaudioframeparameters)(int sampleRate, int channel, [ThunderAudioRawFrameOperationMode](#thunderaudiorawframeoperationmode) mode, int samplesPerCall) = 0 |
| virtual int | [setLogFilePath](#ithunderenginesetlogfilepath)(const char* filePath) = 0 |
| virtual int | [setLogLevel](#ithunderenginesetloglevel)([LOG_FILTER](#log-filter) filter) = 0 |
| virtual int | [registerVideoFrameObserver](#ithunderengineregistervideoframeobserver)([IVideoFrameObserver](#ivideoframeobserver)* observer) = 0 |
| virtual [IVideoDeviceManager](#ivideodevicemanager)* | [getVideoDeviceMgr](#ithunderenginegetvideodevicemgr)() = 0 |
| virtual int | [setVideoEncoderConfig](#ithunderenginesetvideoencoderconfig)(const [VideoEncoderConfiguration](#videoencoderconfiguration)& config) = 0 |
| virtual int | [setLocalVideoCanvas](#ithunderenginesetlocalvideocanvas)(const [VideoCanvas](#videocanvas)& canvas) = 0 |
| virtual int | [setRemoteVideoCanvas](#ithunderenginesetremotevideocanvas)(const [VideoCanvas](#videocanvas)& canvas) = 0 |
| virtual int | [setLocalCanvasScaleMode](#ithunderenginesetlocalcanvasscalemode)([VideoRenderMode](#videorendermode) mode) = 0 |
| virtual int | [setRemoteCanvasScaleMode](#ithunderenginesetremotecanvasscalemode)([VideoRenderMode](#videorendermode) mode) = 0 |
| virtual int | [startVideoPreview](#ithunderenginestartvideopreview)() = 0 |
| virtual int | [stopVideoPreview](#ithunderenginestopvideopreview)() = 0 |
| virtual int | [enableLocalVideoCapture](#ithunderengineenablelocalvideocapture)(bool enabled) = 0 |
| virtual int | [stopLocalVideoStream](#ithunderenginestoplocalvideostream)(bool stop) = 0 |
| virtual int | [stopRemoteVideoStream](#ithunderenginestopremotevideostream)(const char* uid, bool stop) = 0 |
| virtual int | [stopAllRemoteVideoStreams](#ithunderenginestopallremotevideostreams)(bool stop) = 0 |
| virtual int | [setLocalVideoMirrorMode](#ithunderenginesetlocalvideomirrormode)([ThunderVideoMirrorMode](#thundervideomirrormode) mode) = 0 |
| virtual int | [setVideoWatermark](#ithunderenginesetvideowatermark)(const [ThunderBoltImage](#thunderboltimage)& watermark) = 0 |
| virtual int | [removeVideoWatermarks](#ithunderengineremovevideowatermarks)() = 0 |
| virtual int | [setCustomAudioSource](#ithunderenginesetcustomaudiosource)(bool bEnable, [CustomAudioOptions](#customaudiooptions)& option) = 0 |
| virtual int | [pushCustomAudioFrame](#ithunderenginepushcustomaudioframe)(const char* pData, unsigned dataLen, unsigned timeStamp) = 0 |
| virtual int | [setCustomVideoSource](#ithunderenginesetcustomvideosource)(bool bEnable, [CustomVideoOptions](#customvideooptions)& option) = 0 |
| virtual int | [pushCustomVideoFrame](#ithunderenginepushcustomvideoframe)(const unsigned char* yuv[3], int linesize[3], unsigned timestamp) = 0 |
| virtual int | [addPublishOriginStreamUrl](#ithunderengineaddpublishoriginstreamurl)(const char* url) = 0 |
| virtual int | [removePublishOriginStreamUrl](#ithunderengineremovepublishoriginstreamurl)(const char* url) = 0 |
| virtual int | [setLiveTranscodingTask](#ithunderenginesetlivetranscodingtask)(const char* taskId, const [LiveTranscoding](#livetranscoding)& transcodingCfg) = 0 |
| virtual int | [removeLiveTranscodingTask](#ithunderengineremovelivetranscodingtask)(const char* taskId) = 0 |
| virtual int | [addPublishTranscodingStreamUrl](#ithunderengineaddpublishtranscodingstreamurl)(const char* taskId, const char* url) = 0 |
| virtual int | [removePublishTranscodingStreamUrl](#ithunderengineremovepublishtranscodingstreamurl)(const char* taskId, const char* url) = 0 |
| virtual int | [addSubscribe](#ithunderengineaddsubscribe)(const char* roomId, const char* uid) = 0 |
| virtual int | [removeSubscribe](#ithunderengineremovesubscribe)(const char* roomId, const char* uid) = 0 |
| virtual int | [enableWebSdkCompatibility](#ithunderengineenablewebsdkcompatibility)(bool enabled) = 0 |
| virtual int | [sendUserAppMsgData](#ithunderenginesenduserappmsgdata)(const char* msgData) = 0 |
| virtual int | [sendMediaExtraInfo](#ithunderenginesendmediaextrainfo)(const char* extraData) = 0 |
| virtual int | [enableMixVideoExtraInfo](#ithunderengineenablemixvideoextrainfo)(bool enabled) = 0 |
| virtual int | [startScreenCaptureForHwnd](#ithunderenginestartscreencaptureforhwnd)(HWND hWnd, const RECT* pRect) = 0 |
| virtual int | [startScreenCaptureForScreen](#ithunderenginestartscreencaptureforscreen)(int screenId, const RECT* pRect) = 0 |
| virtual int | [updateScreenCaptureRect](#ithunderengineupdatescreencapturerect)(const RECT* pRect) = 0 |
| virtual int | [stopScreenCapture](#ithunderenginestopscreencapture)() = 0 |
| virtual int | [pauseScreenCapture](#ithunderenginepausescreencapture)() = 0 |
| virtual int | [resumeScreenCapture](#ithunderengineresumescreencapture)() = 0 |
| virtual int | [registerVideoCaptureObserver](#ithunderengineregistervideocaptureobserver)([IVideoCaptureObserver](#ivideocaptureobserver)* observer) = 0 |
| virtual int | [registerMediaExtraInfoObserver](#ithunderengineregistermediaextrainfoobserver)([IThunderMediaExtraInfoObserver](notification.md#ithundermediaextrainfoobserver)* observer) = 0 |
| virtual [IThunderAudioPlayer](#ithunderaudioplayer)* | [createThunderAudioPlayer](#ithunderenginecreatethunderaudioplayer)() = 0 |
| virtual void | [destroyThunderAudioPlayer](#ithunderenginedestroythunderaudioplayer)([IThunderAudioPlayer](#ithunderaudioplayer)* player) = 0 |

- 
   ### IAudioDeviceManager

| public member functions | Function Name |
| ---:| :--- |
| virtual int | [enumInputDevices](#iaudiodevicemanagerenuminputdevices)([AudioDeviceList](#audiodevicelist)& devices) = 0 |
| virtual int | [setInputtingDevice](#iaudiodevicemanagersetinputtingdevice)(GUID& id) = 0 |
| virtual int | [getInputtingDevice](#iaudiodevicemanagergetinputtingdevice)(GUID& id) = 0 |
| virtual int | [setInputtingVolume](#iaudiodevicemanagersetinputtingvolume)(int volume) = 0 |
| virtual int | [getInputtingVolume](#iaudiodevicemanagergetinputtingvolume)(int& volume) = 0 |
| virtual int | [setInputtingMute](#iaudiodevicemanagersetinputtingmute)(bool mute) = 0 |
| virtual int | [getInputtingMute](#iaudiodevicemanagergetinputtingmute)(bool& mute) = 0 |
| virtual int | [startInputDeviceTest](#iaudiodevicemanagerstartinputdevicetest)(int indicationInterval) = 0 |
| virtual int | [stopInputDeviceTest](#iaudiodevicemanagerstopinputdevicetest)() = 0 |
| virtual int | [enumOutputDevices](#iaudiodevicemanagerenumoutputdevices)([AudioDeviceList](#audiodevicelist)& devices) = 0 |
| virtual int | [setOutputtingDevice](#iaudiodevicemanagersetoutputtingdevice)(GUID& id) = 0 |
| virtual int | [getOutputtingDevice](#iaudiodevicemanagergetoutputtingdevice)(GUID& id) = 0 |
| virtual int | [setOuttingVolume](#iaudiodevicemanagersetouttingvolume)(int volume) = 0 |
| virtual int | [getOuttingVolume](#iaudiodevicemanagergetouttingvolume)(int& volume) = 0 |
| virtual int | [setOutputtingMute](#iaudiodevicemanagersetoutputtingmute)(bool mute) = 0 |
| virtual int | [getOutputtingMute](#iaudiodevicemanagergetoutputtingmute)(bool& mute) = 0 |
| virtual int | [startOutputDeviceTest](#iaudiodevicemanagerstartoutputdevicetest)(int indicationInterval, const char* audioFileName) = 0 |
| virtual int | [stopOutputDeviceTest](#iaudiodevicemanagerstopoutputdevicetest)() = 0 |
| virtual int | [enableMicEnhancement](#iaudiodevicemanagerenablemicenhancement)(bool enabled) = 0 |
| virtual int | [enableMicDenoise](#iaudiodevicemanagerenablemicdenoise)(bool enabled) = 0 |
| virtual int | [enableAEC](#iaudiodevicemanagerenableaec)(bool enabled) = 0 |
| virtual int | [enableAGC](#iaudiodevicemanagerenableagc)(bool enabled) = 0 |

- 
   ### IThunderAudioPlayer

| public member functions | Function Name |
| ---:| :--- |
| virtual bool | [open](#ithunderaudioplayeropen)(const char* path) = 0 |
| virtual void | [close](#ithunderaudioplayerclose)() = 0 |
| virtual void | [play](#ithunderaudioplayerplay)() = 0 |
| virtual void | [stop](#ithunderaudioplayerstop)() = 0 |
| virtual void | [pause](#ithunderaudioplayerpause)() = 0 |
| virtual void | [resume](#ithunderaudioplayerresume)() = 0 |
| virtual void | [seek](#ithunderaudioplayerseek)(unsigned int timeMS) = 0 |
| virtual unsigned int | [getTotalPlayTimeMS](#ithunderaudioplayergettotalplaytimems)() = 0 |
| virtual unsigned int | [getCurrentPlayTimeMS](#ithunderaudioplayergetcurrentplaytimems)() = 0 |
| virtual int | [setPlayerLocalVolume](#ithunderaudioplayersetplayerlocalvolume)(int volume) = 0 |
| virtual int | [setPlayerPublishVolume](#ithunderaudioplayersetplayerpublishvolume)(int volume) = 0 |
| virtual int | [getPlayerLocalVolume](#ithunderaudioplayergetplayerlocalvolume)() = 0 |
| virtual int | [getPlayerPublishVolume](#ithunderaudioplayergetplayerpublishvolume)() = 0 |
| virtual int | [setLooping](#ithunderaudioplayersetlooping)(int cycle) = 0 |
| virtual void | [SetFilePlayerNotify](#ithunderaudioplayersetfileplayernotify)([IThunderAudioPlayerNotify](notification.md#ithunderaudioplayernotify)* notify) = 0 |

- 
   ### IVideoDeviceManager

| public member functions | Function Name |
| ---:| :--- |
| virtual int | [enumVideoDevices](#ivideodevicemanagerenumvideodevices)([VideoDeviceList](#videodevicelist)& devices) = 0 |
| virtual int | [startVideoDeviceCapture](#ivideodevicemanagerstartvideodevicecapture)(int deviceIdx) = 0 |
| virtual int | [stopVideoDeviceCapture](#ivideodevicemanagerstopvideodevicecapture)() = 0 |
| virtual int | [enumMonitorDevices](#ivideodevicemanagerenummonitordevices)([MonitorDeviceList](#monitordevicelist)& devices) = 0 |

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
> - It is recommended to call the IThunderEngine::[initialize](#ithunderengineinitialize) interface immediately after createEngine is called.
> - Currently, SDK supports only one IThunderEngine instance, that is, each process can only create one IThunderEngine object.
> - Unless otherwise specified, all interfaces in the IThunderEngine class are called asynchronously. It is recommended that interfaces are called on the same thread.

##### Return[](#createengine)

Pointer to the Thunder::IThunderEngine object

--------------------------

#### IThunderEngine::destroyEngine

```c++
virtual void Thunder::IThunderEngine::destroyEngine();
```

Destroy the Thunder::IThunderEngine instance.

##### Description[](#destroyengine)

- This method releases all resources used by SDK.
- Some applications only operate voice communication required by users. Resources can be released for other operations if they are not in need. This method may be applicable for such applications.
- Once [destroyEngine](#ithunderenginedestroyengine) is called, the user will be no longer able to use functions of this instance and event notification will not be triggered any more.
- To use communication function again, [createEngine](#ithunderenginecreateengine) must be called again to create another IThunderEngine instance.

--------------------------

#### IThunderEngine::initialize

```c++
virtual int Thunder::IThunderEngine::initialize(const char* appId, int sceneId, IThunderEventHandler* pHandler);
```

Initialize the engine.

> **Note:**
>
> - Only users with the same appId can communicate with each other.
> - Call this interface after an instance has been created. This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.

##### Parameter[](#initialize)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| appId | IN | appId assigned for application program developers. It can be requested in the official website. |
| sceneId | IN | Id for scenarios customized by developers. It details service scenarios and can be collected with more details based on scenarios. If not required, set it to 0. |
| pHandler | IN | [Pointer of the IThunderEventHandler](notification.md#ithundereventhandler) object. SDK calls back various events for application programs through this abstract class during SDK running. |

##### Return[](#initialize)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - This interface takes effect only if it is called before the calling of [joinRoom](#ithunderenginejoinroom).
> - It is necessary for abroad users but not for domestic users.
> - It can only be reset when [destroyEngine](#ithunderenginedestroyengine) is performed.

##### Parameter[](#setarea)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| area | IN | Region type is domestic by default. For details about the parameter value, see [AREA_TYPE.](#area-type) |

##### Return[](#setarea)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::joinRoom

```c++
virtual int Thunder::IThunderEngine::joinRoom(const char* token, int tokenLen, const char* roomName, const char* uid);
```

Join a room.

This method lets users join the (audio/video) communication room. In the same room, users can communicate with each other, and group chat starts when multiple users join it.

If during the call, users have to call [leaveRoom](#ithunderengineleaveroom) to leave before joining the next one.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - The applications using different appId cannot communicate with each other.
> - Success returned by the function only indicates request execution success. You have joined a room successfully only if you receive the [onJoinRoomSuccess](notification.md#ithundereventhandleronjoinroomsuccess) notification.

##### Parameter[](#joinroom)

| Parameter | Type | Description |
| --- | --- | --- |
| token | IN | Required for authentication. For details, see User Authentication Description on official website. |
| tokenLen | IN | Token length |
| roomName | IN | Room Id (unique for AppId) only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |
| uid | IN | User ID only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes. |

##### Return[](#joinroom)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::leaveRoom

```c++
virtual int Thunder::IThunderEngine::leaveRoom();
```

Leaving room indicates hang off or exiting conversation.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - When [joinRoom](#ithunderenginejoinroom) is called, you have to call [leaveRoom](#ithunderengineleaveroom) to end conversation before starting the next one. No matter whether the user is idle or in a call, [leaveRoom](#ithunderengineleaveroom) can be called, without adverse effects. This method can release all resources related to conversation.

##### Return[](#leaveroom)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::updateToken

```c++
virtual int Thunder::IThunderEngine::updateToken(const char* token, int tokenLen);
```

Update token.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - Success returned by the function only indicates request execution success. You have joined a room successfully only if you receive the [onJoinRoomSuccess](notification.md#ithundereventhandleronjoinroomsuccess) notification.

Token is used for authentication. Recommended token format is as follows. For details, see [Token Generator](/rtc_video_interaction/token_generator/).

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

##### Parameter[](#updatetoken)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| token | IN | Required for authentication. For details, see [User Authentication Description](/rtc_video_interaction/token_generator/). |
| tokenLen | IN | Token length |

##### Return[](#updatetoken)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setMediaMode

```c++
virtual int Thunder::IThunderEngine::setMediaMode(THUNDER_PROFILE mode);
```

Set media format. [PROFILE_NORMAL](#thunder-profile) is used by SDK by default.

> **Note:**
>
> - This interface should be called after initialization ([initialize](#ithunderengineinitialize)) and before joining a room ([joinRoom](#ithunderenginejoinroom)).
> - It can only be reset when [destroyEngine](#ithunderenginedestroyengine) is performed.

##### Parameter[](#setmediamode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Media mode. For details about the parameter value, see Thunder::[THUNDER_PROFILE.](#thunder-profile) |

##### Return[](#setmediamode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setRoomMode

```c++
virtual int Thunder::IThunderEngine::setRoomMode(ROOM_CONFIG_TYPE mode);
```

Set room mode. [ROOM_CONFIG_LIVE](#room-config-type) is used by SDK by default.

> **Note:**
>
> - This interface should be called after initialization ([initialize](#ithunderengineinitialize)) and before joining a room ([joinRoom](#ithunderenginejoinroom)).
> - It can only be reset when [destroyEngine](#ithunderenginedestroyengine) is performed.

##### Parameter[](#setroommode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Room mode. For details about the parameter value, see Thunder::[ROOM_CONFIG_TYPE.](#room-config-type) |

##### Return[](#setroommode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setAudioConfig

```c++
virtual int Thunder::IThunderEngine::setAudioConfig(AUDIO_PROFILE_TYPE profile, COMMUT_MODE commutMode, SCENARIO_MODE scenarioMode);
```

Set audio parameters and application scenarios.

> **Note:**
>
> - Call it before playing audio [stopLocalAudioStream](#ithunderenginestoplocalaudiostream) .
> - It can only be reset when [destroyEngine](#ithunderenginedestroyengine) is performed.

##### Parameter[](#setaudioconfig)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| profile | IN | Audio type. For details about the parameter value, see Thunder::[AUDIO_PROFILE_TYPE.](#audio-profile-type) |
| commuMode | IN | Communication mode. For details about the parameter value, see Thunder::[COMMUT_MODE.](#commut-mode) |
| scenarioMode | IN | Scenario mode. For details about the parameter value, see Thunder::[SCENARIO_MODE.](#scenario-mode) |

##### Return[](#setaudioconfig)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setAudioSourceType

```c++
virtual int Thunder::IThunderEngine::setAudioSourceType(ThunderSourceType sourceType);
```

Set audio publishing type.

> **Note:**
>
> - It can only be reset when [destroyEngine](#ithunderenginedestroyengine) is performed.

##### Parameter[](#setaudiosourcetype)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sourceType | IN | Audio publishing mode. For details about the parameter value, see Thunder::[ThunderSourceType.](#thundersourcetype) |

##### Return[](#setaudiosourcetype)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopLocalAudioStream

```c++
virtual int Thunder::IThunderEngine::stopLocalAudioStream(bool stop);
```

Stop broadcasting/Publish audio (including starting capture, encoding, and stream publishing).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#stoplocalaudiostream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Close local audio; false: Open local audio |

##### Return[](#stoplocalaudiostream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopAllRemoteAudioStreams

```c++
virtual int Thunder::IThunderEngine::stopAllRemoteAudioStreams(bool stop);
```

Stop/Receive all audio data. Process this interface based on the following rules:

- By default, SDK receives all audio data.
- After the setting of receiving all (stop=false), all audio stream in the room will be subscribed automatically. You can specify one stream of not being subscribed by [stopRemoteAudioStream](#ithunderenginestopremoteaudiostream).
- After the setting of receiving nothing (stop=true), all audio stream in the room will not be subscribed. You can specify one stream being subscribed by [stopRemoteAudioStream](#ithunderenginestopremoteaudiostream).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.
> - Determine whether to receive or disable remote users. Check the value of [stopRemoteAudioStream](#ithunderenginestopremoteaudiostream) first. If no value is found, use the value of this function.

##### Parameter[](#stopallremoteaudiostreams)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Close local audio; false: Open local audio |

##### Return[](#stopallremoteaudiostreams)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopRemoteAudioStream

```c++
virtual int Thunder::IThunderEngine::stopRemoteAudioStream(const char* uid, bool stop);
```

Stop/Receive audio data of specified users.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.
> - Determine whether to receive or disable remote users. Check the value of this function first. If no value is found, use the value of [stopRemoteAudioStream](#ithunderenginestopallremoteaudiostreams).

##### Parameter[](#stopremoteaudiostream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | IN | User UID |
| Stop | IN | true: Stop user audio, false: Receive user audio |

##### Return[](#stopremoteaudiostream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setAudioVolumeIndication

```c++
virtual int Thunder::IThunderEngine::setAudioVolumeIndication(int interval, int smooth);
```

Enable volume indication for speaker. 
This method allows SDK to return current speaker and speaker volume to application programs regularly.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.
> - After this method is called, an [onPlayVolumeIndication](notification.md#ithundereventhandleronplayvolumeindication) notification will be received once anyone speaks in the room
> - The volume carried in the notification does not include sound volume collected by the local microphone or played by files.

##### Parameter[](#setaudiovolumeindication)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| interval | IN | Notification interval. The default value is 0 <br><=0: The volume prompt is disabled<br> >0: Notification interval, unit: ms (a value greater than 200 is recommended) |
| smooth | IN | Smooth coefficient, not realized currently |

##### Return[](#setaudiovolumeindication)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::enableLoopbackRecording

```c++
virtual int Thunder::IThunderEngine::enableLoopbackRecording(bool enabled);
```

Enable/Disable graphic card collection.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.

##### Parameter[](#enableloopbackrecording)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Start graphic card collection; false: Stop graphic card collection |

##### Return[](#enableloopbackrecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#startaudiorecording)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| fileName | IN | Recording file name (complete path, not including filename extension, the filename extension is generated based on fileType) |
| fileType | IN | File format. For details about the parameter value, see Thunder::[AUDIO_RECORDING_FILE_TYPE.](#audio-recording-file-type) |
| quality | IN | Recording quality. For details about the parameter value, see Thunder::[AUDIO_RECORDING_QUALITY_TYPE.](#audio-recording-quality-type) |

##### Return[](#startaudiorecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopAudioRecording

```c++
virtual int Thunder::IThunderEngine::stopAudioRecording();
```

Stop audio recording.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#stopaudiorecording)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::adjustRecordingSignalVolume

```c++
virtual int Thunder::IThunderEngine::adjustRecordingSignalVolume(int volume);
```

Set recording volume.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#adjustrecordingsignalvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume range, which is [0--400.] |

##### Return[](#adjustrecordingsignalvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::adjustPlaybackSignalVolume

```c++
virtual int Thunder::IThunderEngine::adjustPlaybackSignalVolume(int volume);
```

Set playing volume.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#adjustplaybacksignalvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume range, which is [0--400.] |

##### Return[](#adjustplaybacksignalvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::getAudioDeviceMgr

```c++
virtual Thunder::IAudioDeviceManager* Thunder::IThunderEngine::getAudioDeviceMgr();
```

Obtain the instance object of the audio device management interface.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#getaudiodevicemgr)

- Object pointer of the audio device management interface [IAudioDeviceManager](#iaudiodevicemanager).
- Null

--------------------------

#### IThunderEngine::registerAudioFrameObserver

```c++
virtual int Thunder::IThunderEngine::registerAudioFrameObserver(IAudioFrameObserver* observer);
```

Register audio frame data observer [IAudioFrameObserver](notification.md#iaudioframeobserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - The user must inherit the [IAudioFrameObserver](notification.md#iaudioframeobserver) interface class and implement the virtual methods. These methods will be used to call related original audio data.

##### Parameter[](#registeraudioframeobserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IAudioFrameObserver](notification.md#iaudioframeobserver) interface class Registration is canceled if it is set to null. |

##### Return[](#registeraudioframeobserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setRecordingAudioFrameParameters

```c++
virtual int Thunder::IThunderEngine::setRecordingAudioFrameParameters(int sampleRate,
 int channel,
 ThunderAudioRawFrameOperationMode mode,
 int samplesPerCall);
```

Set the mode for using raw audio recording data during callback [onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe)

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setrecordingaudioframeparameters)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sampleRate | IN | Sampling rate |
| channel | IN | Audio track; 1: Single track; 2: dual track |
| mode | IN | [Mode of using onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe). For details about the parameter value, see Thunder::[ThunderAudioRawFrameOperationMode.](#thunderaudiorawframeoperationmode) |
| samplesPerCall | IN | Specify sampling point number for data return in [onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe) , e.g. 1024 in transcoding publish stream. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setrecordingaudioframeparameters)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setPlaybackAudioFrameParameters

```c++
virtual int Thunder::IThunderEngine::setPlaybackAudioFrameParameters(int sampleRate,
 int channel,
 ThunderAudioRawFrameOperationMode mode,
 int samplesPerCall);
```

Set the mode for using raw audio playback data during callback [onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe)

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setplaybackaudioframeparameters)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| sampleRate | IN | Sampling rate |
| channel | IN | Audio track; 1: Single track; 2: dual track |
| mode | IN | [Mode of using onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe). For details about the parameter value, see Thunder::[ThunderAudioRawFrameOperationMode.](#thunderaudiorawframeoperationmode) |
| samplesPerCall | IN | Sampling number of returned data in specified [onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe). For example, the value is 1024 in transcoding and stream publishing. samplesPerCall = (int)(sampleRate × sampleInterval), in which: sampleInterval ≥ 0.01, in seconds. |

##### Return[](#setplaybackaudioframeparameters)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setLogFilePath

```c++
virtual int Thunder::IThunderEngine::setLogFilePath(const char* filePath);
```

Set directory for SDK to output log files.

> **Note:**
>
> - Ensure that the specified directory has write permission.

##### Parameter[](#setlogfilepath)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| filePath | IN | Complete list of log files |

##### Return[](#setlogfilepath)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setLogLevel

```c++
virtual int Thunder::IThunderEngine::setLogLevel(LOG_FILTER filter);
```

Set the log storage level. Logs with lower level (LogLevel) will be filtered. Only logs with the log level indicated by this value or higher than this value are recorded.

##### Parameter[](#setloglevel)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| filter | IN | For details about the log filtering level, see Thunder::[LOG_FILTER.](#log-filter) |

##### Return[](#setloglevel)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::registerVideoFrameObserver

```c++
virtual int Thunder::IThunderEngine::registerVideoFrameObserver(IVideoFrameObserver* observer);
```

Register video frame data observer [IVideoFrameObserver](notification.md#ivideoframeobserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - The user must inherit the [IVideoFrameObserver](notification.md#ivideoframeobserver) interface class and implement the virtual methods. These methods will be used to call related original video data.

##### Parameter[](#registervideoframeobserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IVideoFrameObserver](notification.md#ivideoframeobserver) interface class Registration is canceled if it is set to null. |

##### Return[](#registervideoframeobserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::getVideoDeviceMgr

```c++
virtual Thunder::IVideoDeviceManager* Thunder::IThunderEngine::getVideoDeviceMgr();
```

Register video frame data observer [IVideoFrameObserver](notification.md#ivideoframeobserver).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#getvideodevicemgr)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setvideoencoderconfig)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| config | IN | Specific code configuration. For details about the parameter value, see Thunder::[VideoEncoderConfiguration.](#videoencoderconfiguration) |

##### Return[](#setvideoencoderconfig)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setlocalvideocanvas)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| canvas | IN | Reference of rendering object [VideoCanvas](#videocanvas) |

##### Return[](#setlocalvideocanvas)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setremotevideocanvas)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| canvas | IN | Reference of rendering object [VideoCanvas](#videocanvas) |

##### Return[](#setremotevideocanvas)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setLocalCanvasScaleMode

```c++
virtual int Thunder::IThunderEngine::setLocalCanvasScaleMode(VideoRenderMode mode);
```

Set local view display mode.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setlocalcanvasscalemode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#videorendermode) |

##### Return[](#setlocalcanvasscalemode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setRemoteCanvasScaleMode

```c++
virtual int Thunder::IThunderEngine::setRemoteCanvasScaleMode(VideoRenderMode mode);
```

Set the remote play type.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setremotecanvasscalemode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#videorendermode) |

##### Return[](#setremotecanvasscalemode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::startVideoPreview

```c++
virtual int Thunder::IThunderEngine::startVideoPreview();
```

Start camera video preview.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#startvideopreview)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#videorendermode) |

##### Return[](#startvideopreview)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopVideoPreview

```c++
virtual int Thunder::IThunderEngine::stopVideoPreview();
```

Stop camera video preview.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#stopvideopreview)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Rendering mode. For details about the parameter value, see Thunder::[VideoRenderMode](#videorendermode) |

##### Return[](#stopvideopreview)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::enableLocalVideoCapture

```c++
virtual int Thunder::IThunderEngine::enableLocalVideoCapture(bool enabled);
```

Enable/Disable local video capture.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#enablelocalvideocapture)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable local video capture; <br>false: Disable local video capture |

##### Return[](#enablelocalvideocapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopLocalVideoStream

```c++
virtual int Thunder::IThunderEngine::stopLocalVideoStream(bool stop);
```

Enable/Disable local video sending.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#stoplocalvideostream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | True: Disable local video sending; false: Enable local video sending<br> |

##### Return[](#stoplocalvideostream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopRemoteVideoStream

```c++
virtual int Thunder::IThunderEngine::stopRemoteVideoStream(const char* uid, bool stop);
```

Stop/Receive designated remote video.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called
> - Determine whether to receive or disable remote users. Check the value of this function first. If no value is found, use the value of [stopAllRemoteVideoStreams](#ithunderenginestopallremotevideostreams)

##### Parameter[](#stopremotevideostream)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | IN | User id |
| Stop | IN | true: Stop remote video of a specified user; false: Receive remote video of a specified user<br> |

##### Return[](#stopremotevideostream)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopAllRemoteVideoStreams

```c++
virtual int Thunder::IThunderEngine::stopAllRemoteVideoStreams(bool stop);
```

Stop/Receive all remote videos.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.
> - Determine whether to receive or disable remote users. Check the value of [stopRemoteVideoStream](#ithunderenginestopremotevideostream) first. If no value is found, use the value of this function

##### Parameter[](#stopallremotevideostreams)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| Stop | IN | true: Stop all remote video; false; Receive all remote video. The default value is false<br><br> |

##### Return[](#stopallremotevideostreams)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setLocalVideoMirrorMode

```c++
virtual int Thunder::IThunderEngine::setLocalVideoMirrorMode(ThunderVideoMirrorMode mode);
```

Set local video mirror mode

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called.
> - Set the mirror mode for local preview and that visible to viewers respectively.

##### Parameter[](#setlocalvideomirrormode)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mode | IN | Mirror mode. For details about the parameter value, see Thunder::[ThunderVideoMirrorMode](#thundervideomirrormode) |

##### Return[](#setlocalvideomirrormode)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setVideoWatermark

```c++
virtual int Thunder::IThunderEngine::setVideoWatermark(const Thunder::ThunderBoltImage& watermark);
```

Add local video watermark.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - Currently, only one watermark is supported. A newly added watermark will replace the existing one.
> - Only 24-bit and 32-bit pictures are supported. SDK will transform the pictures to the configured width.

##### Parameter[](#setvideowatermark)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| watermark | IN | Reference of watermark picture object to be added to local live streaming push. For details about the picture format, see Thunder::[ThunderBoltImage](#thunderboltimage) |

##### Return[](#setvideowatermark)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::removeVideoWatermarks

```c++
virtual int Thunder::IThunderEngine::removeVideoWatermarks();
```

Remove the local video watermark added.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#removevideowatermarks)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setCustomAudioSource

```c++
virtual int Thunder::IThunderEngine::setCustomAudioSource(bool bEnable, CustomAudioOptions& option);
```

Set parameters for external audio capture.

> **Note:**
>
> - This interface should be called after you perform initialization ([initialize](#ithunderengineinitialize)) and before you call ([stopLocalAudioStream(false)](#ithunderenginestoplocalaudiostream) to publish audio.

##### Parameter[](#setcustomaudiosource)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| bEnable | IN | true: enable external audio capture <br>false: disable external audio capture (by default) |
| option | IN | External audio capture parameter. It is the reference of [CustomAudioOptions](#customaudiooptions) |

##### Return[](#setcustomaudiosource)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::pushCustomAudioFrame

```c++
virtual int Thunder::IThunderEngine::pushCustomAudioFrame(const char* pData, unsigned dataLen, unsigned timeStamp);
```

Push external audio frame.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#pushcustomaudioframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| pData | IN | PCM audio frame data |
| dataLen | IN | Data length |
| timeStamp | IN | Capture timestamp |

##### Return[](#pushcustomaudioframe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::setCustomVideoSource

```c++
virtual int Thunder::IThunderEngine::setCustomVideoSource(bool bEnable, CustomVideoOptions& option)
```

Set parameters for external video capture.

> **Note:**
>
> - This interface should be called after you perform initialization ([initialize](#ithunderengineinitialize)) and before you call ([stopLocalVideoStream(false)](#ithunderenginestoplocalvideostream)) to publish video.

##### Parameter[](#setcustomvideosource)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| bEnable | IN | true: enable external audio capture <br>false: disable external audio capture (by default) |
| option | IN | External video capture parameter. It is the reference of [CustomVideoOptions](#customvideooptions) |

##### Return[](#setcustomvideosource)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::pushCustomVideoFrame

```c++
virtual int Thunder::IThunderEngine::pushCustomVideoFrame(const unsigned char* yuv[3], int linesize[3], unsigned timestamp);
```

Push external video frame.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#pushcustomvideoframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| yuv | IN | YUV video data |
| linesize | IN | Line size of the buffer zone in YUV data |
| timestamp | IN | Capture timestamp |

##### Return[](#pushcustomvideoframe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::addPublishOriginStreamUrl

```c++
virtual int Thunder::IThunderEngine::addPublishOriginStreamUrl(const char* url);
```

Add the source stream publishing address.

- After this interface is called, the server will push source streams to the matching URL after publishing starts. Only one-channel stream publishing address can be added each time by this method. If multi-channel streams need to be pushed, this method have to be called repeatedly.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.
> - A maximum of 5 addresses are supported for stream publishing

##### Parameter[](#addpublishoriginstreamurl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#addpublishoriginstreamurl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::removePublishOriginStreamUrl

```c++
virtual int Thunder::IThunderEngine::removePublishOriginStreamUrl(const char* url);
```

Remove the source stream publishing address.

##### Parameter[](#removepublishoriginstreamurl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#removepublishoriginstreamurl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#setlivetranscodingtask)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID, which is unique in a room and is managed by users |
| transcodingCfg | IN | Specific transcoding layout. For details, see Thunder::[LiveTranscoding](#livetranscoding) |

##### Return[](#setlivetranscodingtask)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::removeLiveTranscodingTask

```c++
virtual int Thunder::IThunderEngine::removeLiveTranscodingTask(const char* taskId);
```

Remove a transcoding task.

- After this interface is called, AIVACOM background will terminate and delete stream mixing tasks.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removelivetranscodingtask)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID, which is unique in a room and is managed by users |

##### Return[](#removelivetranscodingtask)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#addpublishtranscodingstreamurl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#addpublishtranscodingstreamurl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::removePublishTranscodingStreamUrl

```c++
virtual int Thunder::IThunderEngine::removePublishTranscodingStreamUrl(const char* taskId, const char* url);
```

Remove stream publishing address for transcoding stream.

- After this interface is called, the specified mixed stream will not be pushed to the specified CDN address.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removepublishtranscodingstreamurl)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| taskId | IN | Transcoding task ID |
| url | IN | Stream publishing address, in RTMP format. The value does not support special characters including Chinese and the length cannot exceed 512 bytes. Note: Some CDN manufacturers may not support the 512 bytes, for instance, Aliyun supports merely 256 bytes. |

##### Return[](#removepublishtranscodingstreamurl)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::addSubscribe

```c++
virtual int Thunder::IThunderEngine::addSubscribe(const char* roomId, const char* uid);
```

Subscribe to specific streams (cross-room).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#addsubscribe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#addsubscribe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::removeSubscribe

```c++
virtual int Thunder::IThunderEngine::removeSubscribe(const char* roomId, const char* uid);
```

Unsubscribe specified streams.

- After this interface is called, the specified mixed stream will not be pushed to the specified CDN address.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#removesubscribe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#removesubscribe)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::enableWebSdkCompatibility

```c++
virtual int Thunder::IThunderEngine::enableWebSdkCompatibility(bool enabled);
```

Enable/Disable WebSDK compatibility.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called
> - This method is applicable only to the live streaming scenario. Microphone connection is compatible with Web SDK by default, without calling this method.
> - Enable compatibility with WebSDK in live streaming. This interface must be called before publishing, which is irrelevant with entering or leaving the room.

##### Parameter[](#enablewebsdkcompatibility)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | Whether compatibility is enabled. Disabled by default |

##### Return[](#enablewebsdkcompatibility)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
- Monitor and notify causes for failure in sending customized broadcast messages through [onSendAppMsgDataFailedStatus](notification.md#ithundereventhandleronsendappmsgdatafailedstatus).
- Monitor customized broadcast messages sent from other users through [onRecvUserAppMsgData](notification.md#ithundereventhandleronrecvuserappmsgdata).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#senduserappmsgdata)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| msgData | IN | Service customized broadcast message |

##### Return[](#senduserappmsgdata)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
- Monitor causes for failure in sending media extra information through [onSendMediaExtraInfoFailedStatus](notification.md#ithundermediaextrainfoobserveronsendmediaextrainfofailedstatus).
- Monitor media extra information sent from other users through [onRecvMediaExtraInfo](notification.md#ithundermediaextrainfoobserveronrecvmediaextrainfo).

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#sendmediaextrainfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| extraData | IN | Media extra information |

##### Return[](#sendmediaextrainfo)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::enableMixVideoExtraInfo

```c++
virtual int Thunder::IThunderEngine::enableMixVideoExtraInfo(bool enabled);
```

Enable video mixing with media extra information.

> **Note:**
>
> - This interface is called only if you need to join a room ([joinRoom](#ithunderenginejoinroom)). The configuration will be cleaned after you leave the room.

##### Parameter[](#enablemixvideoextrainfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | The default value is false. true: Enable video mixing with media extra information; false: Disable video mixing with media extra information. |

##### Return[](#enablemixvideoextrainfo)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::startScreenCaptureForHwnd

```c++
virtual int Thunder::IThunderEngine::startScreenCaptureForHwnd(HWND hWnd, const RECT* pRect);
```

Start capturing specific screen.

##### Parameter[](#startscreencaptureforhwnd)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| hWnd | IN | Window handle |
| pRect | IN | Sub region captured from a window. The coordinates are relative values. The coordinate of the point in the upper left corner is (0,0). The entire window is captured if the value is NULL. |

##### Return[](#startscreencaptureforhwnd)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::startScreenCaptureForScreen

```c++
virtual int Thunder::IThunderEngine::startScreenCaptureForScreen(int screenId = 0, const RECT* pRect);
```

Start capturing specific region on desktop.

##### Parameter[](#startscreencaptureforscreen)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| screenId | IN | Monitor ID |
| pRect | IN | Sub region specified for capturing. The coordinate is a relative value of the monitor. The entire monitor screen is captured when this parameter is set to NULL. |

##### Return[](#startscreencaptureforscreen)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::updateScreenCaptureRect

```c++
virtual int Thunder::IThunderEngine::updateScreenCaptureRect(const RECT* pRect);
```

Update the displayed region for capturing.

##### Parameter[](#updatescreencapturerect)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| pRect | IN | Sub region specified for capturing. The coordinate is a relative value of the monitor or screen. The entire monitor screen or window is captured when this parameter is set to NULL. |

##### Return[](#updatescreencapturerect)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::stopScreenCapture

```c++
virtual int Thunder::IThunderEngine::stopScreenCapture();
```

Stop capturing the desktop or window.

##### Return[](#stopscreencapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::pauseScreenCapture

```c++
virtual int Thunder::IThunderEngine::pauseScreenCapture();
```

Pause capturing the desktop or window.

##### Return[](#pausescreencapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::resumeScreenCapture

```c++
virtual int Thunder::IThunderEngine::resumeScreenCapture(const char* roomId, const char* uid);
```

Resume capturing the desktop or window.

##### Return[](#resumescreencapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::registerVideoCaptureObserver

```c++
virtual int Thunder::IThunderEngine::registerVideoCaptureObserver(IVideoCaptureObserver* observer);
```

Register observer object for collecting data of camera.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#registervideocaptureobserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IVideoCaptureObserver](notification.md#ivideocaptureobserver) object. If observer is NULL, monitoring is canceled. |

##### Return[](#registervideocaptureobserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::registerMediaExtraInfoObserver

```c++
virtual int Thunder::IThunderEngine::registerMediaExtraInfoObserver(IThunderMediaExtraInfoObserver* observer);
```

Register the observer object of media extra information.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#registermediaextrainfoobserver)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| observer | IN | [Pointer of the IThunderMediaExtraInfoObserver](notification.md#ithundermediaextrainfoobserver) object. If observer is NULL, monitoring is canceled. |

##### Return[](#registermediaextrainfoobserver)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderEngine::createThunderAudioPlayer

```c++
virtual IThunderAudioPlayer* Thunder::IThunderEngine::createThunderAudioPlayer();
```

Create an object for audio file player. For details, see [IThunderAudioPlayer](#ithunderaudioplayer).

##### Return[](#createthunderaudioplayer)

- IThunderAudioPlayer*: Pointer of the audio file player object
- NULL: Creating audio file player failed.

--------------------------

#### IThunderEngine::destroyThunderAudioPlayer

```c++
virtual int Thunder::IThunderEngine::destroyThunderAudioPlayer(IThunderAudioPlayer* player);
```

Destroy audio file player.

##### Parameter[](#destroythunderaudioplayer)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| player | IN | [Pointer of the IThunderAudioPlayer](#ithunderaudioplayer) object |

##### Return[](#destroythunderaudioplayer)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

### IAudioDeviceManager

#### IAudioDeviceManager::enumInputDevices

```c++
virtual int Thunder::IAudioDeviceManager::enumInputDevices(AudioDeviceList& devices);
```

Enumerate audio input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#enuminputdevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | Information about the audio device. For details, see [AudioDeviceList.](#audiodevicelist) |

##### Return[](#enuminputdevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setInputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingDevice(GUID& id);
```

Set audio input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setinputtingdevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | IN | Unique descriptor for a device |

##### Return[](#setinputtingdevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getInputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingDevice(GUID& id);
```

Obtain the currently selected input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getinputtingdevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | OUT | Unique descriptor for a device |

##### Return[](#getinputtingdevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setInputtingVolume

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingVolume(int volume);
```

Set the volume of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setinputtingvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume value [0-400] |

##### Return[](#setinputtingvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getInputtingVolume

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingVolume(int volume);
```

Obtain the volume of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getinputtingvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-400] |

##### Return[](#getinputtingvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setInputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::setInputtingMute(bool mute);
```

Mute the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setinputtingmute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | IN | true: mute; false: unmute<br> |

##### Return[](#setinputtingmute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getInputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::getInputtingMute(bool& mute);
```

Obtain the mute status of the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getinputtingmute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | OUT | true: mute; false: unmute<br> |

##### Return[](#getinputtingmute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::startInputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::startInputDeviceTest(int indicationInterval);
```

Start testing the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - After calling this interface, you will receive an [onInputVolume](notification.md#ithundereventhandleroninputvolume) notification.

##### Parameter[](#startinputdevicetest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| indicationInterval | IN | Check interval. The default value is 0. |

##### Return[](#startinputdevicetest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::stopInputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::stopInputDeviceTest();
```

Stop testing the current audio input device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#stopinputdevicetest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::enumOutputDevices

```c++
virtual int Thunder::IAudioDeviceManager::enumOutputDevices(AudioDeviceList& devices);
```

Enumerate audio playback devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#enumoutputdevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | List of audio playback devices. For details, see [AudioDeviceList.](#audiodevicelist) |

##### Return[](#enumoutputdevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setOutputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::setOutputtingDevice(GUID& id);
```

Specify the audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setoutputtingdevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | IN | Unique descriptor for a device |

##### Return[](#setoutputtingdevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getOutputtingDevice

```c++
virtual int Thunder::IAudioDeviceManager::getOutputtingDevice(GUID& id);
```

Obtain the current audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getoutputtingdevice)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| id | OUT | Unique descriptor for a device |

##### Return[](#getoutputtingdevice)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setOuttingVolume

```c++
virtual int Thunder::IAudioDeviceManager::setOuttingVolume(int volume);
```

Set the volume of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setouttingvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Volume value [0-400] |

##### Return[](#setouttingvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getOuttingVolume

```c++
virtual int Thunder::IAudioDeviceManager::getOuttingVolume(int& volume);
```

Obtain the volume of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getouttingvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-400] |

##### Return[](#getouttingvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::setOutputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::setOutputtingMute(bool mute);
```

Mute/Unmute the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#setoutputtingmute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | IN | true: mute; false: unmute<br> |

##### Return[](#setoutputtingmute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::getOutputtingMute

```c++
virtual int Thunder::IAudioDeviceManager::getOutputtingMute(bool& mute);
```

Obtain the mute status of the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#getoutputtingmute)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| mute | OUT | true: mute; <br>false: unmute |

##### Return[](#getoutputtingmute)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::startOutputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::startOutputDeviceTest(int indicationInterval, const char* audioFileName);
```

Start testing the current playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).
> - Calling the [setOutputtingDevice](#iaudiodevicemanagersetoutputtingdevice) interface will also terminate the test.

##### Parameter[](#startoutputdevicetest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| indicationInterval | IN | Check interval. The default value is 0. |
| audioFileName | IN | Full path of the audio file that is played. Win7 and higher support mp3, aac, and wave formats while versions earlier than Win7 support only the wav format. |

##### Return[](#startoutputdevicetest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::stopOutputDeviceTest

```c++
virtual int Thunder::IAudioDeviceManager::stopOutputDeviceTest();
```

Stop testing the current audio playback device.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#stopoutputdevicetest)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomId | IN | Room ID [which only supports the permutation and combination of characters such as [A,Z],[a,z],[0,9],-,_, with the length of not more than 64 bytes] |
| uid | IN | User ID |

##### Return[](#stopoutputdevicetest)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::enableMicEnhancement

```c++
virtual int Thunder::IAudioDeviceManager::enableMicEnhancement(bool enabled);
```

Enable/Disable microphone enhancement.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called

##### Parameter[](#enablemicenhancement)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable microphone enhancement; false: Disable microphone enhancement. The default value is false. |

##### Return[](#enablemicenhancement)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::enableMicDenoise

```c++
virtual int Thunder::IAudioDeviceManager::enableMicDenoise(bool enabled);
```

Enable/Disable microphone noise reduction.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called

##### Parameter[](#enablemicdenoise)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable microphone noise reduction; false: Disable microphone noise reduction. The default value is false. |

##### Return[](#enablemicdenoise)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::enableAEC

```c++
virtual int Thunder::IAudioDeviceManager::enableAEC(bool enabled);
```

Enable/Disable AEC.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called

##### Parameter[](#enableaec)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable AEC; false: Disable AEC. The default value is false. |

##### Return[](#enableaec)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IAudioDeviceManager::enableAGC

```c++
virtual int Thunder::IAudioDeviceManager::enableAGC(bool enabled);
```

Enable/Disable Automatic Gain Control (AGC).

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)). This interface is reset only when [destroyEngine](#ithunderenginedestroyengine) is called

##### Parameter[](#enableagc)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| enabled | IN | true: Enable AEC; false: Disable AEC. The default value is false. |

##### Return[](#enableagc)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
> - Before playing a file, call IThunderAudioPlayer::[open](#ithunderaudioplayeropen) to open it first.

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
> - The value cannot be greater than that obtained by [getTotalPlayTimeMS](#ithunderaudioplayergettotalplaytimems).

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
> - Call IThunderAudioPlayer::[open](#ithunderaudioplayeropen) to open the file first.

##### Return[](#gettotalplaytimems)

- Total duration for playing a file

--------------------------

#### IThunderAudioPlayer::getCurrentPlayTimeMS

```c++
virtual unsigned int Thunder::IAudioDeviceManager::getCurrentPlayTimeMS();
```

Get the time which has been played.

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#ithunderaudioplayeropen) to open the file and play it.

##### Return[](#getcurrentplaytimems)

- Played duration

--------------------------

#### IThunderAudioPlayer::setPlayerLocalVolume

```c++
virtual int Thunder::IAudioDeviceManager::setPlayerLocalVolume(int volume);
```

Adjusts volume size when music files are played on local end.

##### Parameter[](#setplayerlocalvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Play volume [0-100] |

##### Return[](#setplayerlocalvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderAudioPlayer::setPlayerPublishVolume

```c++
virtual int Thunder::IAudioDeviceManager::setPlayerPublishVolume(int volume);
```

Adjust the publish volume of the music file.

##### Parameter[](#setplayerpublishvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | IN | Play volume [0-100] |

##### Return[](#setplayerpublishvolume)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderAudioPlayer::getPlayerLocalVolume

```c++
virtual int Thunder::IAudioDeviceManager::getPlayerLocalVolume();
```

Get the local volume of music files. The value matches that configured by setPlayerLocalVolume. The range is [0-100].

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#ithunderaudioplayeropen) to open the file and play it.

##### Return[](#getplayerlocalvolume)

- Volume of the music file when played locally

--------------------------

#### IThunderAudioPlayer::getPlayerPublishVolume

```c++
virtual int Thunder::IAudioDeviceManager::getPlayerPublishVolume();
```

Obtain the publish volume of the music file. The value matches that configured by setPlayerPublishVolume. The range is [0-100].

> **Note:**
>
> - Call IThunderAudioPlayer::[open](#ithunderaudioplayeropen) to open the file and play it.

##### Return[](#getplayerpublishvolume)

- Publish volume of the music file

--------------------------

#### IThunderAudioPlayer::setLooping

```c++
virtual int Thunder::IAudioDeviceManager::setLooping(int cycle);
```

Sets times of loop playbacks.

##### Parameter[](#setlooping)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| cycle | IN | -1: indicates infinite loop; 0: No loop (default value); Positive integer: Loop times |

##### Return[](#setlooping)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IThunderAudioPlayer::SetFilePlayerNotify

```c++
virtual void Thunder::IAudioDeviceManager::void SetFilePlayerNotify(IThunderAudioPlayerNotify* notify);
```

Set playback callback.

##### Parameter[](#setfileplayernotify)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| notify | IN | Interface class of the playback callback. For details, see [IThunderAudioPlayerNotify.](#ithunderaudioplayernotify) |

--------------------------

### IVideoDeviceManager

#### IVideoDeviceManager::enumVideoDevices

```c++
virtual int Thunder::IVideoDeviceManager::enumVideoDevices(VideoDeviceList& devices);
```

Enumerate video input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#enumvideodevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | List of video input devices. For details, see [VideoDeviceList.](#videodevicelist) |

##### Return[](#enumvideodevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IVideoDeviceManager::startVideoDeviceCapture

```c++
virtual int Thunder::IVideoDeviceManager::startVideoDeviceCapture(int index);
```

Start the video input device and initiate collection.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#startvideodevicecapture)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| index | IN | Device index |

##### Return[](#startvideodevicecapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IVideoDeviceManager::stopVideoDeviceCapture

```c++
virtual int Thunder::IVideoDeviceManager::stopVideoDeviceCapture();
```

Stop video device capture.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Return[](#stopvideodevicecapture)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

--------------------------

#### IVideoDeviceManager::enumMonitorDevices

```c++
virtual int Thunder::IVideoDeviceManager::enumMonitorDevices(MonitorDeviceList& devices);
```

Enumerate monitor input devices.

> **Note:**
>
> - Do not call this interface before you perform initialization ([initialize](#ithunderengineinitialize)).

##### Parameter[](#enummonitordevices)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| devices | OUT | Returned list of video input devices. For details, see [MonitorDeviceList.](#monitordevicelist) |

##### Return[](#enummonitordevices)

- 0: Method call succeeded
- <0: Method call failed. For details about the return codes, see [enum ThunderRet.](code.md#thunderret)

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
| [VideoPublishPlayType](#videopublishplaytype) | Publishing type |
| [VideoPublishMode](#videopublishmode) | Publishing bracket |

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
| [VideoRenderMode](#videorendermode) | Video rendering mode |
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
