# Event callback

## Interface List

- 
   ### IThunderEventHandler

| public member functions | Function Name |
| ---:| :--- |
| virtual void | [onJoinRoomSuccess](#ithundereventhandleronjoinroomsuccess)(const char* roomId, const char* uid, int elapsed) = 0 |
| virtual void | [onLeaveRoom](#ithundereventhandleronleaveroom)() = 0 |
| virtual void | [onPlayVolumeIndication](#ithundereventhandleronplayvolumeindication)(const [AudioVolumeInfo](#audiovolumeinfo)* speakers, int speakerCount, int totalVolume) = 0 |
| virtual void | [onInputVolume](#ithundereventhandleroninputvolume)(unsigned volume) = 0 |
| virtual void | [onOutputVolume](#ithundereventhandleronoutputvolume)(unsigned volume) = 0 |
| virtual void | [onBizAuthResult](#ithundereventhandleronbizauthresult)(bool bPublish, [AUTH_RESULT](#auth-result) result) = 0 |
| virtual void | [onSdkAuthResult](#ithundereventhandleronsdkauthresult)([AUTH_RESULT](#auth-result) result) = 0 |
| virtual void | [onTokenWillExpire](#ithundereventhandlerontokenwillexpire)(const char* token) = 0 |
| virtual void | [onTokenRequest](#ithundereventhandlerontokenrequest)() = 0 |
| virtual void | [onUserBanned](#ithundereventhandleronuserbanned)(bool status) = 0 |
| virtual void | [onUserJoined](#ithundereventhandleronuserjoined)(const char* uid, int elapsed) = 0 |
| virtual void | [onUserOffline](#ithundereventhandleronuseroffline)(const char* uid, [USER_OFFLINE_REASON_TYPE](#user-offline-reason-type) reason) = 0 |
| virtual void | [onNetworkQuality](#ithundereventhandleronnetworkquality)(const char* uid, [NetworkQuality](#networkquality) txQuality, [NetworkQuality](#networkquality) rxQuality) = 0 |
| virtual void | [onFirstLocalVideoFrameSent](#ithundereventhandleronfirstlocalvideoframesent)(int elapsed) = 0 |
| virtual void | [onFirstLocalAudioFrameSent](#ithundereventhandleronfirstlocalaudioframesent)(int elapsed) = 0 |
| virtual void | [onRemoteAudioStopped](#ithundereventhandleronremoteaudiostopped)(const char* uid, bool stop) = 0 |
| virtual void | [onConnectionStatus](#ithundereventhandleronconnectionstatus)([ThunderConnectionStatus](#thunderconnectionstatus) status) = 0 |
| virtual void | [onConnectionLost](#ithundereventhandleronconnectionlost)() = 0 |
| virtual void | [onRemoteVideoStopped](#ithundereventhandleronremotevideostopped)(const char* uid, bool stop) = 0 |
| virtual void | [onVideoSizeChanged](#ithundereventhandleronvideosizechanged)(const char* uid, int width, int height, int rotation) = 0 |
| virtual void | [onRemoteVideoPlay](#ithundereventhandleronremotevideoplay)(const char* uid, int width, int height, int elapsed) = 0 |
| virtual void | [onNetworkTypeChanged](#ithundereventhandleronnetworktypechanged)([ThunderNetworkType](#thundernetworktype) type) = 0 |
| virtual void | [onAudioCaptureStatus](#ithundereventhandleronaudiocapturestatus)([ThunderAudioDeviceStatus](#thunderaudiodevicestatus) type) = 0 |
| virtual void | [onPublishStreamToCDNStatus](#ithundereventhandleronpublishstreamtocdnstatus)(const char* url, [ThunderPublishCDNErrorCode](#thunderpublishcdnerrorcode) errorCode) = 0 |
| virtual void | [onRoomStats](#ithundereventhandleronroomstats)([RoomStats](#roomstats) stats) = 0 |
| virtual void | [onRecvUserAppMsgData](#ithundereventhandleronrecvuserappmsgdata)(const char* uid, const char* msgData) = 0 |
| virtual void | [onSendAppMsgDataFailedStatus](#ithundereventhandleronsendappmsgdatafailedstatus)(int status) = 0 |
| virtual void | [onVideoCaptureStatus](#ithundereventhandleronvideocapturestatus)(int status) = 0 |
| virtual void | [onLocalVideoStats](#ithundereventhandleronlocalvideostats)(const [LocalVideoStats](#localvideostats) stats) = 0 |
| virtual void | [onLocalAudioStats](#ithundereventhandleronlocalaudiostats)(const [LocalAudioStats](#localaudiostats) stats) = 0 |
| virtual void | [onRemoteVideoStatsOfUid](#ithundereventhandleronremotevideostatsofuid)(const char* uid, const [RemoteVideoStats](#remotevideostats) stats) = 0 |
| virtual void | [onRemoteAudioStatsOfUid](#ithundereventhandleronremoteaudiostatsofuid)(const char* uid, const [RemoteAudioStats](#remoteaudiostats) stats) = 0 |

- 
   ### IAudioFrameObserver

| public member functions | Function Name |
| ---:| :--- |
| virtual bool | [onRecordAudioFrame](#iaudioframeobserveronrecordaudioframe)([AudioFrame](#audioframe)& audioFrame) = 0 |
| virtual bool | [onPlaybackAudioFrame](#iaudioframeobserveronplaybackaudioframe)([AudioFrame](#audioframe)& audioFrame) = 0 |
| virtual bool | [onPlaybackAudioFrameBeforeMixing](#iaudioframeobserveronplaybackaudioframebeforemixing)(char* uid, [AudioFrame](#audioframe)& audioFrame) = 0 |

- 
   ### IThunderAudioPlayerNotify

| public member functions | Function Name |
| ---:| :--- |
| virtual void | [onAudioFileVolume](#ithunderaudioplayernotifyonaudiofilevolume)(unsigned int volume, unsigned int currentMs, unsigned int totalMs) = 0 |
| virtual void | [onAudioFilePlayEnd](#ithunderaudioplayernotifyonaudiofileplayend)() = 0 |

- 
   ### IVideoFrameObserver

| public member functions | Function Name |
| ---:| :--- |
| virtual bool | [onPreviewVideoFrame](#ivideoframeobserveronpreviewvideoframe)([VideoFrame](#videoframe)& videoFrame) = 0 |
| virtual bool | [onRenderVideoFrame](#ivideoframeobserveronrendervideoframe)(const char* uid, [VideoFrame](#videoframe)& videoFrame) = 0 |

- 
   ### IVideoCaptureObserver

| public member functions | Function Name |
| ---:| :--- |
| virtual bool | [onCaptureVideoFrame](#ivideocaptureobserveroncapturevideoframe)([VideoFrame](#videoframe)& videoFrame) = 0 |

- 
   ### IThunderMediaExtraInfoObserver

| public member functions | Function Name |
| ---:| :--- |
| virtual void | [onSendMediaExtraInfoFailedStatus](#ithundermediaextrainfoobserveronsendmediaextrainfofailedstatus)(int status) = 0 |
| virtual void | [onRecvMediaExtraInfo](#ithundermediaextrainfoobserveronrecvmediaextrainfo)(const char* uid, const char* pData, int dataLen) = 0 |
| virtual bool | [onRecvMixAudioInfo](#ithundermediaextrainfoobserveronrecvmixaudioinfo)(const char* uid, [MixAudioInfoList](#mixaudioinfolist)& infos) = 0 |
| virtual bool | [onRecvMixVideoInfo](#ithundermediaextrainfoobserveronrecvmixvideoinfo)(const char* uid, [MixVideoInfoList](#mixvideoinfolist)& infos) = 0 |

## Detailed callback description

### IThunderEventHandler

#### IThunderEventHandler::onJoinRoomSuccess

```c++
virtual void Thunder::IThunderEventHandler::onJoinRoomSuccess(const char* roomName, const char* uid, int elapsed);
```

Occurs when the local user enters a room successfully.

> **Note:**
>
> If you receive this callback after calling IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) means, connection to the server succeeds. In this case, you can call interfaces that are allowed only after entering room successfully.

##### Parameter[](#onjoinroomsuccess)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| roomName | OUT | Room name |
| uid | OUT | User ID |
| elapsed | OUT | Time (ms) consumed from calling IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) to API event callback |

--------------------------

#### IThunderEventHandler::onLeaveRoom

```c++
virtual void Thunder::IThunderEventHandler::onLeaveRoom();
```

Callback on leaving room.

> **Note:**
>
> This callback is received if you leave the room by calling [leaveRoom](function.md#ithunderengineleaveroom).

--------------------------

#### IThunderEventHandler::onPlayVolumeIndication

```c++
virtual void Thunder::IThunderEventHandler::onPlayVolumeIndication(const AudioVolumeInfo* speakers, int speakerCount, int totalVolume);
```

Reporting who is speaking and the speakers' volume.

> **Note:**
>
> After this method is called, an [onPlayVolumeIndication](function.md#ithunderenginesetaudiovolumeindication) notification will be received once anyone speaks in the room.

##### Parameter[](#onplayvolumeindication)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| speakers | OUT | Speaker (array). For details, see [AudioVolumeInfo.](#audiovolumeinfo) |
| speakerCount | OUT | Number of speakers |
| totalVolume | OUT | Total volume (after audio mixing) [0-100] |

--------------------------

#### IThunderEventHandler::onInputVolume

```c++
virtual void Thunder::IThunderEventHandler::onInputVolume(unsigned volume);
```

Reports the input volume for audition.

> **Note:**
>
> This callback is received if [startInputDeviceTest](function.md#iaudiodevicemanagerstartinputdevicetest) is called. The call frequency is 120 ms.

##### Parameter[](#oninputvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-100] |

--------------------------

#### IThunderEventHandler::onOutputVolume

```c++
virtual void Thunder::IThunderEventHandler::onOutputVolume(unsigned volume);
```

Reports the input volume for audition.

> **Note:**
>
> This callback is received if [startOutputDeviceTest](function.md#iaudiodevicemanagerstartoutputdevicetest)is called. The call frequency is 150 ms.

##### Parameter[](#onoutputvolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume value [0-100] |

--------------------------

#### IThunderEventHandler::onBizAuthResult

```c++
virtual void Thunder::IThunderEventHandler::onBizAuthResult(bool bPublish, AUTH_RESULT result);
```

Callback on service authentication results.

> **Note:**
>
> - For returned results to be authenticated by the service, Aivacom will transfer the authentication request to the service authentication server and pass through and return authentication results.
> - This callback is received if service authentication is mandatory for services and there is media stream in the uplink.

##### Parameter[](#onbizauthresult)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| bPublish | OUT | true: publishing authentication false: playing authentication |
| result | OUT | Authentication results 0: pass<br> Other values: fail. |

--------------------------

#### IThunderEventHandler::onSdkAuthResult

```c++
virtual void Thunder::IThunderEventHandler::onSdkAuthResult(AUTH_RESULT result);
```

Callback of SDK authentication result.

> **Note:**
>
> - Reports authentication result if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and there is uplink and downlink media data.

##### Parameter[](#onsdkauthresult)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| result | OUT | For details about the authentication result, see [AUTH_RESULT.](#auth-result) |

--------------------------

#### IThunderEventHandler::onTokenWillExpire

```c++
virtual void Thunder::IThunderEventHandler::onTokenWillExpire(const char* token);
```

This callback is received if the user’s token is to expire.

##### Parameter[](#ontokenwillexpire)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| token | OUT | token expired |

--------------------------

#### IThunderEventHandler::onTokenRequest

```c++
virtual void Thunder::IThunderEventHandler::onTokenRequest();
```

This callback is received if the user’s token has expired.

--------------------------

#### IThunderEventHandler::onUserBanned

```c++
virtual void Thunder::IThunderEventHandler::onUserBanned(bool status);
```

This callback is received if the user’s banning status has changed.

##### Parameter[](#onuserbanned)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| status | OUT | true: banned; false: unbanned<br> |

--------------------------

#### IThunderEventHandler::onUserJoined

```c++
virtual void Thunder::IThunderEventHandler::onUserJoined(const char* uid, int elapsed);
```

This callback is received if a user joins the current room.

**Note:**

> - This callback is valid only in audio-only mode and will be received when other users enter the room where the local user has entered.

##### Parameter[](#onuserjoined)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User ID |
| elapsed | OUT | Delay from calling [joinRoom](function.md#ithunderenginejoinroom) to receiving the callback (ms) |

--------------------------

#### IThunderEventHandler::onUserOffline

```c++
virtual void Thunder::IThunderEventHandler::onUserOffline(const char* uid, USER_OFFLINE_REASON_TYPE reason);
```

Callback when the user leaves the current room.

**Note:**

> - This callback is valid only in audio-only mode and is returned when other users leave the room where the local user has entered.

##### Parameter[](#onuseroffline)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User ID |
| reason | OUT | Causes for going offline. For details, see [USER_OFFLINE_REASON_TYPE.](#user-offline-reason-type) |

--------------------------

#### IThunderEventHandler::onNetworkQuality

```c++
virtual void Thunder::IThunderEventHandler::onNetworkQuality(const char* uid, NetworkQuality txQuality, NetworkQuality rxQuality);
```

Reporting user network uplink/downlink quality.

##### Parameter[](#onnetworkquality)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User ID |
| txQuality | OUT | Uplink network quality of this user. For details, see [NetworkQuality.](#networkquality) |
| rxQuality | OUT | Downlink network quality of this user. For details, see [NetworkQuality.](#networkquality) |

--------------------------

#### IThunderEventHandler::onFirstLocalVideoFrameSent

```c++
virtual void Thunder::IThunderEventHandler::onFirstLocalVideoFrameSent(int elapsed);
```

Callback on first local video frame sent successfully. This callback is received if the user succeeds in publishing video streams.

##### Parameter[](#onfirstlocalvideoframesent)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| elapsed | OUT | Time (ms) consumed from calling IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) to event occurrence |

--------------------------

#### IThunderEventHandler::onFirstLocalAudioFrameSent

```c++
virtual void Thunder::IThunderEventHandler::onFirstLocalAudioFrameSent(int elapsed);
```

Callback on first local audio frame sent successfully. This callback is received if the user succeeds in publishing audio streams.

##### Parameter[](#onfirstlocalaudioframesent)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| elapsed | OUT | Time (ms) consumed from calling IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) to event occurrence |

--------------------------

#### IThunderEventHandler::onRemoteAudioStopped

```c++
virtual void Thunder::IThunderEventHandler::onRemoteAudioStopped(const char* uid, bool stopped);
```

Callback on enabling/disabling remote user’s audio stream. This callback is received if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and status of existing and subsequent audio streams in the room changes.

##### Parameter[](#onremoteaudiostopped)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Remote user Id |
| mute | OUT | true: Audio streams disabled; <br>false: Audio streams enabled |

--------------------------

#### IThunderEventHandler::onConnectionStatus

```c++
virtual void Thunder::IThunderEventHandler::onConnectionStatus(ThunderConnectionStatus status);
```

Reporting status of connection with server network. This callback is received if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and SDK connection with server network changes.

##### Parameter[](#onconnectionstatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| status | OUT | Network connection status. For details, see [ThunderConnectionStatus.](#thunderconnectionstatus) |

--------------------------

#### IThunderEventHandler::onConnectionLost

```c++
virtual void Thunder::IThunderEventHandler::onConnectionLost();
```

Callback on disconnection with server network. This callback is received if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and SDK connection with server network is interrupted.

--------------------------

#### IThunderEventHandler::onRemoteVideoStopped

```c++
virtual void Thunder::IThunderEventHandler::onRemoteVideoStopped(const char* uid, bool stopped);
```

Callback on stopping/starting remote user video streaming. This callback is received if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and status of existing and subsequent video streams in the room change.

##### Parameter[](#onremotevideostopped)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Remote user Id |
| mute | OUT | true: Video streams disabled; false: Video streams enabled<br> |

--------------------------

#### IThunderEventHandler::onVideoSizeChanged

```c++
virtual void Thunder::IThunderEventHandler::onVideoSizeChanged(const char* uid, int width, int height, int rotation);
```

Callback on change in local or remote video resolution. This callback is received if IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) is called and video resolution changes.

##### Parameter[](#onvideosizechanged)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| width | OUT | Width |
| height | OUT | High |
| rotation | OUT | Reserved, not implemented |

--------------------------

#### IThunderEventHandler::onRemoteVideoPlay

```c++
virtual void Thunder::IThunderEventHandler::onRemoteVideoPlay(const char* uid, int width, int height, int elapsed);
```

Callback on displayed first remote video frame. Used to calculate the video speed. This callback is received after [setRemoteVideoCanvas](function.md#ithunderenginesetremotevideocanvas) is called and video streams are received and displayed in the window.

##### Parameter[](#onremotevideoplay)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| width | OUT | Width |
| height | OUT | High |
| elapsed | OUT | Time (ms) consumed from calling IThunderEngine::[joinRoom](function.md#ithunderenginejoinroom) to event callback |

--------------------------

#### IThunderEventHandler::onNetworkTypeChanged

```c++
virtual void Thunder::IThunderEventHandler::onNetworkTypeChanged(ThunderNetworkType type);
```

Callback on network status change. This callback is received if initialization ([initialize](function.md#ithunderengineinitialize)) is complete and network type changes.

##### Parameter[](#onnetworktypechanged)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| type | OUT | Network connection type. For details, see [ThunderNetworkType.](#thundernetworktype) |

--------------------------

#### IThunderEventHandler::onAudioCaptureStatus

```c++
virtual void Thunder::IThunderEventHandler::onAudioCaptureStatus(ThunderAudioDeviceStatus type);
```

Callback on changes in audio device capture status. Enable audio capture. When device for audio capture changes in status, this notification will be received.

##### Parameter[](#onaudiocapturestatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| type | OUT | Collection status of the audio device. For details, see [ThunderAudioDeviceStatus.](#thunderaudiodevicestatus) |

--------------------------

#### IThunderEventHandler::onPublishStreamToCDNStatus

```c++
virtual void Thunder::IThunderEventHandler::onPublishStreamToCDNStatus(const char* url, ThunderPublishCDNErrorCode errorCode);
```

Callback on CDN stream publishing result. This callback is received if the user has called [addPublishOriginStreamUrl](function.md#ithunderengineaddpublishoriginstreamurl) or [addPublishTranscodingStreamUrl](function.md#ithunderengineaddpublishtranscodingstreamurl) for stream publishing and the stream publishing status changes.

##### Parameter[](#onpublishstreamtocdnstatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| url | OUT | URL for stream publishing |
| errorCode | OUT | Error code for stream publishing. For details, see [ThunderPublishCDNErrorCode.](#thunderpublishcdnerrorcode) |

--------------------------

#### IThunderEventHandler::onRoomStats

```c++
virtual void Thunder::IThunderEventHandler::onRoomStats(RoomStats stats);
```

Callback on uplink/downlink traffic (periodic callback at an interval of 2 seconds). This callback is received when the user enters a channel.

##### Parameter[](#onroomstats)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| stats | OUT | Specific status. For details, see [RoomStats.](#roomstats) |

--------------------------

#### IThunderEventHandler::onRecvUserAppMsgData

```c++
virtual void Thunder::IThunderEventHandler::onRecvUserAppMsgData(const char* uid, const char* msgData);
```

Callback custom broadcast message of service This callback is received by users entering the channel if the anchor sends data through [sendUserAppMsgData](function.md#ithunderenginesenduserappmsgdata).

##### Parameter[](#onrecvuserappmsgdata)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | uid of the user that sends the message |
| msgData | OUT | Received customized broadcast message |

--------------------------

#### IThunderEventHandler::onSendAppMsgDataFailedStatus

```c++
virtual void Thunder::IThunderEventHandler::onSendAppMsgDataFailedStatus(ThunderSendAppMsgDataFailedStatus status);
```

This callback is received if the anchor fails to send data by calling [sendUserAppMsgData](function.md#ithunderenginesenduserappmsgdata).

##### Parameter[](#onsendappmsgdatafailedstatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| status | OUT | Causes for failure in sending customized broadcast messages. For details, see [ThunderSendAppMsgDataFailedStatus.](#thundersendappmsgdatafailedstatus) |

--------------------------

#### IThunderEventHandler::onVideoCaptureStatus

```c++
virtual void Thunder::IThunderEventHandler::onVideoCaptureStatus(ThunderCaptureStatus status);
```

Callback on changes in camera capture status. This callback is received when camera collection starts and the collection status of the camera changes.

##### Parameter[](#onvideocapturestatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| status | OUT | Camera collection status. For details, see [ThunderCaptureStatus.](#thundercapturestatus) |

--------------------------

#### IThunderEventHandler::onLocalVideoStats

```c++
virtual void Thunder::IThunderEventHandler::onLocalVideoStats(const LocalVideoStats stats);
```

The statistics of sending of video stream by local device is described during this callback. Callback time: 1. immediate callback when the publishing interface is called; 2. immediate callback on bracket change during the publishing; and 3. periodical callback at an interval of 2s.

##### Parameter[](#onlocalvideostats)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| stats | OUT | Statistical data on local video. For details, see [LocalVideoStats.](#localvideostats) |

--------------------------

#### IThunderEventHandler::onLocalAudioStats

```c++
virtual void Thunder::IThunderEventHandler::onLocalAudioStats(const LocalAudioStats stats);
```

The statistics of sending of video stream by local device is described during this callback. Callback time: periodical callback at an interval of 2s.

##### Parameter[](#onlocalaudiostats)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| stats | OUT | Statistical data on local audio. For details, see [LocalAudioStats.](#localaudiostats) |

--------------------------

#### IThunderEventHandler::onRemoteVideoStatsOfUid

```c++
virtual void Thunder::IThunderEventHandler::onRemoteVideoStatsOfUid(const char* uid, const RemoteVideoStats stats);
```

The end-to-end video stream status in calling of remote users is described during this callback, which is triggered once 2s for each remote user/anchor. In case multiple users/anchors exist remotely at the same time, this callback will be triggered multiple times every 2 seconds.

##### Parameter[](#onremotevideostatsofuid)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Id of remote user/anchor |
| stats | OUT | Statistical data on remote video. For details, see [RemoteVideoStats.](#remotevideostats) |

--------------------------

#### IThunderEventHandler::onRemoteAudioStatsOfUid

```c++
virtual void Thunder::IThunderEventHandler::onRemoteAudioStatsOfUid(const char* uid, const RemoteAudioStats stats);
```

This callback describes end-to-end video streaming status of remote user during the call. It is triggered every 2s for each remote user/anchor. In case multiple users/anchors exist remotely at the same time, this callback will be triggered multiple times every 2 seconds.

##### Parameter[](#onremoteaudiostatsofuid)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Id of remote user/anchor |
| stats | OUT | Statistical data on remote audio. For details, see [RemoteAudioStats.](#remoteaudiostats) |

--------------------------

### IAudioFrameObserver

#### IAudioFrameObserver::onRecordAudioFrame

```c++
virtual void Thunder::IAudioFrameObserver::onRecordAudioFrame(AudioFrame& audioFrame);
```

Callback on raw audio capture data.

- The user has called the [registerAudioFrameObserver](function.md#ithunderengineregisteraudioframeobserver) interface and has registered IAudioFrameObserver.
- Meanwhile, when the user starts capture, this callback will be received.

##### Parameter[](#onrecordaudioframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

#### IAudioFrameObserver::onPlaybackAudioFrame

```c++
virtual void Thunder::IAudioFrameObserver::onPlaybackAudioFrame(AudioFrame& audioFrame);
```

Callback on raw audio play data.

- The user has called the [registerAudioFrameObserver](function.md#ithunderengineregisteraudioframeobserver) interface and has registered IAudioFrameObserver.
- Meanwhile, when there’s audio data being played, this callback will be received.

##### Parameter[](#onplaybackaudioframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

#### IAudioFrameObserver::onPlaybackAudioFrameBeforeMixing

```c++
virtual void Thunder::IAudioFrameObserver::onPlaybackAudioFrameBeforeMixing(char* uid, AudioFrame& audioFrame);
```

Callback of original data decoded by remote user can differentiate users through different uids.

- The user has called the [registerAudioFrameObserver](function.md#ithunderengineregisteraudioframeobserver) interface and has registered IAudioFrameObserver.
- Meanwhile, when there’s remote audio data being played, this callback will be received.

##### Parameter[](#onplaybackaudioframebeforemixing)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | Remote user uid |
| audioFrame | OUT | For original audio data, see [AudioFrame for details](#audioframe) |

--------------------------

### IThunderAudioPlayerNotify

#### IThunderAudioPlayerNotify::onAudioFileVolume

```c++
virtual void Thunder::IThunderAudioPlayerNotify::onAudioFileVolume(unsigned int volume, unsigned int currentMs, unsigned int totalMs);
```

Callback on progress information of audio player.

- Call the IThunderAudioPlayer::[SetFilePlayerNotify](function.md#ithunderaudioplayersetfileplayernotify) interface with IThunderAudioPlayerNotify set as the monitoring object.

##### Parameter[](#onaudiofilevolume)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| volume | OUT | Volume range: [0-100] |
| currentMs | OUT | Current play progress, unit: ms |
| totalMs | OUT | Total duration of the audio file, unit: ms |

--------------------------

#### IThunderAudioPlayerNotify::onAudioFilePlayEnd

```c++
virtual void Thunder::IThunderAudioPlayerNotify::onAudioFilePlayEnd();
```

The audio player plays and then calls back.

- Call the IThunderAudioPlayer::[SetFilePlayerNotify](function.md#ithunderaudioplayersetfileplayernotify) interface with IThunderAudioPlayerNotify set as the monitoring object.

--------------------------

### IVideoFrameObserver

#### IVideoFrameObserver::onPreviewVideoFrame

```c++
virtual bool Thunder::IVideoFrameObserver::onPreviewVideoFrame(VideoFrame& videoFrame);
```

The local video preview data is called back. The current data format is YUV420.

- Call IThunderEngine::[registerVideoFrameObserver](function.md#ithunderengineregistervideoframeobserver) to proceed with registration.

##### Parameter[](#onpreviewvideoframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| videoFrame | OUT | Local preview video data. For details, see [VideoFrame.](#videoframe) |

--------------------------

#### IVideoFrameObserver::onRenderVideoFrame

```c++
virtual bool Thunder::IVideoFrameObserver::onRenderVideoFrame(const char* uid, VideoFrame& videoFrame);
```

The rendering video data of other users is called back. The data format is YUV420.

- Call IThunderEngine::[registerVideoFrameObserver](function.md#ithunderengineregistervideoframeobserver) to proceed with registration.

##### Parameter[](#onrendervideoframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| videoFrame | OUT | User rending video data. For details, see [VideoFrame.](#videoframe) |

--------------------------

### IVideoCaptureObserver

#### IVideoCaptureObserver::onCaptureVideoFrame

```c++
virtual bool Thunder::IVideoCaptureObserver::onCaptureVideoFrame(VideoFrame& videoFrame);
```

The local video capture data is called back. The current data format is BGRA.

- Call IThunderEngine::[registerVideoCaptureObserver](function.md#ithunderengineregistervideocaptureobserver) to proceed with registration.

##### Parameter[](#oncapturevideoframe)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| videoFrame | OUT | Local collection video data. For details, see [VideoFrame.](#videoframe) |

--------------------------

### IThunderMediaExtraInfoObserver

#### IThunderMediaExtraInfoObserver::onSendMediaExtraInfoFailedStatus

```c++
virtual void Thunder::IThunderMediaExtraInfoObserver::onSendMediaExtraInfoFailedStatus(int status);
```

Callback on failure in sending media extra information.

- Call IThunderEngine::[registerMediaExtraInfoObserver](function.md#ithunderengineregistermediaextrainfoobserver) to proceed with registration.

##### Parameter[](#onsendmediaextrainfofailedstatus)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| status | OUT | Error code for failure. See ThunderSendMediaExtraInfoFailedStatus for details. |

--------------------------

#### IThunderMediaExtraInfoObserver::onRecvMediaExtraInfo

```c++
virtual void Thunder::IThunderMediaExtraInfoObserver::onRecvMediaExtraInfo(const char* uid, const char* pData, int dataLen);
```

Callback on media extra information received.

- Call IThunderEngine::[registerMediaExtraInfoObserver](function.md#ithunderengineregistermediaextrainfoobserver) to proceed with registration.

##### Parameter[](#onrecvmediaextrainfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| pData | OUT | Media extra information |
| dataLen | OUT | Length of media extra information |

--------------------------

#### IThunderMediaExtraInfoObserver::onRecvMixAudioInfo

```c++
virtual bool Thunder::IThunderMediaExtraInfoObserver::onRecvMixAudioInfo(const char* uid, MixAudioInfoList& infos);
```

Callback on extra information of mixed audio streams received.

- Call IThunderEngine::[registerMediaExtraInfoObserver](function.md#ithunderengineregistermediaextrainfoobserver) to proceed with registration.

##### Parameter[](#onrecvmixaudioinfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| infos | OUT | List of information about mixed audio stream |

--------------------------

#### IThunderMediaExtraInfoObserver::onRecvMixVideoInfo

```c++
virtual bool Thunder::IThunderMediaExtraInfoObserver::onRecvMixVideoInfo(const char* uid, MixVideoInfoList& infos);
```

Callback on extra information of mixed video streams received.

- Call IThunderEngine::[registerMediaExtraInfoObserver](function.md#ithunderengineregistermediaextrainfoobserver) to proceed with registration.

##### Parameter[](#onrecvmixvideoinfo)

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uid | OUT | User id |
| infos | OUT | List of information about mixed video streams |

--------------------------

## Enumerated values & structure definition

#### AudioVolumeInfo

```c++
#define MAX_THUNDER_UID_LEN 65 // UID length

struct AudioVolumeInfo
{
  char uid[MAX_THUNDER_UID_LEN]; // User id
  int volume; // Volume
};
```

Information about playing volume

--------------------------

#### AUTH_RESULT

```c++
enum Thunder::AUTH_RESULT
```

Authentication result

| Enumerated values | Meaning |
| :--- | :--- |
| AUTHRES_SUCCUSS(0) | Authentication succeeded |
| AUTHRES_ERR_SERVER_INTERNAL(10000) | Server internal error, try again |
| AUTHRES_ERR_NO_TOKEN(10001) | token not carried. [updateToken needs to be called.](#updatetoken) |
| AUTHRES_ERR_TOKEN_ERR(10002) | Token authentication failed (incorrect digital signature), which may be caused by incorrect appSecret |
| AUTHRES_ERR_APPID(10003) | appid in token is inconsistent with appid when execute authentication |
| AUTHRES_ERR_UID(10004) | uid in token is inconsistent with uid when execute authentication |
| AUTHRES_ERR_TOKEN_EXPIRE(10005) | token has expired |
| AUTHRES_ERR_NO_APP(10006) | App does not exist, which is not registered in the management background |
| AUTHRES_ERR_TOKEN_WILL_EXPIRE(10007) | token is about to expire. Callback is returned 30s in advance. |
| AUTHRES_ERR_NO_BAND(10008) | The user is baned |

--------------------------

#### USER_OFFLINE_REASON_TYPE

```c++
enum Thunder::USER_OFFLINE_REASON_TYPE
```

Causes for user going offline

| Enumerated values | Meaning |
| :--- | :--- |
| USER_OFFLINE_QUIT(1) | The user is offline actively |
| USER_OFFLINE_DROPPED(2) | The packet could not be received for long time, lost connection due to timeout. Note: Because SDK uses unreliable channel, the counterpart may leave our side actively. So it is misjudged as timeout offline |
| USER_OFFLINE_BECOME_AUDIENCE(3) | User status is switched from anchor to audience (live mode) |

--------------------------

#### NetworkQuality

```c++
enum Thunder::NetworkQuality
```

Network quality

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_QUALITY_UNKNOWN(0) | Unknown quality |
| THUNDER_QUALITY_EXCELLENT(1) | Excellent network quality |
| THUNDER_QUALITY_GOOD(2) | Good network quality |
| THUNDER_QUALITY_POOR(3) | The network quality is poor, but the communication is not affected even the user can feel its defects. |
| THUNDER_QUALITY_BAD(4) | The network quality is bad, and the communication can be barely made but is not smooth |
| THUNDER_QUALITY_VBAD(5) | The network quality is very bad, the communication cannot be made basically |
| THUNDER_QUALITY_DOWN(6) | Network disconnected and communication failed. |

--------------------------

#### ThunderConnectionStatus

```c++
enum Thunder::ThunderConnectionStatus
```

Server connection status

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_CONNECTION_STATUS_CONNECTING(0) | Connecting |
| THUNDER_CONNECTION_STATUS_CONNECTED(1) | Connected |
| THUNDER_CONNECTION_STATUS_DISCONNECTED(2) | Disconnected |

--------------------------

#### ThunderNetworkType

```c++
enum Thunder::ThunderConnectionStatus
```

Network type

| Enumerated values | Meaning |
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

#### ThunderAudioDeviceStatus

```c++
enum Thunder::ThunderConnectionStatus
```

Audio device status

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_SUCCESS(0) | Callback on successful initialization of audio capture device |
| THUNDER_AUDIO_DEVICE_STATUS_INIT_CAPTURE_ERROR_OR_NO_PERMISSION(1) | Callback on initialization failure of audio capture. It may be caused by no permission |
| THUNDER_AUDIO_DEVICE_STATUS_RELEASE_CAPTURE_SUCCESS(2) | Callback on successful release of audio capture device |

--------------------------

#### ThunderPublishCDNErrorCode

```c++
enum Thunder::ThunderPublishCDNErrorCode
```

Error codes for CDN stream publishing

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_PUBLISH_CDN_ERR_SUCCESS(0) | Stream publishing succeeded |
| THUNDER_PUBLISH_CDN_ERR_TOCDN_FAILED(1) | Publishing stream to external server (CDN) is failed. 1. Check whether url is correct. 2. Check whether the token in the URL is valid (generally, token is required during cdn stream publishing and can be ignored if it doe not exist). |
| THUNDER_PUBLISH_CDN_ERR_THUNDERSERVER_FAILED(2) | Publish the stream to thunder internal server is failed. 1. Check the anchor uplink network. 2. Contact us to locate internal transmission faults. |
| THUNDER_PUBLISH_CDN_ERR_THUNDERSERVER_STOP(3) | Stop stream publishing |

--------------------------

#### RoomStats

```c++
struct Thunder::RoomStats
{
  int txBitrate; // Chain sending bit rate (unit: bps)
  int rxBitrate; // Chain receiving bit rate (unit: bps)
  int txAudioBitrate; // Audio packet sending bit rate (unit: bps)
  int rxAudioBitrate; // Audio packet receiving bit rate (unit: bps)
  int txVideoBitrate; // Video packet sending bit rate (unit: bps)
  int rxVideoBitrate; // Video packet receiving bit rate (unit: bps)
};
```

Information about uplink and downlink traffic in the room

--------------------------

#### ThunderSendAppMsgDataFailedStatus

```c++
enum Thunder::ThunderSendAppMsgDataFailedStatus
```

Causes for failure in sending user-defined messages

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SEND_APP_DATA_HIGHT_FREQUENCY(1) | Excessively high sending frequency. Fewer than twice each second is recommended. |
| THUNDER_SEND_APP_DATA_LARGE_MSG_DATA(2) | Excessively large size of sent data each time. It is recommended that data sent each time does not exceed 200 bytes. |
| THUNDER_SEND_APP_DATA_NO_PUBLISH_SUCCESS(3) | Publishing failed |

--------------------------

#### ThunderCaptureStatus

```c++
enum Thunder::ThunderCaptureStatus
```

Camera collection status

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_VIDEO_CAPTURE_STATUS_SUCCESS(0) | Succeeded |
| THUNDER_VIDEO_CAPTURE_STATUS_AUTHORIZED(1) | Permission not granted to users yet (not supported on PCs temporarily) |
| THUNDER_VIDEO_CAPTURE_STATUS_NOT_DETERMINED(2) | Permission not granted yet (not supported on PCs temporarily) |
| THUNDER_VIDEO_CAPTURE_STATUS_RESTRICTED(3) | Occupied |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(4) | No permission |
| THUNDER_VIDEO_CAPTURE_STATUS_DENIED(5) | Close |
| THUNDER_VIDEO_CAPTURE_STATUS_LOST(6) | The device is removed. |
| THUNDER_VIDEO_CAPTURE_STATUS_RESUME(7) | The device is removed and inserted again. |

--------------------------

#### QUALITY_ADAPT_INDICATION

```c++
enum Thunder::QUALITY_ADAPT_INDICATION
```

Adaption of video quality

| Enumerated values | Meaning |
| :--- | :--- |
| ADAPT_NONE(0) | The quality of local video is constant |
| ADAPT_UP_BANDWIDTH(1) | The quality of local video has been improved because of higher network bandwidth |
| ADAPT_DOWN_BANDWIDTH(2) | The quality of local video becomes worse because of lower network bandwidth |

--------------------------

#### VIDEO_CODEC_TYPE

```c++
enum Thunder::QUALITY_ADAPT_INDICATION
```

Video encoding type

| Enumerated values | Meaning |
| :--- | :--- |
| VIDEO_CODEC_UNKNOW(0) | Unknown type |
| VIDEO_CODEC_VP8(1) | Standard VP8 |
| VIDEO_CODEC_H264(2) | Standard H264 |
| VIDEO_CODEC_H265(3) | Standard H265 |
| VIDEO_CODEC_EVP(4) | Enhanced VP8 |
| VIDEO_CODEC_E264(5) | Enhanced H264 |

--------------------------

#### LocalVideoStats

```c++
struct Thunder::LocalVideoStats
{
  int sendBitrate;// Actual sending bit rate (unit: Kbps), with the exception of sending bit rate of reloaded videos after packet loss
  int sendFrameRate;// Actual sending frame rate (unit: fps), with the exception of sending frame rate of reloaded videos after packet loss
  int encoderOutputFrameRate;// Output frame rate of local encoder (unit: fps)
  int rendererOutputFrameRate;// Output frame rate of local preview (unit: fps)
  int targetBitrate;// Target encoding bit rate of current encoder (unit: Kbps). This bit rate is a value estimated by this SDK in accordance with current network status.
  int targetFrameRate;// Target encoding frame rate of current encoder (unit: fps). This frame rate is a value estimated by this SDK in accordance with current network status.
  QUALITY_ADAPT_INDICATION qualityAdaptIndication;//Quality adaptability of local videos since last statistics (based on target frame rate and target bit rate)
  int encodedBitrate;//Bit rate of video encoding (Kbps). This parameter includes no encoding bit rate of reloaded videos after packet loss.
  int encodedFrameWidth;// Encoded video width (px)
  int encodedFrameHeight;// Encoded video height (px)
  int encodedFrameCount;// Number of frames sent by video, an accumulated value
  VIDEO_CODEC_TYPE codecType;// Encoding type of videos
  int configBitRate;//Configured bit rate (kbps)
  int configFrameRate;// Configured frame rate
  int configWidth;// Configured encoding width
  int configHeight;// Configured encoding height
};
```

Statistics on video streams sent from the local device, among which:

- Video quality adaption: See [QUALITY_ADAPT_INDICATION.](#quality-adapt-indication)
- Video encoding type: See [VIDEO_CODEC_TYPE.](#video-codec-type)

--------------------------

#### LocalAudioStats

```c++
struct LocalAudioStats
{
  int numChannels;    // Number of channels
  int sendSampleRate; // Sampling rate sent (unit: Hz)
  int sendBitrate;    // Average value of bit rate of sent data (unit: Kbps)
};
```

Statistics on audio streams sent from the local device

--------------------------

#### REMOTE_VIDEO_STREAM_TYPE

```c++
enum Thunder::REMOTE_VIDEO_STREAM_TYPE
```

High/Low stream type

| Enumerated values | Meaning |
| :--- | :--- |
| REMOTE_VIDEO_STREAM_HIGH(0) | High stream |
| REMOTE_VIDEO_STREAM_LOW(1) | Low stream |

--------------------------

#### RemoteVideoStats

```c++
struct RemoteVideoStats
{
  int delay; // Delay from publishing remote video stream to playback
  int width; // Width of remote video stream
  int height; // Height of remote video stream
  int receivedBitrate; // Receiving bit rate (unit: Kbps)
  int decoderOutputFrameRate; // Output frame rate of remote video decoder (unit: fps)
  int rendererOutputFrameRate; // Output frame rate of remote video renderer (unit: fps)
  int packetLossRate; // Packet loss rate (%) of remote video after network confrontation
  REMOTE_VIDEO_STREAM_TYPE rxStreamType; // Types of video stream, including large stream and small stream
  int totalFrozenTime; // The accumulated time (ms) from the time when a remote user joins a channel to the time of video freezing
  int frozenRate; // The percentage (%) of the accumulated time (from the time when a remote user joins a channel to the time of video freezing) accounting for total effective time of videos
};
```

Status of end-to-end video streams of remote users in a call. Among which:

- Video stream type: See [REMOTE_VIDEO_STREAM_TYPE.](#remote-video-stream-type)

--------------------------

#### RemoteAudioStats

```c++
struct RemoteAudioStats
{
    int quality;// Quality of audio streams sent by remote users. 0: Unknown; 1: Excellent; 2: Good; 3: Poor, flawed but does not affect communication; 4: Bad, communication can be made but not smoothly; 5: Very Bad, communication can barely be made; 6: Disconnected, communication can not be made at all 
    int networkTransportDelay;// Network delay from an audio sending end to an audio receiving end
    int jitterBufferDelay;// Delay from a receiving end to network jitter buffer
    int frameLossRate;// Frame loss rate (%) of remote audio streams
    int numChannels;// Number of channels
    int receivedSampleRate;// Sampling rate (Hz) of remote audios
    int receivedBitrate;// Average bit rate of remote audios within a statistical period
    int totalFrozenTime;// The accumulated time (ms) from the time when a remote user joins a channel to the time of audio freezing
    int frozenRate;// The percentage (%) of the accumulated time (from the time when a remote user joins a channel to the time of audio freezing) accounting for total effective time of audios
};
```

Status of end-to-end audio streams of remote users in a call.

--------------------------

#### AUDIO_FRAME_TYPE

```c++
enum IAudioFrameObserver::AUDIO_FRAME_TYPE
```

Audio frame type

| Enumerated values | Meaning |
| :--- | :--- |
| FRAME_TYPE_PCM16(0) | PCM 16bit little endian |

--------------------------

#### AudioFrame

```c++
struct IAudioFrameObserver::AudioFrame
{
  AUDIO_FRAME_TYPE type;
  int samples; // Sample quantity of the frame
  int bytesPerSample; // Bytes per sample: PCM (16 digits) contains two types
  int channels; // Number of channels (crossed data for stereo); 1: single track, 2: dual track
  int samplesPerSec; // Sampling rate
  void* buffer; // data buffer
  long long renderTimeMs; // Not used momentarily
  int avsync_type; // Not used momentarily
};
```

Detailed information about audio data. For details about audio frame type, see [AUDIO_FRAME_TYPE.](#audio-frame-type)

--------------------------

#### VIDEO_FRAME_TYPE

```c++
enum Thunder::VIDEO_FRAME_TYPE
```

Video frame type

| Enumerated values | Meaning |
| :--- | :--- |
| FRAME_TYPE_YUV420(0) | YUV420 |
| FRAME_TYPE_BGRA(1) | BGRA |

--------------------------

#### VideoFrame

```c++
#define MAX_THUNDER_VIDEO_BUFFER_PLANE 8 // Maximum plane number of video frames (I420: 3, RGB: 1)

struct VideoFrame
{
  void* dataPtr[MAX_THUNDER_VIDEO_BUFFER_PLANE]; // Pointer to each plane data in video frame
  int dataLength[MAX_THUNDER_VIDEO_BUFFER_PLANE]; // Length of each plane data in video frame
  int dataStride[MAX_THUNDER_VIDEO_BUFFER_PLANE]; // Step size of each plane data in video frame
  int width; // Width of video frame
  int height; // Width and height of video frame
  VIDEO_FRAME_TYPE type; // Type of video frame
  int rotation; // Rotation angle
  __int64 timeStamp; // Presentation timestamp
};
```

Detailed information about video data. For details about video frame type, see [VIDEO_FRAME_TYPE.](#video-frame-type)

--------------------------

#### ThunderSendMediaExtraInfoFailedStatus

```c++
enum IThunderMediaExtraInfoObserver::ThunderSendMediaExtraInfoFailedStatus
```

Causes for failure in sending media extra information.

| Enumerated values | Meaning |
| :--- | :--- |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_EMPTY(1) | Extra information is null. |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_DATA_TOO_LARGE(2) | Excessively large size of sent data each time |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_FREQUENCY_TOO_HIGHT(3) | Excessively high sending frequency |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NOT_IN_ANCHOR_SYSTEM(4) | Not an anchor system |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_JOIN_MEDIA(5) | Channel not to be joined |
| THUNDER_SEND_MEDIA_EXTRA_INFO_FAILED_NO_PUBLISH_SUCCESS(6) | Publishing failed |

--------------------------

#### MixAudioInfo

```c++
  struct MixAudioInfo // Information about mixed audio stream
  {
    char uid[MAX_THUNDER_UID_LEN]; // User id
    int volume;    // Volume of mixed audio stream [0,100]
  };
```

Information about mixed audio stream

--------------------------

#### MixAudioInfoList

```c++
  struct MixAudioInfoList // List of information about mixed audio stream
  {
    int count; // Number of lists of information about mixed audio stream
    MixAudioInfo mixAudio[MAX_THUNDER_MIX_AUDIO_COUNT]; // Specific information about mixed audio stream
  };
```

List of information about mixed audio stream

--------------------------

#### MixVideoInfo

```c++
  struct MixVideoInfo
  {
    char uid[MAX_THUNDER_UID_LEN]; // User id
    int width; // Original width of this user's video
    int height; // Original height of this user's video
    int cropX; // X coordinate of the begin point used to crop the original video in video mixing
    int cropY; // Y coordinate of the begin point used to crop the original video in video mixing
    int cropW; // Width of the original video to be cropped in video mixing
    int cropH; // Height of the original video to be cropped in video mixing
    int layoutX; // X coordinate of the begin point of this user's video in video mixing canvas
    int layoutY; // Y coordinate of the begin point of this user's video in video mixing canvas
    int layoutW; // Width of this user's video in video mixing canvas
    int layoutH; // Height of this user's video in video mixing canvas
    int zOrder; // Layer number of this user's video frame in video mixing. The value range is the integer in [0, 100], and the minimum value is 0, indicating that the image in this region is at the lowest level
    float alpha; // Transparency of this user's video frame in video mixing.
                 // The value range is [0.0, 1.0]. 0.0 indicates that the image in this region is completely transparent, while 1.0 indicates completely opaque
  };
```

Information about mixed video streams

--------------------------

#### MixVideoInfoList

```c++
  struct MixVideoInfoList // List of information about mixed video streams
  {
    int count; // Number of lists of information about mixed video stream
    MixVideoInfo mixVideo[MAX_THUNDER_MIX_VIDEO_COUNT]; // Specific information about mixed video stream
  };
```

List of information about mixed video streams

--------------------------
