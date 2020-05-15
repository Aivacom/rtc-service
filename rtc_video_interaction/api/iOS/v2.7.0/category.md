# Overview

AIVACOM offers various client SDKs, and has a flexible API combination. A global real-time communication network is connected trough SDK, to provide real-time audio/video communication services with stable and reliable quality for developers.

The AIVACOM SDK has a code of`Thunderbolt`, and a pure audio SDK for a mobile terminal has a code of`Thunder`.

- [ThunderEngine](function.md#thunderengine) interface class provides all the methods that can be called by applications.
- [ThunderEventDelegate](notification.md#thundereventdelegate) interface class enables callbacks to your application.

## Basic Method

| Method | Function |
| :---| :--- |
| [createEngine](function.md#thunderenginecreateenginesceneiddelegate) | Create a ThunderEngine instance and initialize |
| [destroyEngine](function.md#thunderenginedestroyengine) | Destroy a ThunderEngine instance |
| [setThunderEventDelegate](function.md#thunderenginesetthundereventdelegate) | Set SDK callback event delegate |
| [getVersion](function.md#thunderenginegetversion) | Get SDK version information |

## Room Management

| Method | Function |
| :---| :--- |
| [setArea](function.md#thunderenginesetarea) | Set user’s area |
| [setSceneId](function.md#thunderenginesetsceneid) | Set scenario ID |
| [setMediaMode](function.md#thunderenginesetmediamode) | Set media mode |
| [setRoomMode](function.md#thunderenginesetroommode) | Set room mode |
| [joinRoom](function.md#thunderenginejoinroomroomnameuid) | Join a room |
| [leaveRoom](function.md#thunderengineleaveroom) | Leave a room |
| [updateToken](function.md#thunderengineupdatetoken) | Update token |

| Callback | Function |
| :---| :--- |
| [onJoinRoomSuccess](notification.md#thundereventdelegatethunderengineonjoinroomsuccesswithuidelapsed) | Callback when the local user joins a room |
| [onLeaveRoomWithStats](notification.md#thundereventdelegatethunderengineonleaveroomwithstats) | Callback upon leaving a room |
| [sdkAuthResult](notification.md#thundereventdelegatethunderenginesdkauthresult) | SDK authentication results notification. For details about authentication, refer to User Authentication Instructions on the official website |
| [onUserBanned](notification.md#thundereventdelegatethunderengineonuserbanned) | Callback on user banned |
| [onUserJoined](notification.md#thundereventdelegatethunderengineonuserjoinedelapsed) | Callback on remote user joining room |
| [onUserOffline](notification.md#thundereventdelegatethunderengineonuserofflinereason) | Callback on remote user leaving current room |
| [onRoomStats](notification.md#thundereventdelegatethunderengineonroomstats) | Callback on uplink/downlink traffic (periodic callback at an interval of 2s) |
| [bizAuthResult](notification.md#thundereventdelegatethunderenginebpublishbizauthresult) | Callback on service authentication results |
| [onTokenWillExpire](notification.md#thundereventdelegatethunderengineontokenwillexpire) | Callback on token to be expired |
| [thunderEngineTokenRequest](notification.md#thundereventdelegatethunderenginetokenrequest) | Callback on expired authentication |

## Audio Publishing

| Method | Function |
| :---| :--- |
| [setAudioConfig](function.md#thunderenginesetaudioconfigcommutmodescenariomode) | Set Audio Profiles |
| [setMicVolume](function.md#thunderenginesetmicvolume) | Set microphone volume |
| [stopLocalAudioStream](function.md#thunderenginestoplocalaudiostream) | Disable/Enable local audio (including audio capture, encoding and upload) |
| [setAudioSourceType](function.md#thunderenginesetaudiosourcetype) | Set publishing mode |

| Callback | Function |
| :---| :--- |
| [onFirstLocalAudioFrameSent](notification.md#thundereventdelegatethunderengineonfirstlocalaudioframesent) | Callback on the first local audio frame sent |
| [onLocalAudioStats](notification.md#thundereventdelegatethunderengineonlocalaudiostats) | Local audio statistics |

## Audio Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteAudioStreams](function.md#thunderenginestopallremoteaudiostreams) | Stop/Resume receiving all remote audio streams |
| [stopRemoteAudioStream](function.md#thunderenginestopremoteaudiostreamstopped) | Stop/Resume receiving audio stream of a specified user |
| [setPlayVolume](function.md#thunderaudiofileplayersetplayvolume) | Set local playing volume of a user |

| Callback | Function |
| :---| :--- |
| [onRemoteAudioStopped](notification.md#thundereventdelegatethunderengineonremoteaudiostoppedbyuid) | Callback on stopping/starting remote user audio stream |
| [onRemoteAudioStatsOfUid](notification.md#thundereventdelegatethunderengineonremoteaudiostatsofuidstats) | Callback on remote audio stream information during the call |

## Video Publishing

| Method | Function |
| :---| :--- |
| [setVideoEncoderConfig](function.md#thunderenginesetvideoencoderconfig) | Set video encoding configuration |
| [setLocalVideoCanvas](function.md#thunderenginesetlocalvideocanvas) | Set the rendering canvas of a local video |
| [enableLocalVideoCapture](function.md#thunderengineenablelocalvideocapture) | Enable/Disable local video capture |
| [startVideoPreview](function.md#thunderenginestartvideopreview) | Start video preview of local camera |
| [stopVideoPreview](function.md#thunderenginestopvideopreview) | Stop video preview of a local camera |
| [setLocalCanvasScaleMode](function.md#thunderenginesetlocalcanvasscalemode) | Set local view display mode |
| [stopLocalVideoStream](function.md#thunderenginestoplocalvideostream) | Enable/Disable local video sending |

| Callback | Function |
| :---| :--- |
| [onFirstLocalVideoFrameSent](notification.md#thundereventdelegatethunderengineonfirstlocalvideoframesent) | Callback on the first local video frame sent |
| [onLocalVideoStats](notification.md#thundereventdelegatethunderengineonlocalvideostats) | Callback on local video statistics |

## Video Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteVideoStreams](function.md#thunderenginestopallremotevideostreams) | Stop/Resume receiving all remote video streams              |
| [stopRemoteVideoStream](function.md#thunderenginestopremotevideostreamstopped) | Stop/Resume receiving video stream of a specified user      |
| [setRemoteCanvasScaleMode](function.md#thunderenginesetremotecanvasscalemodemode) | Set the scale mode of the remote video stream on the canvas |
| [setRemoteVideoCanvas](function.md#thunderenginesetremotevideocanvas) | Set the rendering view of the remote video |
| [setRemotePlayType](function.md#thunderenginesetremoteplaytype) | Sets the type of remote user's render view |
| [setMultiVideoViewLayout](function.md#thunderenginesetmultivideoviewlayout) | Set the layout parameters of the multi videos on the view |

| Callback | Function |
| :---| :--- |
| [onRemoteVideoStopped](notification.md#thundereventdelegatethunderengineonremotevideostoppedbyuid) | Callback when the remote user's video stream starts or stops |
| [onRemoteVideoStatsOfUid](notification.md#thundereventdelegatethunderengineonremotevideostatsofuidstats) | Report statistics of remote user video stream                |
| [onRemoteVideoPlay](notification.md#thundereventdelegatethunderengineonremotevideoplaysizeelapsed) | Callback when displaying the first frame of remote video     |
| [onVideoSizeChangedOfUid](notification.md#thundereventdelegatethunderengineonvideosizechangedofuidsizerotation) | Callback when the resolution of local or remote video changes |

## Network status

| Callback | Function |
| :---| :--- |
| [onNetworkQuality](notification.md#thundereventdelegatethunderengineonnetworkqualitytxqualityrxquality) | Report the uplink and downlink network quality of each user |
| [onNetworkTypeChanged](notification.md#thundereventdelegatethunderengineonnetworktypechanged) | Callback when the network type changes                      |
| [onConnectionStatus](notification.md#thundereventdelegatethunderengineonconnectionstatus) | Report the connection status with the server |
| [thunderEngineConnectionLost](notification.md#thundereventdelegatethunderengineconnectionlost) | Callback when losing connection with server |

## Publishing detection

N/A

## Video mixing and stream publishing

| Method | Function |
| :---| :--- |
| [setLiveTranscodingTask](function.md#thunderenginesetlivetranscodingtasktranscoding) | Add or update transcoding task |
| [removeLiveTranscodingTask](function.md#thunderengineremovelivetranscodingtask) | Remove a transcoding task |
| [addPublishTranscodingStreamUrl](function.md#thunderengineaddpublishtranscodingstreamurlurl) | Add a push address of transcoding stream          |
| [removePublishTranscodingStreamUrl](function.md#thunderengineremovepublishtranscodingstreamurlurl) | Remove the push address of the transcoding stream |
| [addPublishOriginStreamUrl](function.md#thunderengineaddpublishoriginstreamurl) | Add a push address of source stream               |
| [removePublishOriginStreamUrl](function.md#thunderengineremovepublishoriginstreamurl) | Remove the push address of source stream          |
| [enableMixVideoExtraInfo](function.md#thunderengineenablemixvideoextrainfo) | Enable video mixing with media extra information |

| Callback | Function |
| :---| :--- |
| [onPublishStreamToCDNStatusWithUrl](notification.md#thundereventdelegatethunderengineonpublishstreamtocdnstatuswithurlerrorcode) | Report the result of pushing stream to the CDN |

## Audio Recording

| Method | Function |
| :---| :--- |
| [startAudioSaver](function.md#thunderenginestartaudiosaversavermodefilemode) | Start saving audio data as aac format |
| [stopAudioSaver](function.md#thunderenginestopaudiosaver) | Stop saving audio data as aac format |

## Cross-room Microphone Connection

| Method | Function |
| :---| :--- |
| [addSubscribe](function.md#thunderengineaddsubscribeuid) | Subscribe stream of specified user across the room |
| [removeSubscribe](function.md#thunderengineremovesubscribeuid) | Cancel cross-room subscription of specified users |

## Camera Management

| Method | Function |
| :---| :--- |
| [switchFrontCamera](function.md#thunderengineswitchfrontcamera) | Switch to front/rear camera |
| [setVideoCaptureOrientation](function.md#thunderenginesetvideocaptureorientation) | Set portrait/landscape, default is portrait. Available for publishing before preview. |
| [setLocalVideoMirrorMode](function.md#thunderenginesetlocalvideomirrormode) | Set camera mirroring. Available for publishing before preview, valid for front camera only |

## Screen Sharing

N/A

## Real-time Watermark

| Method | Function |
| :---| :--- |
| [setVideoWatermark](function.md#thunderenginesetvideowatermark) | Add local video watermark |

## Video Dual Stream

N/A

## Audio Player

| Method | Function |
| :---| :--- |
| [createAudioFilePlayer](function.md#thunderenginecreateaudiofileplayer) | Create file player [ThunderAudioFilePlayer](function.md#thunderaudiofileplayer) object |
| [destroyAudioFilePlayer](function.md#thunderenginedestroyaudiofileplayer) | Destroy file player [ThunderAudioFilePlayer](function.md#thunderaudiofileplayer) object |

- [Method in a ThunderAudioFilePlayer](function.md#thunderaudiofileplayer) class

| Method | Function |
| :---| :--- |
| [open](function.md#thunderaudiofileplayeropen) | Open audio file, formats supported: mp3, aac, wav |
| [close](function.md#thunderaudiofileplayerclose) | Close audio file |
| [play](function.md#thunderaudiofileplayerplay) | Start playing |
| [Stop](function.md#thunderaudiofileplayerstop) | Stop playing |
| [pause](function.md#thunderaudiofileplayerpause) | Pause playing |
| [resume](function.md#thunderaudiofileplayerresume) | Continue to play |
| [seek](function.md#thunderaudiofileplayerseek) | Skipping to specified play time |
| [getTotalPlayTimeMS](function.md#thunderaudiofileplayergettotalplaytimems) | Get the total play time of files |
| [getCurrentPlayTimeMS](function.md#thunderaudiofileplayergetcurrentplaytimems) | Get the time which has been played |
| [setPlayerLocalVolume](function.md#thunderaudiofileplayersetplayerlocalvolume) | Adjust volume of music file in mixed video being played locally. Please call this method in room |
| [setPlayerPublishVolume](function.md#thunderaudiofileplayersetplayerpublishvolume) | Adjust volume of music file in mixed video being played remotely. Please call this method in room |
| [getPlayerLocalVolume](function.md#thunderaudiofileplayergetplayerlocalvolume) | Get the local playing volume of the file                     |
| [getPlayerPublishVolume](function.md#thunderaudiofileplayergetplayerpublishvolume) | Get the remote playing volume of the file                    |
| [setLooping](function.md#thunderaudiofileplayersetlooping) | Set times of loop playbacks |
| [setPlayerDelegate](function.md#thunderaudiofileplayersetplayerdelegate) | Set a player callback delegate |
| [enableSpectrum](function.md#thunderaudiofileplayerenablespectrum) | Enable/Disable spectrum |
| [enableVolumeIndication](function.md#thunderaudiofileplayerenablevolumeindicationinterval) | Callback on turning on/off volume |
| [setMixStandard](function.md#thunderaudiofileplayersetmixstandard) | Set whether the accompaniment is a standard stream for video mixing |
| [isMixStandard](function.md#thunderaudiofileplayerismixstandard) | Query whether the accompaniment is a standard stream for video mixing |
| [getCurrentSpectrum](function.md#thunderaudiofileplayergetcurrentspectrumlen) | Obtain spectrum information; value range [0-1] |

- Monitor callback via interface class [ThunderAudioFilePlayerDelegate](notification.md#thunderaudiofileplayerdelegate)

| Callback | Function |
| :---| :--- |
| [onAudioFileVolume](notification.md#thunderaudiofileplayerdelegateonaudiofilevolumevolumecurrentmstotalms) | Callback when playing volume |
| [onAudioFilePlayEnd](notification.md#thunderaudiofileplayerdelegateonaudiofileplayend) | Callback when end playing                         |
| [onAudioFilePlayError](notification.md#thunderaudiofileplayerdelegateonaudiofileplayerrorerrorcode) | Callback when audio file playing occur error      |
| [onAudioFilePlaying](notification.md#thunderaudiofileplayerdelegateonaudiofileplaying) | Callback when start playing                       |
| [onAudioFilePause](notification.md#thunderaudiofileplayerdelegateonaudiofilepause) | Callback when pause playing                       |
| [onAudioFileResume](notification.md#thunderaudiofileplayerdelegateonaudiofileresume) | Callback when resume playing                      |
| [onAudioFileStop](notification.md#thunderaudiofileplayerdelegateonaudiofilestop) | Callback when stop playing                        |
| [onAudioFileSeekComplete](notification.md#thunderaudiofileplayerdelegateonaudiofileseekcompletemilliseconds) | Callback when the audio file seeking is completed |
| [onAudioFileStateChange](notification.md#thunderaudiofileplayerdelegateonaudiofilestatechangeeventerrorcode) | Report the status of the playing audio file |


## Sound change in reverb

| Method | Function |
| :---| :--- |
| [setVoiceChanger](function.md#thunderenginesetvoicechanger) | Set voice change mode |
| [setSoundEffect](function.md#thunderenginesetsoundeffect) | Set different sound effects |
| [setEnableReverb](function.md#thunderenginesetenablereverb) | Enable/Disable reverb |
| [setReverbParam](function.md#thunderenginesetreverbparam) | Set reverb parameters |
| [setEnableEqualizer](function.md#thunderenginesetenableequalizer) | Enable/Disable equalizer |
| [setEqGains](function.md#thunderengineseteqgains) | Set equalizer parameters |
| [setEnableCompressor](function.md#thunderenginesetenablecompressor) | Enable/Disable compressor |
| [setCompressorParam](function.md#thunderenginesetcompressorparam) | Set compressor parameters |
| [setEnableLimiter](function.md#thunderenginesetenablelimiter) | Enable/Disable pressure limiter |
| [setLimiterParam](function.md#thunderenginesetlimiterparam) | Set pressure limiter parameters |

## Voice Positioning

| Method | Function |
| :---| :--- |
| [enableVoicePosition](function.md#thunderengineenablevoiceposition) | Enable/Disable voice stereo of remote users |
| [setRemoteUidVoicePosition](function.md#thunderenginesetremoteuidvoicepositionazimuthgain) | Set spatial location and volume of remote user's voice |

## Volume Prompt

| Method | Function |
| :---| :--- |
| [enableCaptureVolumeIndication](function.md#thunderengineenablecapturevolumeindicationmorethanthdlessthanthdsmooth) | Callback on turning on/off microphone volume |
| [setAudioVolumeIndication](function.md#thunderenginesetaudiovolumeindicationmorethanthdlessthanthdsmooth) | Callback on turning on/off user volume |

| Callback | Function |
| :---| :--- |
| [onCaptureVolumeIndication](notification.md#thunderengineoncapturevolumeindicationcptmicvolume) | Report the cpature volume                                |
| [onPlayVolumeIndication](notification.md#thundereventdelegateonplayvolumeindicationtotalvolume) | Report which users are speaking and the speakers' volume |

## Voice Routing

| Method | Function |
| :---| :--- |
| [enableLoudspeaker](function.md#thunderengineenableloudspeaker) | Enable a loudspeaker |
| [isLoudspeakerEnabled](function.md#thunderengineisloudspeakerenabled) | Query whether the loudspeaker is enabled at |
| [setLoudSpeakerVolume](function.md#thunderenginesetloudspeakervolume) | Set loudspeaker volume |

## In-ear Monitor

| Method | Function |
| :---| :--- |
| [setEnableInEarMonitor](function.md#thunderenginesetenableinearmonitor) | Enable/Disable ear monitor |


## Audio Device Management

| Callback | Function |
| :---| :--- |
| [onAudioCaptureStatus](notification.md#thundereventdelegatethunderengineonaudiocapturestatus) | Report the status of the  audio capture device |

## Video Device Management

| Callback | Function |
| :---| :--- |
| [onVideoCaptureStatus](notification.md#thundereventdelegatethunderengineonvideocapturestatus) | Report the status of the video capture device |

## Media extra information

| Method | Function |
| :---| :--- |
| [setMediaExtraInfoDelegate](function.md#thunderenginesetmediaextrainfodelegate) | Set callback delegate of media extra information [ThunderMediaExtraInfoDelegate](notification.md#thundermediaextrainfodelegate) |
| [sendMediaExtraInfo](function.md#thunderenginesendmediaextrainfo) | Send media extra information (during audio/video streaming) |

- Monitor callback via interface type [ThunderMediaExtraInfoDelegate](notification.md#thundermediaextrainfodelegate)

| Callback | Function |
| :---| :--- |
| [onSendMediaExtraInfoFailedStatus](notification.md#thundermediaextrainfodelegateonsendmediaextrainfofailedstatus) | Callback when failure in sending media extra information     |
| [onRecvMediaExtraInfo](notification.md#thundermediaextrainfodelegateonrecvmediaextrainfoofuid) | Callback when received media extra information               |
| [onRecvMixAudioInfo](notification.md#thundermediaextrainfodelegateonrecvmixaudioinfoofuid) | Callback when received extra information of mixed audio stream |
| [onRecvMixVideoInfo](notification.md#thundermediaextrainfodelegateonrecvmixvideoinfoofuid) | Callback when received extra information of mixed video stream |

## Raw Audio Data

| Method | Function |
| :---| :--- |
| [enableAudioDataIndication](function.md#thunderengineenableaudiodataindication) | Enable/Disable data callback on audio playing |
| [enableAudioPlaySpectrum](function.md#thunderengineenableaudioplayspectrum) | Enable/Disable data callback on audio play spectrum |
| [setAudioPlaySpectrumInfo](function.md#thunderenginesetaudioplayspectruminfonotifyintervalms) | Set audio playback spectrum parameters |
| [enableCapturePcmDataCallBack](function.md#thunderengineenablecapturepcmdatacallbacksampleratechannel) | Enable/Disable data callback on audio capture |
| [syncMediaPlayingProgress](function.md#thunderenginesyncmediaplayingprogress) | Synchronize play progress of external accompaniment video for mixed video synchronization. Audio accompaniment and video accompaniment cannot be supported at the same time. |
| [setRecordingAudioFrameParameters](function.md#thunderenginesetrecordingaudioframeparameterschannelmodesamplespercall) | Set the mode for using raw audio recording data during callback onRecordAudioFrame |
| [setPlaybackAudioFrameParameters](function.md#thunderenginesetplaybackaudioframeparameterschannelmodesamplespercall) | Set the mode for using raw audio playback data during callback onPlaybackAudioFrame |


| Callback | Function |
| :---| :--- |
| [onAudioPlayData](notification.md#thundereventdelegatethunderengineonaudioplaydatadurationcptptsdata) | Callback on audio playback data |
| [onAudioPlaySpectrumData](notification.md#thundereventdelegatethunderengineonaudioplayspectrumdata) | Callback on audio play spectrum data |

- Monitor callback via interface type [IAudioFrameObserver](notification.md#iaudioframeobserver)

| Callback                                                         | Function                           |
| :----------------------------------------------------------- | :----------------------------- |
| [onRecordAudioFrame](notification.md#iaudioframeobserveronrecordaudioframe) | Callback on raw audio capture data           |
| [onPlaybackAudioFrame](notification.md#iaudioframeobserveronplaybackaudioframe) | Callback on raw audio play data           |
| [onPlaybackAudioFrameBeforeMixing](notification.md#iaudioframeobserveronplaybackaudioframebeforemixing) | Callback of original data decoded by remote user can differentiate users through different uids |

## Raw Video Data

| Method | Function |
| :---| :--- |
| [registerVideoCaptureFrameObserver](function.md#thunderengineregistervideocaptureframeobserver) | Set the interface for callback on local video preprocessing |
| [registerVideoDecodeFrameObserver](function.md#thunderengineregistervideodecodeframeobserveruid) | Customize decoding picture rendering |

- Callback log via interface [ThunderVideoCaptureFrameObserver](notification.md#thundervideocaptureframeobserver)

| Callback | Function |
| :---| :--- |
| [needThunderVideoCaptureFrameDataType](notification.md#thundervideocaptureframeobserverneedthundervideocaptureframedatatype) | Declare to SDK data in which format is to be used |
| [onVideoCaptureFrame](notification.md#thundervideocaptureframeobserveronvideocaptureframepixelbuffer) | Receive a frame of data from capture for processing and return processed data |
| [onVideoCaptureFrame](notification.md#thundervideocaptureframeobserveronvideocaptureframepixelbuffersourcetextureiddestinationtextureidtextureformattexturetargettexturewidthtextureheight) | Return original texture parameters and target texture parameters |

- Callback log via interface [ThunderVideoDecodeFrameObserver](notification.md#thundervideodecodeframeobserver)

| Callback | Function |
| :---| :--- |
| [onVideoDecodeFrame](notification.md#thundervideodecodeframeobserveronvideodecodeframeptsuid) | Custom rendering of a decoded image is to cut out the decoded image of SDK for custom rendering of services |

## Custom Audio Capture

| Method | Function |
| :---| :--- |
| [enableCustomAudioSource](function.md#thunderengineenablecustomaudiosourcechannelsperframe) | Enable external audio capture |
| [pushCustomAudioRawData](function.md#thunderenginepushcustomaudiorawdatasamplestimestamp) | Push external audio stream |
| [pushCustomAudioSampleBuffer](function.md#thunderenginepushcustomaudiosamplebuffer) | Pushing an external audio frame |
| [disableCustomAudioSource](function.md#thunderenginedisablecustomaudiosource) | Disable external audio capture |

- Monitor callback via interface [ThunderExternalAudioProcessorDelegate](notification.md#thunderexternalaudioprocessordelegate)

| Callback | Function |
| :---| :--- |
| [audioCaptureStart](notification.md#thunderexternalaudioprocessordelegateaudiocapturestart) | Audio capture starts |
| [audioCaptureData](notification.md#thunderexternalaudioprocessordelegateaudiocapturedatadatalensampleratechannelcountbitpersample) | Callback on audio capture data |
| [audioCaptureStop](notification.md#thunderexternalaudioprocessordelegateaudiocapturestop) | Audio capture stops |
| [audioRenderStart](notification.md#thunderexternalaudioprocessordelegateaudiorenderstart) | Audio rendering starts |
| [audioRenderData](notification.md#thunderexternalaudioprocessordelegateaudiorenderdatadatalensampleratechannelcountbitpersample) | Callback on audio rendering data |
| [audioRenderStop](notification.md#thunderexternalaudioprocessordelegateaudiorenderstop) | Audio rendering stops |

## Custom Video Capture

| Method | Function |
| :---| :--- |
| [setCustomVideoSource](function.md#thunderenginesetcustomvideosource) | Set external video capture source |

- Callback via interface [ThunderCustomVideoSourceProtocol](notification.md#thundercustomvideosourceprotocol)

| Callback | Function |
| :---| :--- |
| [onInitialize](notification.md#thundercustomvideosourceprotocoloninitialize) | Initialize video source |
| [bufferType](notification.md#thundercustomvideosourceprotocolbuffertype) | Obtain Buffer type |
| [onStart](notification.md#thundercustomvideosourceprotocolonstart) | Start video source |
| [onStop](notification.md#thundercustomvideosourceprotocolonstop) | Stop video source |
| [onDispose](notification.md#thundercustomvideosourceprotocolondispose) | Dispose video source |

- Push external video data via interface [ThunderVideoFrameConsumer](function.md#thundervideoframeconsumer)

| Callback | Function |
| :---| :--- |
| [consumePixelBuffer](function.md#thundervideoframeconsumerconsumepixelbufferwithtimestamprotation) | Interface for pushing raw video data |
| [consumeRawData](function.md#thundervideoframeconsumerconsumerawdatawithtimestampformatsizerotation) | Interface for pushing raw video data |
| [consumeCMSampleBuffer](function.md#thundervideoframeconsumerconsumecmsamplebuffer) | Interface for pushing raw video data |

## Audio Self-rendering

| Method | Function |
| :---| :--- |
| [enableRenderPcmDataCallBack](function.md#thunderengineenablerenderpcmdatacallbacksampleratechannel) | Enable/Disable callback on audio rending data |

| Callback | Function |
| :---| :--- |
| [onAudioRenderPcmData](notification.md#thundereventdelegatethunderengineonaudiorenderpcmdatadurationsampleratechannel) | Callback audio rendering data |

## Video Self-rendering

| Method | Function |
| :---| :--- |
| [registerVideoDecodeFrameObserver](function.md#thunderengineregistervideodecodeframeobserveruid) | Set decoding data callback for video stream of a certain vid |

- Callback via interface [ThunderVideoDecodeFrameObserver](notification.md#thundervideodecodeframeobserver)

| Callback | Function |
| :---| :--- |
| [onVideoDecodeFrame](notification.md#thundervideodecodeframeobserveronvideodecodeframeptsuid) | Receive decoded frame data from decoder |

## Custom Messages

| Method | Function |
| :---| :--- |
| [sendUserAppMsgData](function.md#thunderenginesenduserappmsgdata) | Sending developer's custom broadcast messages |

| Callback | Function |
| :---| :--- |
| [onRecvUserAppMsgData](notification.md#thundereventdelegateonrecvuserappmsgdatauid) | Callback when received developer's custom broadcast messages |
| [onSendAppMsgDataFailedStatus](notification.md#thundereventdelegatethunderengineonsendappmsgdatafailedstatus) | Callback on failures in sending custom broadcast message of service |

## Log Management

| Method | Function |
| :---| :--- |
| [setLogFilePath](function.md#thunderenginesetlogfilepath) | Set directory for SDK to output log files. A directory with write permissions must be specified. |
| [setLogLevel](function.md#thunderenginesetloglevel) | Set log levels |
| [setLogCallback](function.md#thunderenginesetlogcallback) | Set log callback. Once log callback is set, setLogFilePath is invalid |

- Callback log via interface [ThunderRtcLogDelegate](notification.md#thunderrtclogdelegate)

| Callback | Function |
| :---| :--- |
| [onThunderRtcLogWithLevel](notification.md#thunderrtclogdelegateonthunderrtclogwithlevelmessage) | Callback on log information |

## Other methods

| Method | Function |
| :---| :--- |
| [enableWebSdkCompatibility](function.md#thunderengineenablewebsdkcompatibility) | Enable/Disable WebSDK compatibility |
