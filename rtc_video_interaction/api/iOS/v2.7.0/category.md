# Overview

AIVACOM offers various client SDKs, and has a flexible API combination. A global real-time communication network is connected trough SDK, to provide real-time audio/video communication services with stable and reliable quality for developers.

The AIVACOM SDK has a code of`Thunderbolt`, and a pure audio SDK for a mobile terminal has a code of`Thunder`.

- [ThunderEngine](function.md#ThunderEngine) interface class provides all the methods that can be called by applications.
- [ThunderEventDelegate](notification.md#ThunderEventDelegate) interface class enables callbacks to your application.

## Basic Method

| Method | Function |
| :---| :--- |
| [createEngine](function.md#ThunderEngine::createEngine:sceneId:delegate:) | Create a ThunderEngine instance and initialize |
| [destroyEngine](function.md#ThunderEngine::destroyEngine) | Destroy a ThunderEngine instance |
| [setThunderEventDelegate](function.md#ThunderEngine::setThunderEventDelegate) | Set SDK callback event delegate |
| [getVersion](function.md#ThunderEngine::getVersion) | Get SDK version information |

## Room Management

| Method | Function |
| :---| :--- |
| [setArea](function.md#ThunderEngine::setArea:) | Set user’s area |
| [setSceneId](function.md#ThunderEngine::setSceneId) | Set scenario ID |
| [setMediaMode](function.md#ThunderEngine::setMediaMode:) | Set media mode |
| [setRoomMode](function.md#ThunderEngine::setRoomMode:) | Set room mode |
| [joinRoom](function.md#ThunderEngine::joinRoom:roomName:uid) | Join a room |
| [leaveRoom](function.md#ThunderEngine::leaveRoom) | Leave a room |
| [updateToken](function.md#ThunderEngine::updateToken:) | Update token |

| Callback | Function |
| :---| :--- |
| [onJoinRoomSuccess](notification.md#ThunderEventDelegate::thunderEngine:onJoinRoomSuccess:withUid:elapsed:) | Callback when the local user joins a room |
| [onLeaveRoomWithStats](notification.md#ThunderEventDelegate::thunderEngine:onLeaveRoomWithStats) | Callback upon leaving a room |
| [sdkAuthResult](notification.md#ThunderEventDelegate::thunderEngine:sdkAuthResult) | SDK authentication results notification. For details about authentication, refer to User Authentication Instructions on the official website |
| [onUserBanned](notification.md#ThunderEventDelegate::thunderEngine:onUserBanned) | Callback on user banned |
| [onUserJoined](notification.md#ThunderEventDelegate::thunderEngine:onUserJoined:elapsed) | Callback on remote user joining room |
| [onUserOffline](notification.md#ThunderEventDelegate::thunderEngine:onUserOffline:reason) | Callback on remote user leaving current room |
| [onRoomStats](notification.md#ThunderEventDelegate::thunderEngine:onRoomStats) | Callback on uplink/downlink traffic (periodic callback at an interval of 2s) |
| [bizAuthResult](notification.md#ThunderEventDelegate::thunderEngine:bPublish:bizAuthResult) | Callback on service authentication results |
| [onTokenWillExpire](notification.md#ThunderEventDelegate::thunderEngine:onTokenWillExpire) | Callback on token to be expired |
| [thunderEngineTokenRequest](notification.md#ThunderEventDelegate::thunderEngineTokenRequest) | Callback on expired authentication |

## Audio Publishing

| Method | Function |
| :---| :--- |
| [setAudioConfig](function.md#ThunderEngine::setAudioConfig:commutMode:scenarioMode) | Set Audio Profiles |
| [setMicVolume](function.md#ThunderEngine::setMicVolume:) | Set microphone volume |
| [stopLocalAudioStream](function.md#ThunderEngine::stopLocalAudioStream:) | Disable/Enable local audio (including audio capture, encoding and upload) |
| [setAudioSourceType](function.md#ThunderEngine::setAudioSourceType:) | Set publishing mode |

| Callback | Function |
| :---| :--- |
| [onFirstLocalAudioFrameSent](notification.md#ThunderEventDelegate::thunderEngine:onFirstLocalAudioFrameSent) | Callback on the first local audio frame sent |
| [onLocalAudioStats](notification.md#ThunderEventDelegate::thunderEngine:onLocalAudioStats) | Local audio statistics |

## Audio Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteAudioStreams](function.md#ThunderEngine::stopAllRemoteAudioStreams:) | Stop/Resume receiving all remote audio streams |
| [stopRemoteAudioStream](function.md#ThunderEngine::stopRemoteAudioStream:stopped) | Stop/Resume receiving audio stream of a specified user |
| [setPlayVolume](function.md#ThunderAudioFilePlayer::setPlayVolume:) | Set local playing volume of a user |

| Callback | Function |
| :---| :--- |
| [onRemoteAudioStopped](notification.md#ThunderEventDelegate::thunderEngine:onRemoteAudioStopped:byUid) | Callback on stopping/starting remote user audio stream |
| [onRemoteAudioStatsOfUid](notification.md#ThunderEventDelegate::thunderEngine:onRemoteAudioStatsOfUid:stats) | Callback on remote audio stream information during the call |

## Video Publishing

| Method | Function |
| :---| :--- |
| [setVideoEncoderConfig](function.md#ThunderEngine::setVideoEncoderConfig) | Set video encoding configuration |
| [setLocalVideoCanvas](function.md#ThunderEngine::setLocalVideoCanvas) | Set the rendering canvas of a local video |
| [enableLocalVideoCapture](function.md#ThunderEngine::enableLocalVideoCapture) | Enable/Disable local video capture |
| [startVideoPreview](function.md#ThunderEngine::startVideoPreview) | Start video preview of local camera |
| [stopVideoPreview](function.md#ThunderEngine::stopVideoPreview) | Stop video preview of a local camera |
| [setLocalCanvasScaleMode](function.md#ThunderEngine::setLocalCanvasScaleMode) | Set local view display mode |
| [stopLocalVideoStream](function.md#ThunderEngine::stopLocalVideoStream) | Enable/Disable local video sending |

| Callback | Function |
| :---| :--- |
| [onFirstLocalVideoFrameSent](notification.md#ThunderEventDelegate::thunderEngine:onFirstLocalVideoFrameSent) | Callback on the first local video frame sent |
| [onLocalVideoStats](notification.md#ThunderEventDelegate::thunderEngine:onLocalVideoStats) | Callback on local video statistics |

## Video Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteVideoStreams](function.md#ThunderEngine::stopAllRemoteVideoStreams) | Stop/Resume receiving all remote video streams              |
| [stopRemoteVideoStream](function.md#ThunderEngine::stopRemoteVideoStream:stopped) | Stop/Resume receiving video stream of a specified user      |
| [setRemoteCanvasScaleMode](function.md#ThunderEngine::setRemoteCanvasScaleMode:mode) | Set the scale mode of the remote video stream on the canvas |
| [setRemoteVideoCanvas](function.md#ThunderEngine::setRemoteVideoCanvas) | Set the rendering view of the remote video |
| [setRemotePlayType](function.md#ThunderEngine::setRemotePlayType) | Sets the type of remote user's render view |
| [setMultiVideoViewLayout](function.md#ThunderEngine::setMultiVideoViewLayout) | Set the layout parameters of the multi videos on the view |

| Callback | Function |
| :---| :--- |
| [onRemoteVideoStopped](notification.md#ThunderEventDelegate::thunderEngine:onRemoteVideoStopped:byUid) | Callback when the remote user's video stream starts or stops |
| [onRemoteVideoStatsOfUid](notification.md#ThunderEventDelegate::thunderEngine:onRemoteVideoStatsOfUid:stats) | Report statistics of remote user video stream                |
| [onRemoteVideoPlay](notification.md#ThunderEventDelegate::thunderEngine:onRemoteVideoPlay:size:elapsed) | Callback when displaying the first frame of remote video     |
| [onVideoSizeChangedOfUid](notification.md#ThunderEventDelegate::thunderEngine:onVideoSizeChangedOfUid:size:rotation) | Callback when the resolution of local or remote video changes |

## Network status

| Callback | Function |
| :---| :--- |
| [onNetworkQuality](notification.md#ThunderEventDelegate::thunderEngine:onNetworkQuality:txQuality:rxQuality) | Report the uplink and downlink network quality of each user |
| [onNetworkTypeChanged](notification.md#ThunderEventDelegate::thunderEngine:onNetworkTypeChanged) | Callback when the network type changes                      |
| [onConnectionStatus](notification.md#ThunderEventDelegate::thunderEngine:onConnectionStatus) | Report the connection status with the server |
| [thunderEngineConnectionLost](notification.md#ThunderEventDelegate::thunderEngineConnectionLost) | Callback when losing connection with server |

## Publishing detection

N/A

## Video mixing and stream publishing

| Method | Function |
| :---| :--- |
| [setLiveTranscodingTask](function.md#ThunderEngine::setLiveTranscodingTask:transcoding) | Add or update transcoding task |
| [removeLiveTranscodingTask](function.md#ThunderEngine::removeLiveTranscodingTask) | Remove a transcoding task |
| [addPublishTranscodingStreamUrl](function.md#ThunderEngine::addPublishTranscodingStreamUrl:url) | Add a push address of transcoding stream          |
| [removePublishTranscodingStreamUrl](function.md#ThunderEngine::removePublishTranscodingStreamUrl:url) | Remove the push address of the transcoding stream |
| [addPublishOriginStreamUrl](function.md#ThunderEngine::addPublishOriginStreamUrl) | Add a push address of source stream               |
| [removePublishOriginStreamUrl](function.md#ThunderEngine::removePublishOriginStreamUrl) | Remove the push address of source stream          |
| [enableMixVideoExtraInfo](function.md#ThunderEngine::enableMixVideoExtraInfo:) | Enable video mixing with media extra information |

| Callback | Function |
| :---| :--- |
| [onPublishStreamToCDNStatusWithUrl](notification.md#ThunderEventDelegate::thunderEngine:onPublishStreamToCDNStatusWithUrl:errorCode) | Report the result of pushing stream to the CDN |

## Audio Recording

| Method | Function |
| :---| :--- |
| [startAudioSaver](function.md#ThunderEngine::startAudioSaver:saverMode:fileMode:) | Start saving audio data as aac format |
| [stopAudioSaver](function.md#ThunderEngine::stopAudioSaver) | Stop saving audio data as aac format |

## Cross-room Microphone Connection

| Method | Function |
| :---| :--- |
| [addSubscribe](function.md#ThunderEngine::addSubscribe:uid) | Subscribe stream of specified user across the room |
| [removeSubscribe](function.md#ThunderEngine::removeSubscribe:uid) | Cancel cross-room subscription of specified users |

## Camera Management

| Method | Function |
| :---| :--- |
| [switchFrontCamera](function.md#ThunderEngine::switchFrontCamera) | Switch to front/rear camera |
| [setVideoCaptureOrientation](function.md#ThunderEngine::setVideoCaptureOrientation) | Set portrait/landscape, default is portrait. Available for publishing before preview. |
| [setLocalVideoMirrorMode](function.md#ThunderEngine::setLocalVideoMirrorMode) | Set camera mirroring. Available for publishing before preview, valid for front camera only |

## Screen Sharing

N/A

## Real-time Watermark

| Method | Function |
| :---| :--- |
| [setVideoWatermark](function.md#ThunderEngine::setVideoWatermark) | Add local video watermark |

## Video Dual Stream

N/A

## Audio Player

| Method | Function |
| :---| :--- |
| [createAudioFilePlayer](function.md#ThunderEngine::createAudioFilePlayer) | Create file player [ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) object |
| [destroyAudioFilePlayer](function.md#ThunderEngine::destroyAudioFilePlayer:) | Destroy file player [ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) object |

- [Method in a ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) class

| Method | Function |
| :---| :--- |
| [open](function.md#ThunderAudioFilePlayer::open) | Open audio file, formats supported: mp3, aac, wav |
| [close](function.md#ThunderAudioFilePlayer::close) | Close audio file |
| [play](function.md#ThunderAudioFilePlayer::play) | Start playing |
| [Stop](function.md#ThunderAudioFilePlayer::stop) | Stop playing |
| [pause](function.md#ThunderAudioFilePlayer::pause) | Pause playing |
| [resume](function.md#ThunderAudioFilePlayer::resume) | Continue to play |
| [seek](function.md#ThunderAudioFilePlayer::seek:) | Skipping to specified play time |
| [getTotalPlayTimeMS](function.md#ThunderAudioFilePlayer::getTotalPlayTimeMS) | Get the total play time of files |
| [getCurrentPlayTimeMS](function.md#ThunderAudioFilePlayer::getCurrentPlayTimeMS) | Get the time which has been played |
| [setPlayerLocalVolume](function.md#ThunderAudioFilePlayer::setPlayerLocalVolume) | Adjust volume of music file in mixed video being played locally. Please call this method in room |
| [setPlayerPublishVolume](function.md#ThunderAudioFilePlayer::setPlayerPublishVolume) | Adjust volume of music file in mixed video being played remotely. Please call this method in room |
| [getPlayerLocalVolume](function.md#ThunderAudioFilePlayer::getPlayerLocalVolume) | Get the local playing volume of the file                     |
| [getPlayerPublishVolume](function.md#ThunderAudioFilePlayer::getPlayerPublishVolume) | Get the remote playing volume of the file                    |
| [setLooping](function.md#ThunderAudioFilePlayer::setLooping) | Set times of loop playbacks |
| [setPlayerDelegate](function.md#ThunderAudioFilePlayer::setPlayerDelegate) | Set a player callback delegate |
| [enableSpectrum](function.md#ThunderAudioFilePlayer::enableSpectrum) | Enable/Disable spectrum |
| [enableVolumeIndication](function.md#ThunderAudioFilePlayer::enableVolumeIndication:interval) | Callback on turning on/off volume |
| [setMixStandard](function.md#ThunderAudioFilePlayer::setMixStandard) | Set whether the accompaniment is a standard stream for video mixing |
| [isMixStandard](function.md#ThunderAudioFilePlayer::isMixStandard) | Query whether the accompaniment is a standard stream for video mixing |
| [getCurrentSpectrum](function.md#ThunderAudioFilePlayer::getCurrentSpectrum:len) | Obtain spectrum information; value range [0-1] |

- Monitor callback via interface class [ThunderAudioFilePlayerDelegate](notification.md#ThunderAudioFilePlayerDelegate)

| Callback | Function |
| :---| :--- |
| [onAudioFileVolume](notification.md#ThunderAudioFilePlayerDelegate::onAudioFileVolume:volume:currentMs:totalMs) | Callback when playing volume |
| [onAudioFilePlayEnd](notification.md#ThunderAudioFilePlayerDelegate::onAudioFilePlayEnd) | Callback when end playing                         |
| [onAudioFilePlayError](notification.md#ThunderAudioFilePlayerDelegate::onAudioFilePlayError:errorCode) | Callback when audio file playing occur error      |
| [onAudioFilePlaying](notification.md#ThunderAudioFilePlayerDelegate::onAudioFilePlaying) | Callback when start playing                       |
| [onAudioFilePause](notification.md#ThunderAudioFilePlayerDelegate::onAudioFilePause) | Callback when pause playing                       |
| [onAudioFileResume](notification.md#ThunderAudioFilePlayerDelegate::onAudioFileResume) | Callback when resume playing                      |
| [onAudioFileStop](notification.md#ThunderAudioFilePlayerDelegate::onAudioFileStop) | Callback when stop playing                        |
| [onAudioFileSeekComplete](notification.md#ThunderAudioFilePlayerDelegate::onAudioFileSeekComplete:milliseconds) | Callback when the audio file seeking is completed |
| [onAudioFileStateChange](notification.md#ThunderAudioFilePlayerDelegate::onAudioFileStateChange:event:errorCode) | Report the status of the playing audio file |


## Sound change in reverb

| Method | Function |
| :---| :--- |
| [setVoiceChanger](function.md#ThunderEngine::setVoiceChanger:) | Set voice change mode |
| [setSoundEffect](function.md#ThunderEngine::setSoundEffect:) | Set different sound effects |
| [setEnableReverb](function.md#ThunderEngine::setEnableReverb:) | Enable/Disable reverb |
| [setReverbParam](function.md#ThunderEngine::setReverbParam:) | Set reverb parameters |
| [setEnableEqualizer](function.md#ThunderEngine::setEnableEqualizer:) | Enable/Disable equalizer |
| [setEqGains](function.md#ThunderEngine::setEqGains:) | Set equalizer parameters |
| [setEnableCompressor](function.md#ThunderEngine::setEnableCompressor:) | Enable/Disable compressor |
| [setCompressorParam](function.md#ThunderEngine::setCompressorParam:) | Set compressor parameters |
| [setEnableLimiter](function.md#ThunderEngine::setEnableLimiter:) | Enable/Disable pressure limiter |
| [setLimiterParam](function.md#ThunderEngine::setLimiterParam:) | Set pressure limiter parameters |

## Voice Positioning

| Method | Function |
| :---| :--- |
| [enableVoicePosition](function.md#ThunderEngine::enableVoicePosition:) | Enable/Disable voice stereo of remote users |
| [setRemoteUidVoicePosition](function.md#ThunderEngine::setRemoteUidVoicePosition:azimuth:gain:) | Set spatial location and volume of remote user's voice |

## Volume Prompt

| Method | Function |
| :---| :--- |
| [enableCaptureVolumeIndication](function.md#ThunderEngine::enableCaptureVolumeIndication:moreThanThd:lessThanThd:smooth:) | Callback on turning on/off microphone volume |
| [setAudioVolumeIndication](function.md#ThunderEngine::setAudioVolumeIndication:moreThanThd:lessThanThd:smooth:) | Callback on turning on/off user volume |

| Callback | Function |
| :---| :--- |
| [onCaptureVolumeIndication](notification.md#thunderEngine:onCaptureVolumeIndication:cpt:micVolume:) | Report the cpature volume                                |
| [onPlayVolumeIndication](notification.md#ThunderEventDelegate:onPlayVolumeIndication:totalVolume:) | Report which users are speaking and the speakers' volume |

## Voice Routing

| Method | Function |
| :---| :--- |
| [enableLoudspeaker](function.md#ThunderEngine::enableLoudspeaker:) | Enable a loudspeaker |
| [isLoudspeakerEnabled](function.md#ThunderEngine::isLoudspeakerEnabled) | Query whether the loudspeaker is enabled at |
| [setLoudSpeakerVolume](function.md#ThunderEngine::setLoudSpeakerVolume:) | Set loudspeaker volume |

## In-ear Monitor

| Method | Function |
| :---| :--- |
| [setEnableInEarMonitor](function.md#ThunderEngine::setEnableInEarMonitor:) | Enable/Disable ear monitor |


## Audio Device Management

| Callback | Function |
| :---| :--- |
| [onAudioCaptureStatus](notification.md#ThunderEventDelegate:thunderEngine:onAudioCaptureStatus:) | Report the status of the  audio capture device |

## Video Device Management

| Callback | Function |
| :---| :--- |
| [onVideoCaptureStatus](notification.md#ThunderEventDelegate:thunderEngine:onVideoCaptureStatus:) | Report the status of the video capture device |

## Media extra information

| Method | Function |
| :---| :--- |
| [setMediaExtraInfoDelegate](function.md#ThunderEngine::setMediaExtraInfoDelegate:) | Set callback delegate of media extra information [ThunderMediaExtraInfoDelegate](notification.md#ThunderMediaExtraInfoDelegate) |
| [sendMediaExtraInfo](function.md#ThunderEngine::sendMediaExtraInfo:) | Send media extra information (during audio/video streaming) |

- Monitor callback via interface type [ThunderMediaExtraInfoDelegate](notification.md#ThunderMediaExtraInfoDelegate)

| Callback | Function |
| :---| :--- |
| [onSendMediaExtraInfoFailedStatus](notification.md#ThunderMediaExtraInfoDelegate:onSendMediaExtraInfoFailedStatus:) | Callback when failure in sending media extra information     |
| [onRecvMediaExtraInfo](notification.md#ThunderMediaExtraInfoDelegate:onRecvMediaExtraInfo:ofUid:) | Callback when received media extra information               |
| [onRecvMixAudioInfo](notification.md#ThunderMediaExtraInfoDelegate:onRecvMixAudioInfo:ofUid:) | Callback when received extra information of mixed audio stream |
| [onRecvMixVideoInfo](notification.md#ThunderMediaExtraInfoDelegate:onRecvMixVideoInfo:ofUid:) | Callback when received extra information of mixed video stream |

## Raw Audio Data

| Method | Function |
| :---| :--- |
| [enableAudioDataIndication](function.md#ThunderEngine::enableAudioDataIndication:) | Enable/Disable data callback on audio playing |
| [enableAudioPlaySpectrum](function.md#ThunderEngine::enableAudioPlaySpectrum:) | Enable/Disable data callback on audio play spectrum |
| [setAudioPlaySpectrumInfo](function.md#ThunderEngine::setAudioPlaySpectrumInfo:notifyIntervalMS:) | Set audio playback spectrum parameters |
| [enableCapturePcmDataCallBack](function.md#ThunderEngine::enableCapturePcmDataCallBack:sampleRate:channel:) | Enable/Disable data callback on audio capture |
| [syncMediaPlayingProgress](function.md#ThunderEngine::syncMediaPlayingProgress:) | Synchronize play progress of external accompaniment video for mixed video synchronization. Audio accompaniment and video accompaniment cannot be supported at the same time. |
| [setRecordingAudioFrameParameters](function.md#ThunderEngine::setRecordingAudioFrameParameters:channel:mode:samplesPerCall:) | Set the mode for using raw audio recording data during callback onRecordAudioFrame |
| [setPlaybackAudioFrameParameters](function.md#ThunderEngine::setPlaybackAudioFrameParameters:channel:mode:samplesPerCall:) | Set the mode for using raw audio playback data during callback onPlaybackAudioFrame |


| Callback | Function |
| :---| :--- |
| [onAudioPlayData](notification.md#ThunderEventDelegate::thunderEngine:onAudioPlayData:duration:cpt:pts:data) | Callback on audio playback data |
| [onAudioPlaySpectrumData](notification.md#ThunderEventDelegate:thunderEngine:onAudioPlaySpectrumData:) | Callback on audio play spectrum data |

- Monitor callback via interface type [IAudioFrameObserver](notification.md#IAudioFrameObserver)

| Callback                                                         | Function                           |
| :----------------------------------------------------------- | :----------------------------- |
| [onRecordAudioFrame](notification.md#IAudioFrameObserver.onRecordAudioFrame) | Callback on raw audio capture data           |
| [onPlaybackAudioFrame](notification.md#IAudioFrameObserver.onPlaybackAudioFrame) | Callback on raw audio play data           |
| [onPlaybackAudioFrameBeforeMixing](notification.md#IAudioFrameObserver.onPlaybackAudioFrameBeforeMixing) | Callback of original data decoded by remote user can differentiate users through different uids |

## Raw Video Data

| Method | Function |
| :---| :--- |
| [registerVideoCaptureFrameObserver](function.md#ThunderEngine::registerVideoCaptureFrameObserver:) | Set the interface for callback on local video preprocessing |
| [registerVideoDecodeFrameObserver](function.md#ThunderEngine::registerVideoDecodeFrameObserver:uid) | Customize decoding picture rendering |

- Callback log via interface [ThunderVideoCaptureFrameObserver](notification.md#ThunderVideoCaptureFrameObserver)

| Callback | Function |
| :---| :--- |
| [needThunderVideoCaptureFrameDataType](notification.md#ThunderVideoCaptureFrameObserver::needThunderVideoCaptureFrameDataType) | Declare to SDK data in which format is to be used |
| [onVideoCaptureFrame](notification.md#ThunderVideoCaptureFrameObserver::onVideoCaptureFrame:PixelBuffer) | Receive a frame of data from capture for processing and return processed data |
| [onVideoCaptureFrame](notification.md#ThunderVideoCaptureFrameObserver::onVideoCaptureFrame:PixelBuffer:SourceTextureID:DestinationTextureID:TextureFormat:TextureTarget:TextureWidth:TextureHeight) | Return original texture parameters and target texture parameters |

- Callback log via interface [ThunderVideoDecodeFrameObserver](notification.md#ThunderVideoDecodeFrameObserver)

| Callback | Function |
| :---| :--- |
| [onVideoDecodeFrame](notification.md#ThunderVideoDecodeFrameObserver:onVideoDecodeFrame:pts:uid:) | Custom rendering of a decoded image is to cut out the decoded image of SDK for custom rendering of services |

## Custom Audio Capture

| Method | Function |
| :---| :--- |
| [enableCustomAudioSource](function.md#ThunderEngine::enableCustomAudioSource:channelsPerFrame:) | Enable external audio capture |
| [pushCustomAudioRawData](function.md#ThunderEngine::pushCustomAudioRawData:samples:timestamp:) | Push external audio stream |
| [pushCustomAudioSampleBuffer](function.md#ThunderEngine::pushCustomAudioSampleBuffer:) | Pushing an external audio frame |
| [disableCustomAudioSource](function.md#ThunderEngine::disableCustomAudioSource) | Disable external audio capture |

- Monitor callback via interface [ThunderExternalAudioProcessorDelegate](notification.md#ThunderExternalAudioProcessorDelegate)

| Callback | Function |
| :---| :--- |
| [audioCaptureStart](notification.md#ThunderExternalAudioProcessorDelegate::audioCaptureStart) | Audio capture starts |
| [audioCaptureData](notification.md#ThunderExternalAudioProcessorDelegate::audioCaptureData:data:len:sampleRate:channelCount:bitPerSample) | Callback on audio capture data |
| [audioCaptureStop](notification.md#ThunderExternalAudioProcessorDelegate::audioCaptureStop) | Audio capture stops |
| [audioRenderStart](notification.md#ThunderExternalAudioProcessorDelegate::audioRenderStart) | Audio rendering starts |
| [audioRenderData](notification.md#ThunderExternalAudioProcessorDelegate::audioRenderData:data:len:sampleRate:channelCount:bitPerSample) | Callback on audio rendering data |
| [audioRenderStop](notification.md#ThunderExternalAudioProcessorDelegate::audioRenderStop) | Audio rendering stops |

## Custom Video Capture

| Method | Function |
| :---| :--- |
| [setCustomVideoSource](function.md#ThunderEngine::setCustomVideoSource:) | Set external video capture source |

- Callback via interface [ThunderCustomVideoSourceProtocol](notification.md#ThunderCustomVideoSourceProtocol)

| Callback | Function |
| :---| :--- |
| [onInitialize](notification.md#ThunderCustomVideoSourceProtocol::onInitialize) | Initialize video source |
| [bufferType](notification.md#ThunderCustomVideoSourceProtocol::bufferType) | Obtain Buffer type |
| [onStart](notification.md#ThunderCustomVideoSourceProtocol::onStart) | Start video source |
| [onStop](notification.md#ThunderCustomVideoSourceProtocol::onStop) | Stop video source |
| [onDispose](notification.md#ThunderCustomVideoSourceProtocol::onDispose) | Dispose video source |

- Push external video data via interface [ThunderVideoFrameConsumer](function.md#ThunderVideoFrameConsumer)

| Callback | Function |
| :---| :--- |
| [consumePixelBuffer](function.md#ThunderVideoFrameConsumer::consumePixelBuffer:withTimestamp:rotation) | Interface for pushing raw video data |
| [consumeRawData](function.md#ThunderVideoFrameConsumer::consumeRawData:withTimestamp:format:size:rotation) | Interface for pushing raw video data |
| [consumeCMSampleBuffer](function.md#ThunderVideoFrameConsumer::consumeCMSampleBuffer) | Interface for pushing raw video data |

## Audio Self-rendering

| Method | Function |
| :---| :--- |
| [enableRenderPcmDataCallBack](function.md#ThunderEngine::enableRenderPcmDataCallBack:sampleRate:channel:) | Enable/Disable callback on audio rending data |

| Callback | Function |
| :---| :--- |
| [onAudioRenderPcmData](notification.md#ThunderEventDelegate::thunderEngine:onAudioRenderPcmData:duration:sampleRate:channel) | Callback audio rendering data |

## Video Self-rendering

| Method | Function |
| :---| :--- |
| [registerVideoDecodeFrameObserver](function.md#ThunderEngine::registerVideoDecodeFrameObserver:uid) | Set decoding data callback for video stream of a certain vid |

- Callback via interface [ThunderVideoDecodeFrameObserver](notification.md#ThunderVideoDecodeFrameObserver)

| Callback | Function |
| :---| :--- |
| [onVideoDecodeFrame](notification.md#ThunderVideoDecodeFrameObserver:onVideoDecodeFrame:pts:uid:) | Receive decoded frame data from decoder |

## Custom Messages

| Method | Function |
| :---| :--- |
| [sendUserAppMsgData](function.md#ThunderEngine::sendUserAppMsgData) | Sending developer's custom broadcast messages |

| Callback | Function |
| :---| :--- |
| [onRecvUserAppMsgData](notification.md##ThunderEventDelegate:onRecvUserAppMsgData:uid:) | Callback when received developer's custom broadcast messages |
| [onSendAppMsgDataFailedStatus](notification.md#ThunderEventDelegate::thunderEngine:onSendAppMsgDataFailedStatus) | Callback on failures in sending custom broadcast message of service |

## Log Management

| Method | Function |
| :---| :--- |
| [setLogFilePath](function.md#ThunderEngine::setLogFilePath) | Set directory for SDK to output log files. A directory with write permissions must be specified. |
| [setLogLevel](function.md#ThunderEngine::setLogLevel) | Set log levels |
| [setLogCallback](function.md#ThunderEngine::setLogCallback) | Set log callback. Once log callback is set, setLogFilePath is invalid |

- Callback log via interface [ThunderRtcLogDelegate](notification.md#ThunderRtcLogDelegate)

| Callback | Function |
| :---| :--- |
| [onThunderRtcLogWithLevel](notification.md#ThunderRtcLogDelegate::onThunderRtcLogWithLevel:message) | Callback on log information |

## Other methods

| Method | Function |
| :---| :--- |
| [enableWebSdkCompatibility](function.md#ThunderEngine::enableWebSdkCompatibility:) | Enable/Disable WebSDK compatibility |
