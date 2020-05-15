# Overview

AIVACOM provides various client SDKs with APIs that can be flexibly combined. SDK-based connection to globally-deployed real-time communication networks guarantees stable and reliable real-time audio/video communication services.

The Aivacom SDK has a code of `Thunderbolt`, and a pure audio SDK for a mobile terminal has a code of `Thunder`.

- [The IThunderEngine](function.md#ithunderengine) interface class provides all functions that can be called by application.
- [The IThunderEventHandler](notification.md#ithundereventhandler) interface class is used to send callbacks to the application.

> Note: Unless otherwise stated, event callbacks in this document are monitored through the [IThunderEventHandler](notification.md#ithundereventhandler) interface.

## Basic Method

| Method | Function |
| :---| :--- |
| [createEngine](function.md#ithunderenginecreateengine) | Create the IThunderEngine instance |
| [initialize](function.md#ithunderengineinitialize) | Initialize the IThunderEngine object |
| [destroyEngine](function.md#ithunderenginedestroyengine) | Destroy the IThunderEngine object |

## Room Management

| Method | Function |
| :---| :--- |
| [setArea](function.md#ithunderenginesetarea) | Set user’s area |
| [setMediaMode](function.md#ithunderenginesetmediamode) | Set media mode |
| [setRoomMode](function.md#ithunderenginesetroommode) | Set room mode |
| [joinRoom](function.md#ithunderenginejoinroom) | Join a room |
| [leaveRoom](function.md#ithunderengineleaveroom) | Leave a room |
| [updateToken](function.md#ithunderengineupdatetoken) | Update Token |

| Callback | Function |
| :---| :--- |
| [onJoinRoomSuccess](notification.md#ithundereventhandleronjoinroomsuccess) | Callback when the local user joins a room |
| [onLeaveRoom](notification.md#ithundereventhandleronleaveroom) | Callback after the local user leaves a room |
| [onSdkAuthResult](notification.md#ithundereventhandleronsdkauthresult) | Callback on SDK authentication result. For authentication details, refer to “User Authentication Description” on official website. |
| [onUserBanned](notification.md#ithundereventhandleronuserbanned) | Callback when a user is banned |
| [onUserJoined](notification.md#ithundereventhandleronuserjoined) | Callback when a remote user joins the current room |
| [onUserOffline](notification.md#ithundereventhandleronuseroffline) | Callback on user leaving a current room |
| [onRoomStats](notification.md#ithundereventhandleronroomstats) | Callback on uplink/downlink traffic (periodic callback at an interval of 2s) |
| [onBizAuthResult](notification.md#ithundereventhandleronbizauthresult) | Callback on service authentication results |
| [onTokenWillExpire](notification.md#ithundereventhandlerontokenwillexpire) | Callback on token to be expired |
| [onTokenRequest](notification.md#ithundereventhandlerontokenrequest) | Callback when token expires |

## Audio Publishing

| Method | Function |
| :---| :--- |
| [setAudioConfig](function.md#ithunderenginesetaudioconfig) | Sets audio parameters and application scenarios. |
| [adjustRecordingSignalVolume](function.md#ithunderengineadjustrecordingsignalvolume) | Set microphone volume |
| [stopLocalAudioStream](function.md#ithunderenginestoplocalaudiostream) | Stop broadcasting/Publishing audio (including starting collection, encoding, and stream publishing) |
| [enableLoopbackRecording](function.md#ithunderengineenableloopbackrecording) | Enable/Disable graphic card capture. |
| [setAudioSourceType](function.md#ithunderenginesetaudiosourcetype) | Set audio publishing type |

| Callback | Function |
| :---| :--- |
| [onFirstLocalAudioFrameSent](notification.md#ithundereventhandleronfirstlocalvideoframesent) | Callback on first local audio frame sent successfully |
| [onLocalAudioStats](notification.md#ithundereventhandleronlocalaudiostats) | Reporting audio streaming sending statistics in every 2s |

## Audio Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteAudioStreams](function.md#ithunderenginestopallremoteaudiostreams) | Stop/Receive all audio streaming data |
| [stopRemoteAudioStream](function.md#ithunderenginestopremoteaudiostream) | Stop/Receive audio streaming data of a specified user |
| [adjustPlaybackSignalVolume](function.md#ithunderengineadjustplaybacksignalvolume) | Set local playing volume |

| Callback | Function |
| :---| :--- |
| [onRemoteAudioStopped](notification.md#ithundereventhandleronremoteaudiostopped) | Callback when a remote user stops broadcasting/publishing audio streams |
| [onRemoteAudioStatsOfUid](notification.md#ithundereventhandleronremoteaudiostatsofuid) | Reporting remote audio streams statistics by user in every 2s |

## Video Publishing

| Method | Function |
| :---| :--- |
| [setVideoEncoderConfig](function.md#ithunderenginesetvideoencoderconfig) | Set video encoding configuration |
| [enableLocalVideoCapture](function.md#ithunderengineenablelocalvideocapture) | Enable/Disable local video capture |
| [setLocalVideoCanvas](function.md#ithunderenginesetlocalvideocanvas) | Set the rendering canvas of a local video |
| [startVideoPreview](function.md#ithunderenginestartvideopreview) | Enable video preview |
| [stopVideoPreview](function.md#ithunderenginestopvideopreview) | Disable video preview |
| [setLocalCanvasScaleMode](function.md#ithunderenginesetlocalcanvasscalemode) | Set a scaling mode of a local canvas |
| [setLocalVideoMirrorMode](function.md#ithunderenginesetlocalvideomirrormode) | Set local video mirror mode |
| [stopLocalVideoStream](function.md#ithunderenginestoplocalvideostream) | Stop/Start the sending of a local video streaming (codes included) |

| Callback | Function |
| :---| :--- |
| [onFirstLocalVideoFrameSent](notification.md#ithundereventhandleronfirstlocalvideoframesent) | Callback when the first video frame is successfully sent |
| [onLocalVideoStats](notification.md#ithundereventhandleronlocalvideostats) | Callback every 2s, reporting video streaming sending statistics |

## Video Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteVideoStreams](function.md#ithunderenginestopallremotevideostreams) | Stop/Receive all video stream data |
| [stopRemoteVideoStream](function.md#ithunderenginestopremotevideostream) | Stop/Receive video stream data of a specified user |
| [setRemoteCanvasScaleMode](function.md#ithunderenginesetremotecanvasscalemode) | Set a scaling mode of a remote canvas |
| [setRemoteVideoCanvas](function.md#ithunderenginesetremotevideocanvas) | Set the rendering view of remote video stream. |

| Callback | Function |
| :---| :--- |
| [onRemoteVideoStopped](notification.md#ithundereventhandleronremotevideostopped) | Callback on stopping/publishing user’s video stream |
| [onRemoteVideoStatsOfUid](notification.md#ithundereventhandleronremotevideostatsofuid) | Reporting remote video streams statistics by user in every 2s |
| [onRemoteVideoPlay](notification.md#ithundereventhandleronremotevideoplay) | Callback on displayed first remote video frame |
| [onVideoSizeChanged](notification.md#ithundereventhandleronvideosizechanged) | Callback on change in local/remote video resolution |

## Network status

| Callback | Function |
| :---| :--- |
| [onNetworkQuality](notification.md#ithundereventhandleronnetworkquality) | Reporting the network statistics in every 2s|
| [onNetworkTypeChanged](notification.md#ithundereventhandleronnetworktypechanged) | Callback on network status change |
| [onConnectionStatus](notification.md#ithundereventhandleronconnectionstatus) | Callback on server network connection status change |
| [onConnectionLost](notification.md#ithundereventhandleronconnectionlost) | Callback on lost network connection with a server |

## Publishing detection

N/A

## Video mixing and stream publishing

| Method | Function |
| :---| :--- |
| [setLiveTranscodingTask](function.md#ithunderenginesetlivetranscodingtask) | Add/update transcoding task |
| [removeLiveTranscodingTask](function.md#ithunderengineremovelivetranscodingtask) | Remove a transcoding task |
| [removePublishTranscodingStreamUrl](function.md#ithunderengineremovepublishtranscodingstreamurl) | Remove a stream publishing address of a transcoding stream |
| [addPublishTranscodingStreamUrl](function.md#ithunderengineaddpublishtranscodingstreamurl) | Add a stream publishing address of a transcoding stream |
| [addPublishOriginStreamUrl](function.md#ithunderengineaddpublishoriginstreamurl) | Add the source stream publishing address |
| [removePublishOriginStreamUrl](function.md#ithunderengineremovepublishoriginstreamurl) | Remove the source stream publishing address |
| [enableMixVideoExtraInfo](function.md#ithunderengineenablemixvideoextrainfo) | Enable video mixing with media extra information |

| Callback | Function |
| :---| :--- |
| [onPublishStreamToCDNStatus](notification.md#ithundereventhandleronpublishstreamtocdnstatus) | Reporting CDN stream publishing result |

## Audio Recording

| Method | Function |
| :---| :--- |
| [startAudioRecording](function.md#ithunderenginestartaudiorecording) | Start audio recording |
| [stopAudioRecording](function.md#ithunderenginestopaudiorecording) | Stop audio recording |

## Cross-room Microphone Connection

| Method | Function |
| :---| :--- |
| [addSubscribe](function.md#ithunderengineaddsubscribe) | Subscribe a stream of the specified user in other rooms |
| [removeSubscribe](function.md#ithunderengineremovesubscribe) | UnSubscribe a stream stream of the specified user in other rooms |

## Camera Management

N/A

## Screen Sharing

| Method | Function |
| :---| :--- |
| [startScreenCaptureForHwnd](function.md#ithunderenginestartscreencaptureforhwnd) | Start screen capturing specific window |
| [startScreenCaptureForScreen](function.md#ithunderenginestartscreencaptureforscreen) | Start screen capturing a specific region on desktop |
| [updateScreenCaptureRect](function.md#ithunderengineupdatescreencapturerect) | Update the region of screen capturing |
| [stopScreenCapture](function.md#ithunderenginestopscreencapture) | Stop screen capturing the desktop or window |
| [pauseScreenCapture](function.md#ithunderenginepausescreencapture) | Pause screen capturing the desktop or window |
| [resumeScreenCapture](function.md#ithunderengineresumescreencapture) | Resume screen capturing the desktop or window |

## Real-time Watermark

| Method | Function |
| :---| :--- |
| [setVideoWatermark](function.md#ithunderenginesetvideowatermark) | Set video watermark |
| [removeVideoWatermarks](function.md#ithunderengineremovevideowatermarks) | Remove video watermark |

## Video Dual Stream

N/A

## Audio Player

| Method | Function |
| :---| :--- |
| [createThunderAudioPlayer](function.md#ithunderenginecreatethunderaudioplayer) | Create audio file player object[IThunderAudioPlayer](function.md#ithunderaudioplayer) |
| [destroyThunderAudioPlayer](function.md#ithunderenginedestroythunderaudioplayer) | Destroy the audio file player object[IThunderAudioPlayer](function.md#ithunderaudioplayer) |

- [Methods in the IThunderAudioPlayer](function.md#ithunderaudioplayer) interface class

| Method | Function |
| :---| :--- |
| [open](function.md#ithunderaudioplayeropen) | Open an file for accompaniment |
| [close](function.md#ithunderaudioplayerclose) | Close an file for accompaniment|
| [play](function.md#ithunderaudioplayerplay) | Start playing the file |
| [Stop](function.md#ithunderaudioplayerstop) | Stop playing the file |
| [pause](function.md#ithunderaudioplayerpause) | Pause playing the file |
| [resume](function.md#ithunderaudioplayerresume) | Resume playing the file |
| [seek](function.md#ithunderaudioplayerseek) | Seek time for playing the file |
| [getTotalPlayTimeMS](function.md#ithunderaudioplayergettotalplaytimems) | Obtain the total duration of the audio file |
| [getCurrentPlayTimeMS](function.md#ithunderaudioplayergetcurrentplaytimems) | Obtain the current playback duration of the audio file |
| [setPlayerLocalVolume](function.md#ithunderaudioplayersetplayerlocalvolume) | Set the local playing volume of the audio file |
| [setPlayerPublishVolume](function.md#ithunderaudioplayersetplayerpublishvolume) | Set the remote playing volume of the audio file |
| [getPlayerLocalVolume](function.md#ithunderaudioplayergetplayerlocalvolume) | Obtain the local playing volume of the audio file |
| [getPlayerPublishVolume](function.md#ithunderaudioplayergetplayerpublishvolume) | Get the remote playing volume of the audio file |
| [setLooping](function.md#ithunderaudioplayersetlooping) | Set a looping count |
| [SetFilePlayerNotify](function.md#ithunderaudioplayersetfileplayernotify) | Callback when the audio file player is configured |

- Callback of monitoring through [IThunderAudioPlayerNotify](notification.md#ithunderaudioplayernotify)

| Callback | Function |
| :---| :--- |
| [onAudioFileVolume](notification.md#ithunderaudioplayernotifyonaudiofilevolume) | Reporting the playing progress |
| [onAudioFilePlayEnd](notification.md#ithunderaudioplayernotifyonaudiofileplayend) | Reporting the playing-end status |


## Voice Change and Reverb

N/A

## Voice Positioning

N/A

## Volume Prompt

| Method | Function |
| :---| :--- |
| [setAudioVolumeIndication](function.md#ithunderenginesetaudiovolumeindication) | Enable/Disable speaker volume callback |

| Callback | Function |
| :---| :--- |
| [onPlayVolumeIndication](notification.md#ithundereventhandleronplayvolumeindication) | Reporting the speakers' volume |

## Voice Routing

N/A

## In-ear Monitor

N/A


## Audio Device Management

Major methods are encapsulated in the [IAudioDeviceManager](function.md#iaudiodevicemanager) interface class and obtain object pointers through the [getAudioDeviceMgr](function.md#ithunderenginegetaudiodevicemgr) interface.

| Method | Function |
| :---| :--- |
| [getAudioDeviceMgr](function.md#ithunderenginegetaudiodevicemgr) | Get pointers of audio/video device management objects |

- [Methods in the IAudioDeviceManager](function.md#iaudiodevicemanager) interface class

| Method | Function |
| :---| :--- |
| [enumInputDevices](function.md#iaudiodevicemanagerenuminputdevices) | Enumerate audio input devices |
| [setInputtingDevice](function.md#iaudiodevicemanagersetinputtingdevice) | Set audio input devices for capturing|
| [getInputtingDevice](function.md#iaudiodevicemanagergetinputtingdevice) | Get the currently selected audio input device |
| [setInputtingVolume](function.md#iaudiodevicemanagersetinputtingvolume) | Set the volume of the current audio input device |
| [getInputtingVolume](function.md#iaudiodevicemanagergetinputtingvolume) | Get the volume of the current audio input device |
| [setInputtingMute](function.md#iaudiodevicemanagersetinputtingmute) | Mute or unmute the current audio input device |
| [getInputtingMute](function.md#iaudiodevicemanagergetinputtingmute) | Get the mute status of the current audio input device |
| [startInputDeviceTest](function.md#iaudiodevicemanagerstartinputdevicetest) | Start testing the current audio input device |
| [stopInputDeviceTest](function.md#iaudiodevicemanagerstopinputdevicetest) | Stop testing the current audio input device |
| [enumOutputDevices](function.md#iaudiodevicemanagerenumoutputdevices) | Enumerate audio playback devices |
| [setOutputtingDevice](function.md#iaudiodevicemanagersetoutputtingdevice) | Specify the audio playback device |
| [getOutputtingDevice](function.md#iaudiodevicemanagergetoutputtingdevice) | Get the current audio playback device |
| [setOuttingVolume](function.md#iaudiodevicemanagersetouttingvolume) | Set the volume of the current playback device |
| [getOuttingVolume](function.md#iaudiodevicemanagergetouttingvolume) | Get the volume of the current playback device |
| [setOutputtingMute](function.md#iaudiodevicemanagersetoutputtingmute) | Mute/Unmute the current playback device |
| [getOutputtingMute](function.md#iaudiodevicemanagergetoutputtingmute) | Get the mute status of the current playback device |
| [startOutputDeviceTest](function.md#iaudiodevicemanagerstartoutputdevicetest) | Start testing the current audio playback device |
| [stopOutputDeviceTest](function.md#iaudiodevicemanagerstopoutputdevicetest) | Stop testing the current audio playback device |
| [enableMicEnhancement](function.md#iaudiodevicemanagerenablemicenhancement) | Enable/Disable microphone enhancement |
| [enableMicDenoise](function.md#iaudiodevicemanagerenablemicdenoise) | Enable/Disable microphone noise reduction |
| [enableAEC](function.md#iaudiodevicemanagerenableaec) | Enable/Disable AEC |
| [enableAGC](function.md#iaudiodevicemanagerenableagc) | Enable/Disable Automatic Gain Control (AGC) |

| Callback | Function |
| :---| :--- |
| [onAudioCaptureStatus](notification.md#ithundereventhandleronaudiocapturestatus) | Callback on changes in audio device capture status |
| [onInputVolume](notification.md#ithundereventhandleroninputvolume) | Callback on test volume of the current audio input device |
| [onOutputVolume](notification.md#ithundereventhandleronoutputvolume) | Callback on test volume of the current audio playback device |

## Video Device Management

Major methods are encapsulated in the [IVideoDeviceManager](function.md#ivideodevicemanager) interface class and obtain object pointers through the [getVideoDeviceMgr](function.md#ithunderenginegetvideodevicemgr) interface.

| Method | Function |
| :---| :--- |
| [getVideoDeviceMgr](function.md#ithunderenginegetvideodevicemgr) | Get the pointer of the video device management object |

- [Methods in the IVideoDeviceManager](function.md#ivideodevicemanager) interface class

| Method | Function |
| :---| :--- |
| [enumVideoDevices](function.md#ivideodevicemanagerenumvideodevices) | Enumerate video input devices |
| [startVideoDeviceCapture](function.md#ivideodevicemanagerstartvideodevicecapture) | Start video device capturing |
| [stopVideoDeviceCapture](function.md#ivideodevicemanagerstopvideodevicecapture) | Stop video device capturing |
| [enumMonitorDevices](function.md#ivideodevicemanagerenummonitordevices) | Enumerate monitor input devices |

| Callback | Function |
| :---| :--- |
| [onVideoCaptureStatus](notification.md#ithundereventhandleronvideocapturestatus) | Reporting the camera capturing status |

## Media extra information

| Method | Function |
| :---| :--- |
| [registerMediaExtraInfoObserver](function.md#ithunderengineregistermediaextrainfoobserver) | Register the monitored object of media extra information [IThunderMediaExtraInfoObserver](notification.md#ithundermediaextrainfoobserver) |
| [sendMediaExtraInfo](function.md#ithunderenginesendmediaextrainfo) | Send media extra information |

- the [IThunderMediaExtraInfoObserver](notification.md#ithundermediaextrainfoobserver) interface class reports the status and informations of the MediaExtraInfo.

| Callback | Function |
| :---| :--- |
| [onSendMediaExtraInfoFailedStatus](notification.md#ithundermediaextrainfoobserveronsendmediaextrainfofailedstatus) | Callback on failure in sending media extra information |
| [onRecvMediaExtraInfo](notification.md#ithundermediaextrainfoobserveronrecvmediaextrainfo) | Received media extra information |
| [onRecvMixAudioInfo](notification.md#ithundermediaextrainfoobserveronrecvmixaudioinfo) | Received extra information of mixed audio stream |
| [onRecvMixVideoInfo](notification.md#ithundermediaextrainfoobserveronrecvmixvideoinfo) | Received extra information of mixed video stream |

## Audio Raw Data

| Method | Function |
| :---| :--- |
| [registerAudioFrameObserver](function.md#ithunderengineregisteraudioframeobserver) | Register a observer [IAudioFrameObserver](notification.md#iaudioframeobserver) |
| [setRecordingAudioFrameParameters](function.md#ithunderenginesetrecordingaudioframeparameters) | Set the mode for using raw audio recording data during callback [onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe) |
| [setPlaybackAudioFrameParameters](function.md#ithunderenginesetplaybackaudioframeparameters) | Set the mode for using raw audio playback data during callback [onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe) |

- the [IAudioFrameObserver](notification.md#iaudioframeobserver) interface class reports the information of the Audio Raw Data information.

| Callback | Function |
| :---| :--- |
| [onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe) | Callback on raw audio capture data |
| [onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe) | Callback on raw audio play data |
| [onPlaybackAudioFrameBeforeMixing](notification.md#iaudioframeobserveronplaybackaudioframebeforemixing) | Callback on raw data after the audio remote data decoding (differentiated among users) |

## Video Raw Data

| Method | Function |
| :---| :--- |
| [registerVideoFrameObserver](function.md#ithunderengineregistervideoframeobserver) | Register video monitor object [IVideoFrameObserver](notification.md#ivideoframeobserver) |
| [registerVideoCaptureObserver](function.md#ithunderengineregistervideocaptureobserver) | Register monitoring object for camera data capture [IVideoCaptureObserver.](notification.md#ivideocaptureobserver) |

- the [IVideoFrameObserver](notification.md#ivideoframeobserver) interface class reports the Video Raw Data (rendering & preview)information.

| Callback | Function |
| :---| :--- |
| [onPreviewVideoFrame](notification.md#ivideoframeobserveronpreviewvideoframe) | Occurs when local video preview data is returned. |
| [onRenderVideoFrame](notification.md#ivideoframeobserveronrendervideoframe) | Callback on rendering video data of other users |

- the [IVideoCaptureObserver](notification.md#ivideocaptureobserver) interface class reports the Video Raw Data (capturing) information.

| Callback | Function |
| :---| :--- |
| [onCaptureVideoFrame](notification.md#ivideocaptureobserveroncapturevideoframe) | Callback on video data collected locally |

## Custom Audio Capture

| Method | Function |
| :---| :--- |
| [setCustomAudioSource](function.md#ithunderenginesetcustomaudiosource) | Set parameters of external audio capturing |
| [pushCustomAudioFrame](function.md#ithunderenginepushcustomaudioframe) | Publishing an external audio frame |

## Custom Video Capture

| Method | Function |
| :---| :--- |
| [setCustomVideoSource](function.md#ithunderenginesetcustomvideosource) | Set parameters for external video capturing |
| [pushCustomVideoFrame](function.md#ithunderenginepushcustomvideoframe) | Publishing external video frame |

## Audio Self-rendering

N/A

## Video Self-rendering

N/A

## Custom Messages

| Method | Function |
| :---| :--- |
| [sendUserAppMsgData](function.md#ithunderenginesenduserappmsgdata) | Send custom broadcasting message |

| Callback | Function |
| :---| :--- |
| [onRecvUserAppMsgData](notification.md#ithundereventhandleronrecvuserappmsgdata) | Reporting custom broadcasting message |
| [onSendAppMsgDataFailedStatus](notification.md#ithundereventhandleronsendappmsgdatafailedstatus) | Callback on failure when sending broadcasting message |

## Log Management

| Method | Function |
| :---| :--- |
| [setLogFilePath](function.md#ithunderenginesetlogfilepath) | Set a directory for SDK to write the log files |
| [setLogLevel](function.md#ithunderenginesetloglevel) | Set the log levels |

## Other methods

| Method | Function |
| :---| :--- |
| [enableWebSdkCompatibility](function.md#ithunderengineenablewebsdkcompatibility) | Enable/Disable WebSDK compatibility |
