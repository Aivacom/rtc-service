# Event callback

## Interface List

- 
   ### ThunderEventDelegate

| Public callback function | Function Name |
| ---:| :--- |
| void | [thunderEngine:onJoinRoomSuccess:withUid:elapsed:](#thundereventdelegatethunderengineonjoinroomsuccesswithuidelapsed) |
| void | [thunderEngine:onLeaveRoomWithStats:](#thundereventdelegatethunderengineonleaveroomwithstats) |
| void | [thunderEngine:sdkAuthResult:](#thundereventdelegatethunderenginesdkauthresult) |
| void | [thunderEngine:bPublish:bizAuthResult:](#thundereventdelegatethunderenginebpublishbizauthresult) |
| void | [thunderEngine:onPlayVolumeIndication:totalVolume:](#thundereventdelegateonplayvolumeindicationtotalvolume) |
| void | [thunderEngine:onCaptureVolumeIndication:cpt:micVolume:](#thundereventdelegatethunderengineoncapturevolumeindicationcptmicvolume) |
| void | [thunderEngine:onAudioPlaySpectrumData:](#thundereventdelegatethunderengineonaudioplayspectrumdata) |
| void | [thunderEngine:onRecvUserAppMsgData:uid:](#thundereventdelegatethunderengineonrecvuserappmsgdatauid) |
| void | [thunderEngine:onSendAppMsgDataFailedStatus:](#thundereventdelegatethunderengineonsendappmsgdatafailedstatus) |
| void | [thunderEngine:onRemoteAudioStopped:byUid:](#thundereventdelegatethunderengineonremoteaudiostoppedbyuid) |
| void | [thunderEngine:onRemoteVideoStopped:byUid:](#thundereventdelegatethunderengineonremotevideostoppedbyuid) |
| void | [thunderEngine:onRemoteVideoPlay:size:elapsed:](#thundereventdelegatethunderengineonremotevideoplaysizeelapsed) |
| void | [thunderEngine:onVideoSizeChangedOfUid:size:rotation:](#thundereventdelegatethunderengineonvideosizechangedofuidsizerotation) |
| void | [thunderEngine:onVideoCaptureStatus:](#thundereventdelegatethunderengineonvideocapturestatus) |
| void | [thunderEngine:onConnectionStatus:](#thundereventdelegatethunderengineonconnectionstatus) |
| void | [thunderEngine:onRoomStats:](#thundereventdelegatethunderengineonroomstats) |
| void | [thunderEngine:onFirstLocalAudioFrameSent:](#thundereventdelegatethunderengineonfirstlocalaudioframesent) |
| void | [thunderEngine:onFirstLocalVideoFrameSent:](#thundereventdelegatethunderengineonfirstlocalvideoframesent) |
| void | [thunderEngine:onPublishStreamToCDNStatusWithUrl:errorCode:](#thundereventdelegatethunderengineonpublishstreamtocdnstatuswithurlerrorcode) |
| void | [thunderEngine:onNetworkTypeChanged:](#thundereventdelegatethunderengineonnetworktypechanged) |
| void | [thunderEngine:onLocalVideoStats:](#thundereventdelegatethunderengineonlocalvideostats) |
| void | [thunderEngine:onLocalAudioStats:](#thundereventdelegatethunderengineonlocalaudiostats) |
| void | [thunderEngine:onAudioCaptureStatus:](#thundereventdelegatethunderengineonaudiocapturestatus) |
| void | [thunderEngineConnectionLost:](#thundereventdelegatethunderengineconnectionlost) |
| void | [thunderEngine:onTokenWillExpire:](#thundereventdelegatethunderengineontokenwillexpire) |
| void | [thunderEngineTokenRequest:](#thundereventdelegatethunderenginetokenrequest) |
| void | [thunderEngine:onUserBanned:](#thundereventdelegatethunderengineonuserbanned) |
| void | [thunderEngine:onUserJoined:elapsed:](#thundereventdelegatethunderengineonuserjoinedelapsed) |
| void | [thunderEngine:onUserOffline:reason:](#thundereventdelegatethunderengineonuserofflinereason) |
| void | [thunderEngine:onNetworkQuality:txQuality:rxQuality:](#thundereventdelegatethunderengineonnetworkqualitytxqualityrxquality) |
| void | [thunderEngine:onRemoteVideoStatsOfUid:stats:](#thundereventdelegatethunderengineonremotevideostatsofuidstats) |
| void | [thunderEngine:onRemoteAudioStatsOfUid:stats:](#thundereventdelegatethunderengineonremoteaudiostatsofuidstats) |

- ### ThunderVideoDecodeFrameObserver

| Public callback function | Function Name |
| ---:| :--- |
| void | [onVideoDecodeFrame:pts:uid:](#thundervideodecodeframeobserveronvideodecodeframeptsuid) |

- ### ThunderVideoCaptureFrameObserver

| Public callback function | Function Name |
| ---:| :--- |
| [ThunderVideoCaptureFrameDataType](#thundervideocaptureframedatatype) | [needThunderVideoCaptureFrameDataType:](#thundervideocaptureframeobserverneedthundervideocaptureframedatatype) |
| CVPixelBufferRef _Nullable | [onVideoCaptureFrame:PixelBuffer:](#thundervideocaptureframeobserveronvideocaptureframepixelbuffer) |
| BOOL | [onVideoCaptureFrame:PixelBuffer:SourceTextureID:DestinationTextureID:TextureFormat:TextureTarget:TextureWidth:TextureHeight:](#thundervideocaptureframeobserveronvideocaptureframepixelbuffersourcetextureiddestinationtextureidtextureformattexturetargettexturewidthtextureheight) |

- ### ThunderMediaExtraInfoDelegate

| Public callback function | Function Name |
| ---:| :--- |
| void | [onSendMediaExtraInfoFailedStatus:](#thundermediaextrainfodelegateonsendmediaextrainfofailedstatus) |
| void | [onRecvMediaExtraInfo:ofUid:](#thundermediaextrainfodelegateonrecvmediaextrainfoofuid) |
| void | [onRecvMixAudioInfo:ofUid:](#thundermediaextrainfodelegateonrecvmixaudioinfoofuid) |
| void | [onRecvMixVideoInfo:ofUid:](#thundermediaextrainfodelegateonrecvmixvideoinfoofuid) |

- ### ThunderAudioFilePlayerDelegate

| Public callback function | Function Name |
| ---:| :--- |
| void | [onAudioFilePlayEnd:](#thunderaudiofileplayerdelegateonaudiofileplayend) |
| void | [onAudioFilePlayError:errorCode:](#thunderaudiofileplayerdelegateonaudiofileplayerrorerrorcode) |
| void | [onAudioFilePlaying:](#thunderaudiofileplayerdelegateonaudiofileplaying) |
| void | [onAudioFilePause:](#thunderaudiofileplayerdelegateonaudiofilepause) |
| void | [onAudioFileResume:](#thunderaudiofileplayerdelegateonaudiofileresume) |
| void | [onAudioFileStop:](#thunderaudiofileplayerdelegateonaudiofilestop) |
| void | [onAudioFileSeekComplete:milliseconds:](#thunderaudiofileplayerdelegateonaudiofileseekcompletemilliseconds) |
| void | [onAudioFileVolume:volume:currentMs:totalMs:](#thunderaudiofileplayerdelegateonaudiofilevolumevolumecurrentmstotalms) |
| void | [onAudioFileStateChange:event:errorCode:](#thunderaudiofileplayerdelegateonaudiofilestatechangeeventerrorcode) |

- ### IAudioFrameObserver

| Public callback function | Function Name |
| ---:| :--- |
| virtual bool | [onRecordAudioFrame](#iaudioframeobserveronrecordaudioframe)([AudioFrame](#audioframe)& audioFrame) = 0 |
| virtual bool | [onPlaybackAudioFrame](#iaudioframeobserveronplaybackaudioframe)([AudioFrame](#audioframe)& audioFrame) = 0 |
| virtual bool | [onPlaybackAudioFrameBeforeMixing](#iaudioframeobserveronplaybackaudioframebeforemixing)(char* uid, [AudioFrame](#audioframe)& audioFrame) = 0 |

- ### ThunderRtcLogDelegate

| Public callback function | Function Name |
| ---:| :--- |
| void | [onThunderRtcLogWithLevel:message:](#thunderrtclogdelegateonthunderrtclogwithlevelmessage) |

- ### ThunderCustomVideoSourceProtocol

| Public callback function | Function Name |
| ---:| :--- |
| BOOL | [onInitialize](#thundercustomvideosourceprotocoloninitialize):(nullable id<[ThunderVideoFrameConsumer](function.html#thundervideoframeconsumer)>)protocol |
| [ThunderVideoBufferType](#thundervideobuffertype) | [bufferType](#thundercustomvideosourceprotocolbuffertype) |
| void | [onStart](#thundercustomvideosourceprotocolonstart) |
| void | [onStop](#thundercustomvideosourceprotocolonstop) |
| void | [onDispose](#thundercustomvideosourceprotocolondispose) |

- ### ThunderExternalAudioProcessorDelegate

| Public callback function | Function Name |
| ---:| :--- |
| void | [audioCaptureStart](#thunderexternalaudioprocessordelegateaudiocapturestart) |
| void | [audioCaptureData:data:len:sampleRate:channelCount:bitPerSample:](#thunderexternalaudioprocessordelegateaudiocapturedatadatalensampleratechannelcountbitpersample) |
| void | [audioCaptureStop](#thunderexternalaudioprocessordelegateaudiocapturestop) |
| void | [audioRenderStart](#thunderexternalaudioprocessordelegateaudiorenderstart) |
| void | [audioRenderData:data:len:sampleRate:channelCount:bitPerSample:](#thunderexternalaudioprocessordelegateaudiorenderdatadatalensampleratechannelcountbitpersample) |
| void | [audioRenderStop](#thunderexternalaudioprocessordelegateaudiorenderstop) |

## Detailed callback description

### ThunderRtcLogDelegate

#### ThunderRtcLogDelegate::onThunderRtcLogWithLevel:message:

```objc
- (void)onThunderRtcLogWithLevel:(ThunderRtcLogLevel)level message:(nonnull NSString*)msg;
```

Callback of processing log

##### Parameter[](#onthunderrtclogwithlevel)

| Parameter | Description |
| :--- | :--- |
| level | For levels, see [ThunderRtcLogLevel for details](#thunderrtcloglevel) |
| msg | Log |

--------------------------

#### ThunderEventDelegate:thunderEngine:onJoinRoomSuccess:withUid:elapsed:

```objc
- (void)thunderEngine:(ThunderEngine* _Nonnull)engine
    onJoinRoomSuccess:(nonnull NSString*)room
              withUid:(nonnull NSString*)uid
              elapsed:(NSInteger)elapsed;
```

Callback of Join Room

##### Parameter[](#onjoinroomsuccess)

| Parameter | Description |
| :--- | :--- |
| room | Room name |
| uid | User ID |
| elapsed | Time (ms) consumed from callback of [joinRoom](function.html#thunderenginejoinroomroomnameuid) API to callback of the event |

--------------------------

#### ThunderEventDelegate:thunderEngine:sdkAuthResult:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine sdkAuthResult:(ThunderRtcSdkAuthResult)sdkAuthResult;
```

Callback of SDK authentication result. Result of SunClouds’ authentication returned

##### Parameter[](#sdkauthresult)

| Parameter | Description |
| :--- | :--- |
| sdkAuthResult | For authentication results, see [ThunderRtcSdkAuthResult for details](#thunderrtcsdkauthresult) |

--------------------------

#### ThunderEventDelegate:thunderEngine:bPublish:bizAuthResult:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine bPublish:(BOOL)bPublish bizAuthResult:(NSInteger)bizAuthResult;
```

Callback on service authentication results.

> **Note:**
>
> - For returned results to be authenticated by the service, SunClouds will transfer the authentication request to the service authentication server and pass through and return authentication results.

##### Parameter[](#bizauthresult)

| Parameter | Description |
| :--- | :--- |
| bPublish | YES: Authentication for publishing <br>NO: Authentication for playing |
| bizAuthResult | Authentication result: Pass through service authentication result returned, 0 for success; |

--------------------------

#### ThunderEventDelegate:onPlayVolumeIndication:totalVolume:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
onPlayVolumeIndication:(NSArray<ThunderRtcAudioVolumeInfo *> * _Nonnull)speakers
          totalVolume:(NSInteger)totalVolume;
```

Callback of speaking volume.

> **Note:**
>
> - Callback of prompt who is speaking in the room and volume of the speaker.

##### Parameter[](#onplayvolumeindication)

| Parameter | Description |
| :--- | :--- |
| speakers | Speaker (array). Each speaker includes:<br> Uid: User ID of the speaker. <br>volume: speaker's volume. <br>Pts: Playing timestamp |
| totalVolume | Total volume (after audio mixing) [0-100] |

--------------------------

#### ThunderEventDelegate:thunderEngine:onAudioPlaySpectrumData:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onAudioPlaySpectrumData:(nullable NSData*)data;
```

Callback on audio play spectrum data.

> **Note:**
>
> - This callback calls back the spectrum data of the audio played to the user.

##### Parameter[](#onaudioplayspectrumdata)

| Parameter | Description |
| :--- | :--- |
| Date | Spectrum data |

--------------------------

#### ThunderEventDelegate:onRecvUserAppMsgData:uid:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
  onRecvUserAppMsgData:(nonnull NSData*)msgData
                   uid:(nonnull NSString*)uid;
```

Callback of receiving service-customized broadcast message.

> **Note:**
>
> - This callback calls back the pass-through message received by the user and uid of the user sending the message.

##### Parameter[](#onrecvuserappmsgdata)

| Parameter | Description |
| :--- | :--- |
| msgData | Pass-through message received |
| uid | Uid of user sending the message |

--------------------------

#### ThunderEventDelegate:thunderEngine:onSendAppMsgDataFailedStatus:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onSendAppMsgDataFailedStatus:(NSUInteger)status;
```

Callback of failure of sending service-customized broadcast message.

> **Note:**
>
> - This callback calls back the reason why the user fails in sending the service-customized broadcast message. As stipulated currently, the passthrough frequency is twice/s and size of data sent is <=200Byte.

##### Parameter[](#onsendappmsgdatafailedstatus)

| Parameter | Description |
| :--- | :--- |
| status | Failure status:<br> 1: Frequency is too high <br>2: Data sent is too large <br>3: Publishing is not started successfully |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRemoteAudioStopped:byUid:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onRemoteAudioStopped:(BOOL)stopped byUid:(nonnull NSString*)uid;
```

Notification of enabling/disabling audio stream of remote user.

##### Parameter[](#onremoteaudiostopped)

| Parameter | Description |
| :--- | :--- |
| stopped | Callback on stopping/starting remote user audio stream |
| uid | Remote user uid |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRemoteVideoStopped:byUid:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onRemoteVideoStopped:(BOOL)stopped byUid:(nonnull NSString*)uid;
```

Notification of enabling/disabling video stream of remote user.

##### Parameter[](#onremotevideostopped)

| Parameter | Description |
| :--- | :--- |
| stopped | Callback of enabling/disabling video stream of remote user |
| uid | Remote user uid |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRemoteVideoPlay:size:elapsed:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine
    onRemoteVideoPlay:(nonnull NSString *)uid
    size:(CGSize)size
    elapsed:(NSInteger)elapsed;
```

Callback on displayed first remote video frame.

> **Note:**
>
> - Used to calculate the video speed.

##### Parameter[](#onremotevideoplay)

| Parameter | Description |
| :--- | :--- |
| uid | User id |
| size | For video size (width and height), see [CGSize for details](#cgsize) |
| elapsed | Time (ms) consumed from callback of [joinRoom](function.html#thunderenginejoinroomroomnameuid) API to callback of the event |

--------------------------

#### ThunderEventDelegate:thunderEngine:onVideoSizeChangedOfUid:size:rotation:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine
onVideoSizeChangedOfUid:(nonnull NSString*)uid
                 size:(CGSize)size
                 rotation:(NSInteger)rotation;
```

Callback on change in local or remote video resolution.

##### Parameter[](#onvideosizechangedofuid)

| Parameter | Description |
| :--- | :--- |
| uid | User id |
| size | For video size (width and height), see [CGSize for details](#cgsize) |
| rotation | Rotation information [0 , 360] |

--------------------------

#### ThunderEventDelegate:thunderEngine:onVideoCaptureStatus:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onVideoCaptureStatus:(ThunderVideoCaptureStatus)status;
```

Notification of change in camera capture status.

> **Note:**
>
> - Enable camera capture. When device for camera capture changes in status, this notification will be received.

##### Parameter[](#onvideocapturestatus)

| Parameter | Description |
| :--- | :--- |
| status | For status of camera capture, see [ThunderVideoCaptureStatus for details](#thundervideocapturestatus) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onConnectionStatus:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onConnectionStatus:(ThunderConnectionStatus)status;
```

This interface will be called upon change of connection between SDK and server.

##### Parameter[](#onconnectionstatus)

| Parameter | Description |
| :--- | :--- |
| status | For status of connection between SDK and server, see [ThunderConnectionStatus for details](#thunderconnectionstatus) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRoomStats:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onRoomStats:(nonnull RoomStats*)stats;
```

Notification of upstream/downstream traffic

> **Note:**
>
> - Notification of upstream/downstream traffic pops out once 2s.

##### Parameter[](#onroomstats)

| Parameter | Description |
| :--- | :--- |
| stats | For statistics of upstream/downstream traffic, see [RoomStats for details](#roomstats) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onFirstLocalAudioFrameSent:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onFirstLocalAudioFrameSent:(NSInteger)elapsed;
```
Callback on the first local audio frame sent.

##### Parameter[](#onfirstlocalaudioframesent)

| Parameter | Description |
| :--- | :--- |
| elapsed | Time (ms) consumed from callback of [joinRoom](function.html#thunderenginejoinroomroomnameuid) API to callback of the event |

--------------------------

#### ThunderEventDelegate:thunderEngine:onFirstLocalVideoFrameSent:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onFirstLocalVideoFrameSent:(NSInteger)elapsed;
```

Callback on the first local video frame sent.

##### Parameter[](#onfirstlocalvideoframesent)

| Parameter | Description |
| :--- | :--- |
| elapsed | Time (ms) consumed from callback of [joinRoom](function.html#thunderenginejoinroomroomnameuid) API to callback of the event |

--------------------------

#### ThunderEventDelegate:thunderEngine:onPublishStreamToCDNStatusWithUrl:errorCode:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine
  onPublishStreamToCDNStatusWithUrl:(NSString *_Nonnull)url
  errorCode:(ThunderPublishCDNErrorCode)errorCode;
```

Callback on cdn stream publishing result.
> **Note:**
>
> - This callback will be triggered when calling addPublishOriginStreamUrl to set publishing source stream to CDN or when calling addPublishTranscodingStreamUrl to set publishing mixed video stream to CDN, after publishing or setting up transcoding task.
> - To notify whether CDN stream publishing succeeds. If it fails, errorCode will indicate the specific reason.
> - This callback will be triggered when stream publishing status changes, or every 10s when publish stream status stays unchanged.

##### Parameter[](#onpublishstreamtocdnstatuswithurl)

| Parameter | Description |
| :--- | :--- |
| url | Target url of stream publishing |
| errorCode | For stream publishing error code, see [ThunderPublishCDNErrorCode](#thunderpublishcdnerrorcode) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onNetworkTypeChanged:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onNetworkTypeChanged:(NSInteger)type;
```

Callback on network type change.

##### Parameter[](#onnetworktypechanged)

| Parameter | Description |
| :--- | :--- |
| type | <br> THUNDER_NETWORK_TYPE_UNKNOWN(0): Network connection type unknown <br>THUNDER_NETWORK_TYPE_DISCONNECTED(1): Network disconnected<br>THUNDER_NETWORK_TYPE_CABLE(2): Wired network<br>THUNDER_NETWORK_TYPE_WIFI(3): Wi-Fi (including hotspot)<br>THUNDER_NETWORK_TYPE_MOBILE(4): Mobile network, 2G, 3G or 4G not distinguished<br>THUNDER_NETWORK_TYPE_MOBILE_2G(5): 2G mobile network<br>THUNDER_NETWORK_TYPE_MOBILE_3G(6): 3G mobile network<br>THUNDER_NETWORK_TYPE_MOBILE_4G(7): 4G mobile network <br> |

--------------------------

#### ThunderEventDelegate:thunderEngine:onLocalVideoStats:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onLocalVideoStats:(ThunderRtcLocalVideoStats * _Nonnull)stats;
```

Notification of statistics of local video

> **Note:**
>
> - The statistics of sending of video stream by local device is described during this callback. Callback time: 1. immediate callback when the publishing interface is called; 2. immediate callback on bracket change during the publishing; and 3. periodical callback at an interval of 2s.

##### Parameter[](#onlocalvideostats)

| Parameter | Description |
| :--- | :--- | :--- |
| stats | For statistics of local video, see [ThunderRtcLocalVideoStats](#thunderrtclocalvideostats) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onLocalAudioStats:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onLocalAudioStats:(ThunderRtcLocalAudioStats * _Nonnull)stats;
```

Notification of statistics of local audio.

> **Note:**
>
> - The statistics of sending of video stream by local device is described during this callback. Callback time: periodical callback at an interval of 2s.

##### Parameter[](#onlocalaudiostats)

| Parameter | Description |
| :--- | :--- |
| stats | For statistics of local audio, see [ThunderRtcLocalAudioStats](#thunderrtclocalaudiostats) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onAudioCaptureStatus:

```objc
- (void)thunderEngine:(ThunderEngine *_Nonnull)engine onAudioCaptureStatus:(NSInteger)status;
```

Notification of change in audio device capture status.

> **Note:**
>
> - Enable audio capture. When device for audio capture changes in status, this notification will be received

##### Parameter[](#onaudiocapturestatus)

| Parameter | Description |
| :--- | :--- |
| status | For status of audio device, see [ThunderAudioDeviceStatus](#thunderaudiodevicestatus) |

--------------------------

#### ThunderEventDelegate:thunderEngineConnectionLost:

```objc
- (void)thunderEngineConnectionLost:(ThunderEngine *_Nonnull)engine;
```

Callback of interruption of network connection with server.

> **Note:**
>
> - After calling joinRoom, regardless of whether joining is successful or not, SDK will trigger this callback as long as server cannot be connected in 10 seconds. Before app proactively calls leaveRoom, SDK will be automatically reconnecting.

--------------------------

#### ThunderEventDelegate:thunderEngine:onTokenWillExpire:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onTokenWillExpire:(nonnull NSString*)token;
```

Callback of near expiration of server's authentication.

> **Note:**
>
> - SDK will call back this interface 30s before expiration of the token.

##### Parameter[](#ontokenwillexpire)

| Parameter | Description |
| :--- | :--- |
| token | Token of near-expiration of service |

--------------------------

#### ThunderEventDelegate:thunderEngineTokenRequest:

```objc
- (void)thunderEngineTokenRequest:(ThunderEngine * _Nonnull)engine;
```

Callback of expiration of server's authentication.

> **Note:**
>
> - SDK will call back this interface upon expiration of the token.

--------------------------

#### ThunderEventDelegate:thunderEngine:onUserBanned:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onUserBanned:(BOOL)status;
```

Callback during banning period of the user.

##### Parameter[](#onuserbanned)

| Parameter | Description |
| :--- | :--- |
| status | Banning status (YES-Ban  NO-Unban) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onUserJoined:elapsed:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine onUserJoined:(nonnull NSString*)uid elapsed:(NSInteger)elapsed;
```

Callback of remote user joining the room.

> **Note:**
>
> - Validated only in audio mode.

##### Parameter[](#onuserjoined)

| Parameter | Description |
| :--- | :--- |
| uid | Remote user id |
| elapsed | Delay (ms) from local user’s calling joinRoom to triggering the callback |

--------------------------

#### ThunderEventDelegate:thunderEngine:onUserOffline:reason:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
        onUserOffline:(nonnull NSString*)uid
        reason:(ThunderLiveRtcUserOfflineReason)reason;
```

Callback of remote user leaving the room.

> **Note:**
>
> - Validated only in audio mode.

##### Parameter[](#onuseroffline)

| Parameter | Description |
| :--- | :--- |
| uid | Remote user id |
| reason | For offline reason, see [ThunderLiveRtcUserOfflineReason](#thunderlivertcuserofflinereason) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onNetworkQuality:txQuality:rxQuality:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
     onNetworkQuality:(nonnull NSString*)uid
     txQuality:(ThunderLiveRtcNetworkQuality)txQuality
     rxQuality:(ThunderLiveRtcNetworkQuality)rxQuality;
```

Callback on uplink/downlink quality report.

##### Parameter[](#onnetworkquality)

| Parameter | Description |
| :--- | :--- |
| uid | It means this callback indicates the network quality of user of the id. When the uid is 0, network quality of local user is returned |
| txQuality | For uplink network quality of this user, see [ThunderLiveRtcNetworkQuality](#thunderlivertcnetworkquality) |
| rxQuality | For downlink network quality of this user, see [ThunderLiveRtcNetworkQuality](#thunderlivertcnetworkquality) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRemoteVideoStatsOfUid:stats:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
        onRemoteVideoStatsOfUid:(nonnull NSString*)uid
        stats:(ThunderRtcRemoteVideoStats* _Nonnull)stats;
```

Callback on remote video stream information during the call.

> **Note:**
>
> - The end-to-end video stream status in calling of remote users is described during this callback, which is triggered once 2s for each remote user/anchor. In case multiple users/anchors exist remotely at the same time, this callback will be triggered multiple times every 2 seconds.

##### Parameter[](#onremotevideostatsofuid)

| Parameter | Description |
| :--- | :--- |
| uid | Id of remote user/anchor |
| stats | For statistics of remote video, see [ThunderRtcRemoteVideoStats](#thunderrtcremotevideostats) |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRemoteAudioStatsOfUid:stats:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
        onRemoteAudioStatsOfUid:(nonnull NSString*)uid
        stats:(ThunderRtcRemoteAudioStats* _Nonnull)stats;
```

Callback on remote audio stream information during the call.

> **Note:**
>
> - The statistics of end-to-end audio in calling of remote users is described during this callback, which is triggered once 2s for each remote user/anchor. If there are multiple users/anchors existing remotely at the same time, SDK will be triggered several times every 2s.

##### Parameter[](#onremoteaudiostatsofuid)

| Parameter | Description |
| :--- | :--- |
| uid | Id of remote user/anchor |
| stats | For statistics of remote audio, see [ThunderRtcRemoteAudioStats](#thunderrtcremoteaudiostats) |

--------------------------

#### ThunderVideoDecodeFrameObserver:onVideoDecodeFrame:pts:uid:

```objc
- (void) onVideoDecodeFrame:(CVPixelBufferRef)pixelBuf pts:(uint64_t)pts uid:(NSString*)uid;
```

Custom rendering of a decoded image is to cut out the decoded image of SDK for custom rendering of services.

> **Note:**
>
> - There may be multiple video streams in the room, and the ThunderDecodeFrameObserver interface protocol should be set for different uid video streams.

##### Parameter[](#onvideodecodeframe)

| Parameter | Description |
| :--- | :--- |
| pixelBuf | buf pointer of current frame |
| pts | Time shown in current frame (pts) |
| uid | View the other's uid |

--------------------------

#### ThunderVideoCaptureFrameObserver:needThunderVideoCaptureFrameDataType:

```objc
- (ThunderVideoCaptureFrameDataType)needThunderVideoCaptureFrameDataType;
```

> ThunderVideoCaptureFrameObserver has defined a set of interfaces, through which the developer can create the pre-processing process for video images, and return the result in the returned parameter to SDK to continue the encoding.

Declaration is made to SDK on which format of data will be used. The following two methods will be called in accordance with the format set. Which format of data is used for callback?

##### Return value

For type of video capture data called back, see [ThunderVideoCaptureFrameDataType for details](#thundervideocaptureframedatatype)

--------------------------

#### ThunderVideoCaptureFrameObserver:onVideoCaptureFrame:PixelBuffer:

```objc
- (CVPixelBufferRef _Nullable)onVideoCaptureFrame:(EAGLContext *_Nonnull)glContext
                                      PixelBuffer:(CVPixelBufferRef _Nonnull)pixelBuf;
```

> ThunderVideoCaptureFrameObserver has defined a set of interfaces, through which the developer can create the pre-processing process for video images, and return the result in the returned parameter to SDK to continue the encoding.

Receive a frame of data from capture for processing and return processed data

> **Note:**
>
> - SDK returns the original PixelBuffer to the developer via interface. After the developer processes the PixelBuffer, the result is returned to SDK in form of return value for further procedure.

##### Parameter[](#onvideocaptureframe)

| Parameter | Description |
| :--- | :--- |
| glContext | EAGLContext |
| pixelBuf | buf pointer of current frame |

--------------------------

#### ThunderVideoCaptureFrameObserver:onVideoCaptureFrame:PixelBuffer:SourceTextureID:DestinationTextureID:TextureFormat:TextureTarget:TextureWidth:TextureHeight:

```objc
- (BOOL)onVideoCaptureFrame:(EAGLContext *_Nonnull)context
                PixelBuffer:(CVPixelBufferRef _Nonnull)pixelBuffer
            SourceTextureID:(unsigned int)srcTextureID
       DestinationTextureID:(unsigned int)dstTextureID
              TextureFormat:(int)textureFormat
              TextureTarget:(int)textureTarget
               TextureWidth:(int)width
              TextureHeight:(int)height;
```

> ThunderVideoCaptureFrameObserver has defined a set of interfaces, through which the developer can create the pre-processing process for video images, and return the result in the returned parameter to SDK to continue the encoding.

Receive a frame of data from capture for processing and return processed data Process data by OpenGL texture ID.

> **Note:**
>
> - SDK converts pixelBuffer into srcTextureID and dstTextureID via interface to return to the developer. Developer can operate the texture and render the final result in dstTextureID. SDK will take dstTextureID as data to perform the next work flow.

##### Parameter[](#onvideocaptureframe)

| Parameter | Description |
| :--- | :--- |
| context | EAGLContext |
| pixelBuffer | Original image pixelBuffer |
| srcTextureID | Source texture id |
| dstTextureID | Destination texture id |
| textureFormat | Texture format |
| textureTarget | texture target |
| width | Texture width |
| height | Texture height |

##### Return[](#onvideocaptureframe)

- YES

--------------------------

#### ThunderEventDelegate:thunderEngine:onLeaveRoomWithStats:

```objc
- (void)thunderEngine:(ThunderEngine* _Nonnull)engine onLeaveRoomWithStats:(ThunderRtcRoomStats* _Nonnull)stats;
```

Callback on leaving room.

> **Note:**
>
> - When leaveRoom is called, this notification will be received upon normal leaving of the room.

##### Parameter[](#onleaveroomwithstats)

| Parameter | Description |
| :--- | :--- |
| stats | Leave room status, reserved parameter type, not realized momentarily |

--------------------------

#### ThunderEventDelegate:thunderEngine:onCaptureVolumeIndication:cpt:micVolume:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
onCaptureVolumeIndication:(NSInteger)totalVolume
                  cpt:(NSUInteger)cpt
            micVolume:(NSInteger)micVolume;
```

Callback on capture volume

> **Note:**
>
> - This callback is set with the [enableCaptureVolumeIndication](function.html#thunderengineenablecapturevolumeindicationmorethanthdlessthanthdsmooth) interface.

##### Parameter[](#oncapturevolumeindication)

| Parameter | Description |
| :--- | :--- |
| totalVolume | Total volume of capture (including microphone capture and file playback) [0-100] |
| cpt | Capture timestamp (ms) |
| micVolume | Volume of microphone capture [0-100] |

--------------------------

#### ThunderEventDelegate:thunderEngine:onRecvUserAppMsgData:uid:

```objc
- (void)thunderEngine:(ThunderEngine * _Nonnull)engine
  onRecvUserAppMsgData:(nonnull NSData*)msgData
                   uid:(nonnull NSString*)uid;
```

Callback of receiving service-customized broadcast message.

> **Note:**
>
> - This callback calls back the passthrough message received by the user and uid of the user sending the message.

##### Parameter[](#onrecvuserappmsgdata)

| Parameter | Description |
| :--- | :--- |
| msgData | Pass-through message received |
| uid | Uid of user sending the message |

--------------------------

### ThunderMediaExtraInfoDelegate

#### ThunderMediaExtraInfoDelegate::onSendMediaExtraInfoFailedStatus:

```objc
- (void)onSendMediaExtraInfoFailedStatus:(NSUInteger)status;
```

Callback on failure in sending media extra information.

> **Note:**
>
> - For return failure status, see [ThunderSendMediaExtraInfoFailedStatus](#thundersendmediaextrainfofailedstatus)

--------------------------

#### ThunderMediaExtraInfoDelegate::onRecvMediaExtraInfo:ofUid:

```objc
- (void)onRecvMediaExtraInfo:(nonnull NSData*)data ofUid:(nonnull NSString*)uid;
```

Receive media extra information.

##### Parameter[](#onrecvmediaextrainfo)

| Parameter | Description |
| :--- | :--- |
| Date | User uid |
| uid | Media extra information |

--------------------------

#### ThunderMediaExtraInfoDelegate::onRecvMixAudioInfo:ofUid:

```objc
- (void)onRecvMixAudioInfo:(nonnull NSArray<ThunderMixAudioInfo*>*)infos ofUid:(nonnull NSString*)uid;
```

Extra information of mixed audio stream received.

##### Parameter[](#onrecvmixaudioinfo)

| Parameter | Description |
| :--- | :--- |
| infos | Original information about mixed audio stream indicates sources of this mixed audio stream. See [ThunderMixAudioInfo for details](#thundermixaudioinfo) |
| uid | Mixed audio stream uid |

--------------------------

#### ThunderMediaExtraInfoDelegate::onRecvMixVideoInfo:ofUid:

```objc
- (void)onRecvMixVideoInfo:(nonnull NSArray<ThunderMixVideoInfo*>*)infos ofUid:(nonnull NSString*)uid;
```

Extra information of mixed video stream received.

##### Parameter[](#onrecvmixvideoinfo)

| Parameter | Description |
| :--- | :--- |
| uid | Mixed video stream uid |
| infos | Original information about mixed video stream indicates sources of this mixed video stream. See [ThunderMixAudioInfo for details](#thundermixvideoinfo) |

--------------------------

### IAudioFrameObserver

#### IAudioFrameObserver::onRecordAudioFrame:

```c++
virtual void Thunder::IAudioFrameObserver::onRecordAudioFrame(AudioFrame& audioFrame);
```

Callback on raw audio capture data.

> **Note:**
>
> - This interface adopts the C++ method. The user calls the [registerAudioFrameObserver](#registeraudioframeobserver) interface and has registered the IAudioFrameObserver. Meanwhile, when the user starts capture, this callback will be received.

##### Parameter[](#onrecordaudioframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

#### IAudioFrameObserver::onPlaybackAudioFrame:

```c++
virtual void Thunder::IAudioFrameObserver::onPlaybackAudioFrame(AudioFrame& audioFrame);
```

Callback on raw audio play data.

> **Note:**
>
> - This interface adopts the C++ method. The user calls the [registerAudioFrameObserver](#registeraudioframeobserver) interface and has registered the IAudioFrameObserver. Meanwhile, when there’s audio data being played, this callback will be received.

##### Parameter[](#onplaybackaudioframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

#### IAudioFrameObserver::onPlaybackAudioFrameBeforeMixing:

```c++
virtual void Thunder::IAudioFrameObserver::onPlaybackAudioFrameBeforeMixing(char* uid, AudioFrame& audioFrame);
```

Callback of original data decoded by remote user can differentiate users through different uids.

> **Note:**
>
> - This interface adopts the C++ method. The user calls the [registerAudioFrameObserver](#registeraudioframeobserver) interface and has registered the IAudioFrameObserver. Meanwhile, when there’s remote audio data being played, this callback will be received.

##### Parameter[](#onplaybackaudioframebeforemixing)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Remote user uid |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

### ThunderAudioFilePlayerDelegate

#### ThunderAudioFilePlayerDelegate::onAudioFilePlayEnd:

```objc
- (void)onAudioFilePlayEnd:(nonnull ThunderAudioFilePlayer*)player;
```

End of audio file playback.

##### Parameter[](#onaudiofileplayend)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFilePlayError:errorCode:

```objc
- (void)onAudioFilePlayError:(nonnull ThunderAudioFilePlayer*)player errorCode:(int)errorCode;
```

Callback on audio file playback error

##### Parameter[](#onaudiofileplayerror)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |
| errorCode | errorCode = 0:  Opening file successful <br>errorCode = -1: Error in parsing file format <br>errorCode = -2: Error in decoding file format <br>errorCode = -3: Unsupported file format <br>errorCode = -4: File path not in existence |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFilePlaying:

```objc
- (void)onAudioFilePlaying:(nonnull ThunderAudioFilePlayer*)player;
```

Start playing.

##### Parameter[](#onaudiofileplaying)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFilePause:

```objc
- (void)onAudioFilePause:(nonnull ThunderAudioFilePlayer*)player;
```

Pause playing.

##### Parameter[](#onaudiofilepause)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFileResume:

```objc
- (void)onAudioFileResume:(nonnull ThunderAudioFilePlayer*)player;
```

Resume playing.

##### Parameter[](#onaudiofileresume)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFileStop:

```objc
- (void)onAudioFileStop:(nonnull ThunderAudioFilePlayer*)player;
```

Callback on playback being stopped by user.

##### Parameter[](#onaudiofilestop)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFileSeekComplete:milliseconds:

```objc
- (void)onAudioFileSeekComplete:(nonnull ThunderAudioFilePlayer*)player milliseconds:(int)milliseconds;
```

Forwarding to specified time completed.

##### Parameter[](#onaudiofileseekcomplete)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |
| milliseconds | Actual fast forward progress |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFileVolume:volume:currentMs:totalMs:

```objc
- (void)onAudioFileVolume:(nonnull ThunderAudioFilePlayer*)player
                   volume:(uint32_t)volume
                   currentMs:(uint32_t)currentMs
                   totalMs:(uint32_t)totalMs;
```

Audio playing volume.

##### Parameter[](#onaudiofilevolume)

| Parameter | Description |
| :--- | :--- |
| player | Pointer of file playing object |
| volume | Playing volume |
| currentMs | Current playing duration |
| totalMs | Total playing duration |

--------------------------

#### ThunderAudioFilePlayerDelegate::onAudioFileStateChange:event:errorCode

```objc
- (void)onAudioFileStateChange:(nonnull ThunderAudioFilePlayer*)player event:(ThunderAudioFilePlayerEvent)event  errorCode:(ThunderAudioFilePLayerErrorCode)errorCode;
```

Notification of changes in player status.

##### Parameter[](#onaudiofilestatechange)

| Parameter | Description |
| :--- | :--- |
| player |  Pointer of file playing object |
| event | player event，see [ThunderAudioFilePlayerEvent](#thunderaudiofileplayerevent) |
| errorCode | For other errors，see [ThunderAudioFilePLayerErrorCode](#thunderaudiofileplayererrorcode) |

--------------------------

### ThunderCustomVideoSourceProtocol

#### ThunderCustomVideoSourceProtocol::onInitialize

```objc
- (BOOL)onInitialize:(nullable id<ThunderVideoFrameConsumer>)protocol;
```

Initialize video source.

When initializing video source, Engine will call this method. The developer can make some preparations in this method, e.g. opening the camera, initializing the video source, and telling Engine via return value whether the customized video source is ready. 
In initializing the video source, the developer shall specify a Buffer type in bufferType, and use only the method corresponding to it in customized video source to transmit the video frame data. 
In initializing the video source, Engine will transmit a ThunderVideoFrameConsumer object to the developer. The developer shall save this object, and input the video frame to Engine via this object after the video source is enabled.

##### Parameter[](#oninitialize)

| Parameter | Description |
| :--- | :--- |
| protocol | For operation object of external video frame, see [ThunderVideoFrameConsumer for details](function.html#thundervideoframeconsumer) |

##### Return value[](#oninitialize)

- YES: Initializing customized video source completed.
- NO: Customized video source device is not ready or fails in initialization. Engine will stop and report the error.

--------------------------

#### ThunderCustomVideoSourceProtocol::bufferType

```objc
- (ThunderVideoBufferType)bufferType;
```

Acquire Buffer type.

In initialization, Engine will call this method to consult the Buffer type used by this video source. The developer must and can only specify one Buffer type and tell Media Engine via return value.

##### Return value[](#buffertype)

- [ThunderVideoBufferType](#thundervideobuffertype) Buffer type used by the video.

--------------------------

#### ThunderCustomVideoSourceProtocol::onStart

```objc
- (void)onStart;
```

Start video source.

In initialization, Engine will call this method to consult the Buffer type used by this video source. The developer must and can only specify one Buffer type and tell Media Engine via return value.

--------------------------

#### ThunderCustomVideoSourceProtocol::onStop

```objc
- (void)onStop;
```

Stop video source.

This method will be called when the video source is stopped. The developer can stop collecting videos in this method. Media Engine notifies the developer via this callback that the frame input switch of ThunderVideoFrameConsumer is about to close and video frame input afterwards will be discarded.

--------------------------

#### ThunderCustomVideoSourceProtocol::onDispose

```objc
- (void)onDispose;
```

Dispose video source.

Engine notifies the developer that the video source is about to be invalidated and he can shut down the video source device in this method. Engine will destroy the ThunderVideoFrameConsumer object and the developer shall ensure it will no longer be used after this callback.

--------------------------

### ThunderExternalAudioProcessorDelegate

#### ThunderExternalAudioProcessorDelegate::audioCaptureStart

```objc
- (void)audioCaptureStart;
```

Audio capture starts.

--------------------------

#### ThunderExternalAudioProcessorDelegate::audioCaptureData:data:len:sampleRate:channelCount:bitPerSample:

```objc
- (void)audioCaptureData:(void*_Nonnull)data
                     len:(uint32_t)len
              sampleRate:(uint32_t)sampleRate
            channelCount:(uint32_t)channelCount
            bitPerSample:(uint32_t)bitPerSample;
```

Callback on audio acquisition data.

##### Parameter[](#audiocapturedata)

| Parameter | Description |
| :--- | :--- |
| Date | Audio data |
| len | Audio duration |
| sampleRate | Audio sampling rate |
| channelCount | Channel count |
| bitPerSample | Bit width of sampling point |

--------------------------

#### ThunderExternalAudioProcessorDelegate::audioCaptureStop

```objc
- (void)audioCaptureStop;
```

Audio capture stops.

--------------------------

#### ThunderExternalAudioProcessorDelegate::audioRenderStart

```objc
- (void)audioRenderStart;
```

Audio rendering starts.

--------------------------

#### ThunderExternalAudioProcessorDelegate::audioRenderData:data:len:sampleRate:channelCount:bitPerSample:

```objc
-(void)audioRenderData:(void*_Nonnull)data
                   len:(uint32_t)len
            sampleRate:(uint32_t)sampleRate
          channelCount:(uint32_t)channelCount
          bitPerSample:(uint32_t)bitPerSample;
```

Callback on audio rendering data.

##### Parameter[](#audiorenderdata)

| Parameter | Description |
| :--- | :--- |
| Date | Audio data |
| len | Audio duration |
| sampleRate | Audio sampling rate |
| channelCount | Channel count |
| bitPerSample | Bit width of sampling point |

--------------------------

#### ThunderExternalAudioProcessorDelegate::audioRenderStop

```objc
- (void)audioRenderStop;
```

Audio rendering stops.

--------------------------

## Enumerated values & structure definition

#### AudioFrame

```c++
struct IAudioFrameObserver::AudioFrame;
```

Detailed information of audio data

| Parameter | Meaning |
| :--- | :--- |
| type | For audio frame type, see [AUDIO_FRAME_TYPE for details](#audio-frame-type) |
| samples | Sample quantity of the frame |
| bytesPerSample | Bytes per sample: PCM (16 digits) contains two types |
| channels | Number of channels (crossed data for stereo); 1: single track, 2: dual track |
| samplesPerSec | Sampling rate |
| buffer | data buffer |
| renderTimeMs | Not used momentarily |
| avsync_type | Not used momentarily |

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

#### ThunderRtcScenarioMode

```objc
typedef NS_ENUM(NSInteger, ThunderRtcScenarioMode);
```

Set scenario mode

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SCENARIO_MODE_DEFAULT(0) | =1 by default |
| THUNDER_SCENARIO_MODE_STABLE_FIRST(1) | Fluent priority: applicable for stable education |
| THUNDER_SCENARIO_MODE_QUALITY_FIRST(2) | Tone quality priority: applicable for show field with a few or without interaction |

--------------------------

#### ThunderRtcLogLevel

```objc
typedef NS_ENUM(NSInteger, ThunderRtcLogLevel);
```

Set log level

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_LOG_LEVEL_TRACE(0) | TRACE |
| THUNDER_LOG_LEVEL_DEBUG(1) | DEBUG |
| THUNDER_LOG_LEVEL_INFO(2) | INFO |
| THUNDER_LOG_LEVEL_WARN(3) | WARN |
| THUNDER_LOG_LEVEL_ERROR(4) | ERROR |

--------------------------

#### ThunderRtcSdkAuthResult

```objc
typedef NS_ENUM(NSInteger, ThunderRtcSdkAuthResult);
```

Authentication results

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SDK_AUTHRES_SUCCUSS(0) | Authentication succeeded |
| THUNDER_SDK_AUTHRES_ERR_SERVER_INTERNAL(10000) | Server internal error, try again |
| THUNDER_SDK_AUTHRES_ERR_NO_TOKEN(10001) | Without token, [ThunderAPI updateToken needs calling:] |
| THUNDER_SDK_AUTHRES_ERR_TOKEN_ERR(10002) | Token authentication failed (incorrect digital signature), which may be caused by incorrect appSecret |
| THUNDER_SDK_AUTHRES_ERR_APPID(10003) | appid in token is inconsistent with appid when execute authentication |
| THUNDER_SDK_AUTHRES_ERR_UID(10004) | uid in token is inconsistent with uid when execute authentication |
| THUNDER_SDK_AUTHRES_ERR_TOKEN_EXPIRE(10005) | token has expired |
| THUNDER_SDK_AUTHRES_ERR_NO_APP(10006) | App does not exist, which is not registered in the management background |
| THUNDER_SDK_AUTHRES_ERR_TOKEN_WILL_EXPIRE(10007) | token is about to expire |
| THUNDER_SDK_AUTHRES_ERR_BAND(10008) | The user is baned |

--------------------------

#### ThunderLiveRtcUserOfflineReason

```objc
typedef NS_ENUM(NSUInteger, ThunderLiveRtcUserOfflineReason);
```

Offline reason

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SDK_USER_OFF_LINE_REASON_QUIT(1) | The user is offline actively |
| THUNDER_SDK_USER_OFF_LINE_REASON_DROPPED(2) | Go offline for timeout, because no data received from the other side for a long time |
| THUNDER_SDK_USER_OFF_LINE_REASON_BECOME_AUDIENCE(3) | User status is switched from anchor to audience (live mode) |

--------------------------

#### ThunderLiveRtcNetworkQuality

```objc
typedef NS_ENUM(NSUInteger, ThunderLiveRtcNetworkQuality);
```

Network quality

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SDK_NETWORK_QUALITY_UNKNOWN(0) | Unknown quality |
| THUNDER_SDK_NETWORK_QUALITY_EXCELLENT(1) | Excellent network quality |
| THUNDER_SDK_NETWORK_QUALITY_GOOD(2) | Good network quality |
| THUNDER_SDK_NETWORK_QUALITY_POOR(3) | The network quality is poor, but the communication is not affected even the user can feel its defects. |
| THUNDER_SDK_NETWORK_QUALITY_BAD(4) | The network quality is bad, and the communication can be barely made but is not smooth |
| THUNDER_SDK_NETWORK_QUALITY_VBAD(5) | The network quality is very bad, the communication cannot be made basically |
| THUNDER_SDK_NETWORK_QUALITY_DOWN(6) | The network has been disconnected, and the communication cannot be made at all |

--------------------------

#### ThunderSendMediaExtraInfoFailedStatus

```objc
typedef NS_ENUM(NSUInteger, ThunderSendMediaExtraInfoFailedStatus);
```

Status of failure in sending media extra information

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_EMPTY(1) | Extra information is null. |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_TOO_LARGE(2) | Data sent each time is too large. It shall not exceed 200Byte each time when only audio is published, or 2048Byte each time when video is published |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_FREQUENCY_TOO_HIGHT(3) | The sending frequency is too high, which cannot exceeds 100ms each time |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NOT_IN_ANCHOR_SYSTEM(4) | Not an anchor system |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_JOIN_MEDIA(5) | Channel not to be joined |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_PUBLISH_SUCCESS(6) | Publishing failed |

--------------------------

#### ThunderVideoCaptureStatus

```objc
typedef NS_ENUM(NSInteger, ThunderVideoCaptureStatus);
```

Callback of video capture status

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_STATUS_SUCEESS(0) | Open successfully. Fail to detect ios currently. Add this value to unify with Android |
| THUNDER_VIDEO_CAPTURE_STATUS_AUTHORIZED(1) | User authorization |
| THUNDER_VIDEO_CAPTURE_STATUS_NOT_DETERMINED(2) | Users don’t give authority |
| THUNDER_VIDEO_CAPTURE_STATUS_RESTRICTED(3) | Occupied |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(4) | Users refuse to give authority |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(5) | Camera closed |

--------------------------

#### ThunderVideoCaptureFrameDataType

```objc
typedef NS_ENUM(NSInteger, ThunderVideoCaptureFrameDataType);
```

Type of video capture data called back

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_DATATYPE_PIXELBUFFER(0) | SDK will return the camera data of pixelbuffer |
| THUNDER_VIDEO_CAPTURE_DATATYPE_TEXTURE(1) | SDK will return the data of texture ID |

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

#### RoomStats

```objc
__attribute__((visibility("default"))) @interface RoomStats : NSObject
@property(nonatomic, assign) uint32_t txBitrate; // Chain sending bit rate (unit: bps)
@property(nonatomic, assign) uint32_t rxBitrate; // Chain receiving bit rate (unit: bps)
@property(nonatomic, assign) uint32_t txAudioBitrate; // Audio packet sending bit rate (unit: bps)
@property(nonatomic, assign) uint32_t rxAudioBitrate; // Audio packet receiving bit rate (unit: bps)
@property(nonatomic, assign) uint32_t txVideoBitrate; // Video packet sending bit rate (unit: bps)
@property(nonatomic, assign) uint32_t rxVideoBitrate; // Video packet receiving bit rate (unit: bps)
@end
```

Statistics of upstream/downstream traffic

--------------------------

#### ThunderPublishCDNErrorCode

```objc
typedef NS_ENUM(NSInteger, ThunderPublishCDNErrorCode);
```

Publish stream to external server result status code.

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_PUBLISH_CDN_ERR_SUCCESS(0) | Stream publishing succeeded |
| THUNDER_PUBLISH_CDN_ERR_TOCDN_FAILED(1) | Publishing stream to external server (CDN) is failed. <br>1. Check whether url is correct. <br>2. Check whether the token in the URL is valid (generally, token is required during cdn stream publishing and can be ignored if it doe not exist). |
| THUNDER_PUBLISH_CDN_ERR_THUNDERSERVER_FAILED(2) | Publish the stream to thunder internal server is failed. <br>1. Check anchor’s upstream network <br>2. Contact us to troubleshoot internal transmission problems |

--------------------------

#### ThunderRtcLocalVideoStats

```objc
__attribute__((visibility("default"))) @interface ThunderRtcLocalVideoStats : NSObject
@property (assign, nonatomic) NSUInteger sendBitrate;  // Actual sending bit rate (Kbps)
@property (assign, nonatomic) NSUInteger sendFrameRate; // Actual sending frame rate (unit: fps)
@property (assign, nonatomic) NSUInteger encoderOutputFrameRate;// Output frame rate of local encoder (unit: fps)
@property (assign, nonatomic) NSUInteger renderOutputFrameRate;// Output frame rate of local renderer (unit: fps)
@property (assign, nonatomic) NSUInteger targetBitrate;// Target encoding bit rate of current encoder (unit: Kbps)
@property (assign, nonatomic) NSUInteger targetFrameRate;// Target encoding frame rate of current coder (unit: fps)
// Quality adaptability of local videos since last statistics (based on target frame rate and target bit rate)
@property (assign, nonatomic) ThunderVideoQualityAdaptIndication qualityAdaptIndication;
@property (assign, nonatomic) NSUInteger encodedBitrate;// Bit rate of video encoding (Kbps)
@property (assign, nonatomic) NSUInteger encodedFrameWidth;// Encoded video width (px)
@property (assign, nonatomic) NSUInteger encodedFrameHeight;// Encoded video height (px
@property (assign, nonatomic) NSUInteger encodedFrameCount;// Number of frames sent by video, an accumulated value
@property (assign, nonatomic) ThunderVideoCodecType codecType;// Encoding type of videos
@property (assign, nonatomic) NSUInteger configBitRate;  //Configured bit rate (kbps)
@property (assign, nonatomic) NSUInteger configFrameRate;// Configured frame rate
@property (assign, nonatomic) NSUInteger configWidth;// Video height configured
@property (assign, nonatomic) NSUInteger configHeight;// Video width configured
@end
```

Statistics of local video

--------------------------

#### ThunderRtcLocalAudioStats

```objc
__attribute__((visibility("default"))) @interface ThunderRtcLocalAudioStats : NSObject
@property (assign, nonatomic) NSUInteger numChannels;// Number of channels
@property (assign, nonatomic) NSUInteger sendSampleRate;// Sampling rate HZ
@property (assign, nonatomic) NSUInteger sendBitrate;// Sending bit rate (kbps)
@end
```

Statistics of local audio

--------------------------

#### ThunderAudioDeviceStatus

```objc
typedef NS_ENUM(NSInteger, ThunderAudioDeviceStatus);
```

Audio device capture status

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_SUCCESS(0) | Callback on successful initialization of audio capture device |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_ERROR_OR_NO_PERMISSION(1) | Callback on initialization failure of audio capture. It may be caused by no permission |
| THUNDER_AUDIO_DEVICE_STATUS_RELEASE_CAPTURE_SUCCESS(2) | Callback on successful release of audio capture device |

--------------------------

#### ThunderRtcRemoteVideoStats

```objc
__attribute__((visibility("default"))) @interface ThunderRtcRemoteVideoStats : NSObject
@property (assign, nonatomic) NSUInteger delay; // Delay from publishing remote video stream to playback
@property (assign, nonatomic) NSUInteger width; // Width of remote video stream
@property (assign, nonatomic) NSUInteger height; // Height of remote video stream
@property (assign, nonatomic) NSUInteger receivedBitrate; // Receiving bit rate (unit: Kbps)
@property (assign, nonatomic) NSUInteger decoderOutputFrameRate; // Output frame rate of remote video decoder (unit: fps)
@property (assign, nonatomic) NSUInteger rendererOutputFrameRate; // Output frame rate of remote video renderer (unit: fps)
@property (assign, nonatomic) NSUInteger packetLossRate; // Packet loss rate (%) of remote video after network confrontation
@property (assign, nonatomic) NSUInteger rxStreamType; // Types of video stream, including large stream and small stream
@property (assign, nonatomic) NSUInteger totalFrozenTime; // The accumulated time (ms) from the time when a remote user begins to punish to the time of video freezing
@property (assign, nonatomic) NSUInteger frozenRate; // The percentage (%) of the accumulated time (from the time when a remote user begins to publish to the time of video freezing) accounting for total effective time of videos
@end
```

Statistics of remote video

--------------------------

#### ThunderRtcRemoteAudioStats

```objc
__attribute__((visibility("default"))) @interface ThunderRtcRemoteAudioStats : NSObject
@property (assign, nonatomic) NSUInteger quality; // Quality of audio streams sent by remote users. 0: Unknown; 1: Excellent; 2: Good; 3: Poor, flawed but does not affect communication; 4: Bad, communication can be made but not smoothly; 5: Very Bad, communication can barely be made; 6: Disconnected, communication can not be made at all
@property (assign, nonatomic) NSUInteger networkTransportDelay; // Network delay from an audio sending end to an audio receiving end
@property (assign, nonatomic) NSUInteger jitterBufferDelay; // Delay from a receiving end to network jitter buffer
@property (assign, nonatomic) NSUInteger frameLossRate; // Frame loss rate (%) of remote audio streams
@property (assign, nonatomic) NSUInteger numChannels; // Number of channels
@property (assign, nonatomic) NSUInteger receivedSampleRate; // Sampling rate (Hz) of remote audios
@property (assign, nonatomic) NSUInteger receivedBitrate; // Average bit rate of remote audios within a statistical period
@property (assign, nonatomic) NSUInteger totalFrozenTime; // The accumulated time (ms) from the time when a remote user joins a channel to the time of audio freezing
@property (assign, nonatomic) NSUInteger frozenRate; // The percentage (%) of the accumulated time (from the time when a remote user joins a channel to the time of audio freezing) accounting for total effective time of audios
@end
```

Statistics of remote audio

--------------------------

#### ThunderMixAudioInfo

```objc
__attribute__((visibility("default")))@interface ThunderMixAudioInfo : NSObject
@property(copy, nonatomic) NSString* _Nonnull uid;
@property(assign, nonatomic) int volume; // [0,100]
@end
```

Source information of mixed video stream

--------------------------

#### ThunderMixVideoInfo

```objc
__attribute__((visibility("default"))) @interface ThunderMixVideoInfo : NSObject
@property(copy, nonatomic) NSString* _Nonnull uid; // User id
@property(assign, nonatomic) CGSize size; // Original width and height of this user's video
@property(assign, nonatomic) CGRect crop; // The region used to crop the original video in video mixing
@property(assign, nonatomic) CGRect layout; // Location of this user's video in video mixing canvas
@property(assign, nonatomic) int zOrder; // Layer number of this user's video frame in video mixing. The value range is the integer in [0, 100],
                                         // and the minimum value is 0, indicating that the image in this region is at the lowest level
@property(assign, nonatomic) float alpha; // Transparency of this user's video frame in video mixing. The value range is [0.0, 1.0].
                                          // 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque.
@end
```

Source information of mixed video stream

--------------------------

#### ThunderVideoBufferType

```objc
typedef NS_ENUM(NSInteger, ThunderVideoBufferType);
```

Buffer type

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEOBUFFER_TYPE_PIXELBUFFER(1) | Buffer using Pixel Buffer type |
| THUNDER_VIDEOBUFFER_TYPE_RAWDATA(2) | Buffer using Raw Data type |

--------------------------
