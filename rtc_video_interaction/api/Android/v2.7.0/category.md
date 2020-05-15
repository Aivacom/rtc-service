# Overview

AIVACOM offers various client SDKs, and has a flexible API combination. A global real-time communication network is connected trough SDK, to provide real-time audio/video communication services with stable and reliable quality for developers.

The AIVACOM SDK has a code of `Thunderbolt`, and a pure audio SDK for a mobile terminal has a code of `Thunder`.

- The [ThunderEngine](function.md#ThunderEngine) class offers all methods that could be called by an application.
- The [ThunderEventHandler](notification.md#ThunderEventHandler) abstract class is used to receive an event callback on [ThunderEngine](function.md#ThunderEngine) .

> Notes: Unless otherwise specified, all callback events in the document are monitored through the [ThunderEventHandler](notification.md#ThunderEventHandler) abstract class.

## Basic Method

| Method | Function |
| :---| :--- |
| [createEngine](function.md#ThunderEngine.createEngine) | Create and initialize a ThunderEngine instance object. |
| [createWithLoop](function.md#ThunderEngine.createWithLoop) | Create and initialize a ThunderEngine instance object, and specifying a running thread which the callback function of [ThunderEventHandler](notification.md#ThunderEventHandler) class will be running in it. |
| [destroyEngine](function.md#ThunderEngine.destroyEngine) | Destroy the ThunderEngine instance object. |
| [getVersion](function.md#ThunderEngine.getVersion) | Get SDK version information. |

## Room Management

| Method | Function |
| :---| :--- |
| [setArea](function.md#ThunderEngine.setArea) | Set user’s area |
| [setSceneId](function.md#ThunderEngine.setSceneId) | Set a scenario ID |
| [setMediaMode](function.md#ThunderEngine.setMediaMode) | Set media mode |
| [setRoomMode](function.md#ThunderEngine.setRoomMode) | Set room mode |
| [joinRoom](function.md#ThunderEngine.joinRoom) | Join a room |
| [leaveRoom](function.md#ThunderEngine.leaveRoom) | Leave a room |
| [updateToken](function.md#ThunderEngine.updateToken) | Update Token |

| Callback | Function |
| :---| :--- |
| [onJoinRoomSuccess](notification.md#ThunderEventHandler.onJoinRoomSuccess) | Callback when the local user joins a room |
| [onLeaveRoom](notification.md#ThunderEventHandler.onLeaveRoom) | Callback after leaving a room |
| [onSdkAuthResult](notification.md#ThunderEventHandler.onSdkAuthResult) | Report the SDK authentication result. For authentication details, refer to “User Authentication Description” on official website. |
| [onUserBanned](notification.md#ThunderEventHandler.onUserBanned) | Callback when user is banned |
| [onUserJoined](notification.md#ThunderEventHandler.onUserJoined) | Callback when user join the current room |
| [onUserOffline](notification.md#ThunderEventHandler.onUserOffline) | Callback when user leave the current room |
| [onRoomStats](notification.md#ThunderEventHandler.onRoomStats) | Report upstream and downstream traffic data every two seconds |
| [onBizAuthResult](notification.md#ThunderEventHandler.onBizAuthResult) | Report business authentication results |
| [onTokenWillExpire](notification.md#ThunderEventHandler.onTokenWillExpire) | Report token is about to expire |
| [onTokenRequested](notification.md#ThunderEventHandler.onTokenRequested) | Report token has expired |

## Audio Publishing

| Method | Function |
| :---| :--- |
| [setAudioConfig](function.md#ThunderEngine.setAudioConfig) | Set an audio mode |
| [setAudioSourceType](function.md#ThunderEngine.setAudioSourceType) | Set the audio source type |
| [setMicVolume](function.md#ThunderEngine.setMicVolume) | Set microphone volume |
| [stopLocalAudioStream](function.md#ThunderEngine.stopLocalAudioStream) | Audio Publishing (including enabling capture, encoding and stream publishing) |

| Callback | Function |
| :---| :--- |
| [onFirstLocalAudioFrameSent](notification.md#ThunderEventHandler.onFirstLocalAudioFrameSent) | Callback when first local audio frame sent successfully |
| [onLocalAudioStats](notification.md#ThunderEventHandler.onLocalAudioStats) | Report the statistics of the local audio stream |

## Audio Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteAudioStreams](function.md#ThunderEngine.stopAllRemoteAudioStreams) | Stop/Resume receiving all remote audio streams |
| [stopRemoteAudioStream](function.md#ThunderEngine.stopRemoteAudioStream) | Stop/Resume receiving audio stream of a specified user |
| [setRemoteAudioStreamsVolume](function.md#ThunderEngine.setRemoteAudioStreamsVolume) | Set the volume of the specified user audio stream |

| Callback | Function |
| :---| :--- |
| [onRemoteAudioStopped](notification.md#ThunderEventHandler.onRemoteAudioStopped) | Callback when the remote user's audio stream starts or stops |
| [onRemoteAudioStatsOfUid](notification.md#ThunderEventHandler.onRemoteAudioStatsOfUid) | Report status message of remote audio stream |

## Video Publishing

| Method | Function |
| :---| :--- |
| [setVideoEncoderConfig](function.md#ThunderEngine.setVideoEncoderConfig) | Set video encoding configuration |
| [setLocalVideoCanvas](function.md#ThunderEngine.setLocalVideoCanvas) | Set the rendering canvas of a local video |
| [enableLocalVideoCapture](function.md#ThunderEngine.enableLocalVideoCapture) | Enable/Disable local video capture |
| [startVideoPreview](function.md#ThunderEngine.startVideoPreview) | Start video preview of local camera |
| [stopVideoPreview](function.md#ThunderEngine.stopVideoPreview) | Stop video preview of a local camera |
| [setLocalCanvasScaleMode](function.md#ThunderEngine.setLocalCanvasScaleMode) | Set the scale mode of the local video stream on the canvas |
| [setLocalVideoMirrorMode](function.md#ThunderEngine.setLocalVideoMirrorMode) | Set local video mirror mode |
| [stopLocalVideoStream](function.md#ThunderEngine.stopLocalVideoStream) | Start/Stop the sending of a local video (included encoding) |

| Callback | Function |
| :---| :--- |
| [onFirstLocalVideoFrameSent](notification.md#ThunderEventHandler.onFirstLocalVideoFrameSent) | Callback when first local video frame sent successfully |
| [onLocalVideoStats](notification.md#ThunderEventHandler.onLocalVideoStats) | Report statistics of local video stream |

## Video Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteVideoStreams](function.md#ThunderEngine.stopAllRemoteVideoStreams) | Stop/Resume receiving all remote video streams |
| [stopRemoteVideoStream](function.md#ThunderEngine.stopRemoteVideoStream) | Stop/Resume receiving video stream of a specified user |
| [setRemoteCanvasScaleMode](function.md#ThunderEngine.setRemoteCanvasScaleMode) | Set the scale mode of the remote video stream on the canvas |
| [setMultiVideoViewLayout](function.md#ThunderEngine.setMultiVideoViewLayout) | Set the layout parameters of the multi videos on the view |
| [setRemoteVideoCanvas](function.md#ThunderEngine.setRemoteVideoCanvas) | Set the rendering view of the remote video |
| [setRemotePlayType](function.md#ThunderEngine.setRemotePlayType) | Sets the type of remote user's render view |

| Callback | Function |
| :---| :--- |
| [onRemoteVideoStopped](notification.md#ThunderEventHandler.onRemoteVideoStopped) | Callback when the remote user's video stream starts or stops |
| [onRemoteVideoStatsOfUid](notification.md#ThunderEventHandler.onRemoteVideoStatsOfUid) | Report status message of remote video stream |
| [onRemoteVideoPlay](notification.md#ThunderEventHandler.onRemoteVideoPlay) | Callback when displaying the first frame of remote video |
| [onVideoSizeChanged](notification.md#ThunderEventHandler.onVideoSizeChanged) | Callback when the resolution of local or remote video changes |

## Network status

| Callback | Function |
| :---| :--- |
| [onNetworkQuality](notification.md#ThunderEventHandler.onNetworkQuality) | Report the uplink and downlink network quality of each user |
| [onNetworkTypeChanged](notification.md#ThunderEventHandler.onNetworkTypeChanged) | Callback when the network type changes |
| [onConnectionStatus](notification.md#ThunderEventHandler.onConnectionStatus) | Report the connection status with the server |
| [onConnectionLost](notification.md#ThunderEventHandler.onConnectionLost) | Callback when losing connection with server |

## Publishing Test

N/A

## Video mixing and stream publishing

| Method | Function |
| :---| :--- |
| [setLiveTranscodingTask](function.md#ThunderEngine.setLiveTranscodingTask) | Add or update transcoding task |
| [removeLiveTranscodingTask](function.md#ThunderEngine.removeLiveTranscodingTask) | Remove a transcoding task |
| [addPublishTranscodingStreamUrl](function.md#ThunderEngine.addPublishTranscodingStreamUrl) | Add a pushing address of transcoding stream |
| [removePublishTranscodingStreamUrl](function.md#ThunderEngine.removePublishTranscodingStreamUrl) | Remove the pushing address of the transcoding stream |
| [addPublishOriginStreamUrl](function.md#ThunderEngine.addPublishOriginStreamUrl) | Add a pushing address of source stream  |
| [removePublishOriginStreamUrl](function.md#ThunderEngine.removePublishOriginStreamUrl) | Remove the pushing address of source stream |
| [enableMixVideoExtraInfo](function.md#ThunderEngine.enableMixVideoExtraInfo) | Enable video mixing with extra information |

| Callback | Function |
| :---| :--- |
| [onPublishStreamToCDNStatus](notification.md#ThunderEventHandler.onPublishStreamToCDNStatus) | Report the result of pushing stream to the CDN |

## Audio Recording

| Method | Function |
| :---| :--- |
| [startAudioSaver](function.md#ThunderEngine.startAudioSaver) | Start saving audio data as aac format file |
| [stopAudioSaver](function.md#ThunderEngine.stopAudioSaver) | Stop saving audio data as aac format file |

## Cross-room subscription

| Method | Function |
| :---| :--- |
| [addSubscribe](function.md#ThunderEngine.addSubscribe) | Subscribe stream of specified user across the room |
| [removeSubscribe](function.md#ThunderEngine.removeSubscribe) | Remove the subscription of stream of specified user across the room |

## Camera Management

| Method | Function |
| :---| :--- |
| [switchFrontCamera](function.md#ThunderEngine.switchFrontCamera) | Switch front/rear camera |
| [setVideoCaptureOrientation](function.md#ThunderEngine.setVideoCaptureOrientation) | Set the capture orientation of camera video ( landscape / portrait ) |

## Screen Sharing

N/A

## Real-time Watermark

| Method | Function |
| :---| :--- |
| [setVideoWatermark](function.md#ThunderEngine.setVideoWatermark) | Set watermark of local video |

## Video Dual Stream

N/A

## Audio Player

| Method | Function |
| :---| :--- |
| [createAudioFilePlayer](function.md#ThunderEngine.createAudioFilePlayer) | Create an instance object of an audio file player [ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) |
| [destroyAudioFilePlayer](function.md#ThunderEngine.destroyAudioFilePlayer) | Destroy an instance object of an audio file player [ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) |

- Method in a [ThunderAudioFilePlayer](function.md#ThunderAudioFilePlayer) class

| Method | Function |
| :---| :--- |
| [open](function.md#ThunderAudioFilePlayer.open) | Open an accompaniment file |
| [close](function.md#ThunderAudioFilePlayer.close) | Close an accompaniment file |
| [play](function.md#ThunderAudioFilePlayer.play) | Start playing |
| [Stop](function.md#ThunderAudioFilePlayer.stop) | Stop playing |
| [pause](function.md#ThunderAudioFilePlayer.pause) | Pause |
| [resume](function.md#ThunderAudioFilePlayer.resume) | Resume |
| [seek](function.md#ThunderAudioFilePlayer.seek) | Jump to specified time for playing |
| [getTotalPlayTimeMS](function.md#ThunderAudioFilePlayer.getTotalPlayTimeMS) | Get total play time of the file |
| [getCurrentPlayTimeMS](function.md#ThunderAudioFilePlayer.getCurrentPlayTimeMS) | Get current play time of the file |
| [setPlayVolume](function.md#ThunderAudioFilePlayer.setPlayVolume) | Set the playing volume of current file |
| [setPlayerLocalVolume](function.md#ThunderAudioFilePlayer.setPlayerLocalVolume) | Set the local playing volume of the file |
| [setPlayerPublishVolume](function.md#ThunderAudioFilePlayer.setPlayerPublishVolume) | Set the remote playing volume of the file |
| [getPlayerLocalVolume](function.md#ThunderAudioFilePlayer.getPlayerLocalVolume) | Get the local playing volume of the file |
| [getPlayerPublishVolume](function.md#ThunderAudioFilePlayer.getPlayerPublishVolume) | Get the remote playing volume of the file |
| [getAudioTrackCount](function.md#ThunderAudioFilePlayer.getAudioTrackCount) | Get the number of audio tracks |
| [selectAudioTrack](function.md#ThunderAudioFilePlayer.selectAudioTrack) | Select an audio track |
| [setSemitone](function.md#ThunderAudioFilePlayer.setSemitone) | Set the tone for audio playing |
| [setLooping](function.md#ThunderAudioFilePlayer.setLooping) | Set times of loop playbacks |
| [enablePublish](function.md#ThunderAudioFilePlayer.enablePublish) | Enable use current audio file as accompaniment in live |
| [setPlayerNotify](function.md#ThunderAudioFilePlayer.setPlayerNotify) | Set a playing callback interface [ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback) |
| [enableVolumeIndication](function.md#ThunderAudioFilePlayer.enableVolumeIndication) | Enable the [ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileVolume](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileVolume) callback to report the volume of playing audio file |
| [setMixStandard](function.md#ThunderAudioFilePlayer.setMixStandard) | Set whether the accompaniment is a standard stream for video mixing |
| [isMixStandard](function.md#ThunderAudioFilePlayer.isMixStandard) | Query whether the accompaniment is a standard stream for video mixing |

- Monitor the callback through [ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback) interface.

| Callback | Function |
| :---| :--- |
| [onAudioFilePlayError](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayError) | Callback when audio file playing occur error |
| [onAudioFileVolume](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileVolume) | Report the volume of the playing audio file |
| [onAudioFileSeekComplete](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileSeekComplete) | Callback when the audio file seeking is completed |
| [onAudioFilePlaying](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlaying) | Callback when start playing |
| [onAudioFilePause](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePause) | Callback when pause playing |
| [onAudioFileResume](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileResume) | Callback when resume playing |
| [onAudioFileStop](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFileStop) | Callback when stop playing |
| [onAudioFilePlayEnd](notification.md#ThunderAudioFilePlayer.IThunderAudioFilePlayerCallback.onAudioFilePlayEnd) | Callback when end playing |

## Voice Change and Reverb

| Method | Function |
| :---| :--- |
| [setVoiceChanger](function.md#ThunderEngine.setVoiceChanger) | Set voice change mode |
| [setSoundEffect](function.md#ThunderEngine.setSoundEffect) | Set sound effect mode |
| [setEnableEqualizer](function.md#ThunderEngine.setEnableEqualizer) | Enable/Disable local voice equalizer |
| [setEqGains](function.md#ThunderEngine.setEqGains) | Set voice equalizer parameters |
| [setEnableReverb](function.md#ThunderEngine.setEnableReverb) | Enable/Disable local voice reverberation |
| [setReverbExParameter](function.md#ThunderEngine.setReverbExParameter) | Set local voice reverberation parameters |
| [setEnableCompressor](function.md#ThunderEngine.setEnableCompressor) | Enable/Disable audio compressor |
| [setCompressorParam](function.md#ThunderEngine.setCompressorParam) | Set audio compressor parameters |
| [setEnableLimiter](function.md#ThunderEngine.setEnableLimiter) | Enable/Disable limiter |
| [setLimiterParam](function.md#ThunderEngine.setLimiterParam) | Set limiter parameters |

## Voice Positioning

| Method | Function |
| :---| :--- |
| [enableVoicePosition](function.md#ThunderEngine.enableVoicePosition) | Enable/Disable voice stereo of remote users |
| [setRemoteUidVoicePosition](function.md#ThunderEngine.setRemoteUidVoicePosition) | Set spatial location and volume of remote user's voice |

## Volume Prompt

| Method | Function |
| :---| :--- |
| [enableCaptureVolumeIndication](function.md#ThunderEngine.enableCaptureVolumeIndication) | Enable/Disable capture volume callback |
| [setAudioVolumeIndication](function.md#ThunderEngine.setAudioVolumeIndication) | Enable/Disable speaker volume callback |

| Callback | Function |
| :---| :--- |
| [onCaptureVolumeIndication](notification.md#ThunderEventHandler.onCaptureVolumeIndication) | Report the cpature volume |
| [onPlayVolumeIndication](notification.md#ThunderEventHandler.onPlayVolumeIndication) | Report which users are speaking and the speakers' volume |

## Voice Routing

| Method | Function |
| :---| :--- |
| [isLoudspeakerEnabled](function.md#ThunderEngine.isLoudspeakerEnabled) | Query whether the loudspeaker is enabled at |
| [enableLoudspeaker](function.md#ThunderEngine.enableLoudspeaker) | Enable a loudspeaker |
| [setLoudSpeakerVolume](function.md#ThunderEngine.setLoudSpeakerVolume) | Set loudspeaker volume |

## In-ear Monitor

| Method | Function |
| :---| :--- |
| [setEnableInEarMonitor](function.md#ThunderEngine.setEnableInEarMonitor) | Enable/Disable in-ear monitor |

## Audio Device Management

| Callback | Function |
| :---| :--- |
| [onAudioCaptureStatus](notification.md#ThunderEventHandler.onAudioCaptureStatus) | Callback when the audio device capture status changes |

## Video Device Management

| Callback | Function |
| :---| :--- |
| [onVideoCaptureStatus](notification.md#ThunderEventHandler.onVideoCaptureStatus) | Callback when the video device capture status changes |

## Media extra information

| Method | Function |
| :---| :--- |
| [setMediaExtraInfoCallback](function.md#ThunderEngine.setMediaExtraInfoCallback) | Set callback monitoring of media extra information [IThunderMediaExtraInfoCallback](notification.md#IThunderMediaExtraInfoCallback) |
| [sendMediaExtraInfo](function.md#ThunderEngine.sendMediaExtraInfo) | Send media extra information |

- Monitor the callback through [IThunderMediaExtraInfoCallback](notification.md#IThunderMediaExtraInfoCallback) interface

| Callback | Function |
| :---| :--- |
| [onSendMediaExtraInfoFailedStatus](notification.md#IThunderMediaExtraInfoCallback.onSendMediaExtraInfoFailedStatus) | Callback when failure in sending media extra information |
| [onRecvMediaExtraInfo](notification.md#IThunderMediaExtraInfoCallback.onRecvMediaExtraInfo) | Callback when received media extra information |
| [onRecvMixAudioInfo](notification.md#IThunderMediaExtraInfoCallback.onRecvMixAudioInfo) | Callback when received extra information of mixed audio stream |
| [onRecvMixVideoInfo](notification.md#IThunderMediaExtraInfoCallback.onRecvMixVideoInfo) | Callback when received extra information of mixed video stream |

## Raw Audio Data

| Method | Function |
| :---| :--- |
| [enableAudioPlaySpectrum](function.md#ThunderEngine.enableAudioPlaySpectrum) | Enable/Disable data callback of audio play spectrum [onAudioPlaySpectrumData](notification.md#ThunderEventHandler.onAudioPlaySpectrumData) |
| [setAudioPlaySpectrumInfo](function.md#ThunderEngine.setAudioPlaySpectrumInfo) | Set callback information of audio play spectrum data |
| [enableAudioDataIndication](function.md#ThunderEngine.enableAudioDataIndication) | Enable/Disable data callback of audio playback [onAudioPlayData](notification.md#ThunderEventHandler.onAudioPlayData) |
| [setRecordingAudioFrameParameters](function.md#ThunderEngine.setRecordingAudioFrameParameters) | Set a format for callback on captured raw data |
| [setPlaybackAudioFrameParameters](function.md#ThunderEngine.setPlaybackAudioFrameParameters) | Set a format for callback on play data |
| [registerAudioFrameObserver](function.md#ThunderEngine.registerAudioFrameObserver) | Register an audio observer object [IAudioFrameObserver](notification.md#IAudioFrameObserver) |

| Callback | Function |
| :---| :--- |
| [onAudioPlaySpectrumData](notification.md#ThunderEventHandler.onAudioPlaySpectrumData) | Report the audio playback spectrum data |
| [onAudioPlayData](notification.md#ThunderEventHandler.onAudioPlayData) | Report the audio playback data |

- Monitor the callback through [IAudioFrameObserver](notification.md#IAudioFrameObserver) interface.

| Callback | Function |
| :---| :--- |
| [onRecordAudioFrame](notification.md#IAudioFrameObserver.onRecordAudioFrame) | Report the raw audio capture data |
| [onPlaybackAudioFrame](notification.md#IAudioFrameObserver.onPlaybackAudioFrame) | Report the raw audio play data |
| [onPlaybackAudioFrameBeforeMixing](notification.md#IAudioFrameObserver.onPlaybackAudioFrameBeforeMixing) | Report the raw decoded audio data of remote user |

## Raw Video Data

| Method | Function |
| :---| :--- |
| [registerVideoCaptureTextureObserver](function.md#ThunderEngine.registerVideoCaptureTextureObserver) | Registering a video capture texture observer for beauty processing [IGPUProcess](notification.md#IGPUProcess) |
| [registerVideoCaptureFrameObserver](function.md#ThunderEngine.registerVideoCaptureFrameObserver) | Registering a video capture frame observer [IVideoCaptureObserver](notification.md#IVideoCaptureObserver) |
| [registerVideoDecodeFrameObserver](function.md#ThunderEngine.registerVideoDecodeFrameObserver) | Registering a decoded YUV (I420) video data observer [IVideoDecodeObserver](notification.md#IVideoDecodeObserver) |

- Monitor the callback through [IGPUProcess](notification.md#IGPUProcess) interface.

| Callback | Function |
| :---| :--- |
| [onInit](notification.md#IGPUProcess.onInit) | Allowing users to use third-party special effects |
| [onDestroy](notification.md#IGPUProcess.onDestroy) | Destroying resources of special effects |
| [onDraw](notification.md#IGPUProcess.onDraw) | Process every frame |
| [onOutputSizeChanged](notification.md#IGPUProcess.onOutputSizeChanged) | Callback when the texture size update |

- Monitor the callback through [IVideoCaptureObserver](notification.md#IVideoCaptureObserver) interface

| Callback | Function |
| :---| :--- |
| [onCaptureVideoFrame](notification.md#IVideoCaptureObserver.onCaptureVideoFrame) | Report the capture video frame data |

- Monitor the callback through [IVideoDecodeObserver](notification.md#IVideoDecodeObserver) interface.

| Callback | Function |
| :---| :--- |
| [onVideoDecodeFrame](notification.md#IVideoDecodeObserver.onVideoDecodeFrame) | Report the decoded YUV (I420) video data |

## Custom Audio Capture

| Method | Function |
| :---| :--- |
| [setCustomAudioSource](function.md#ThunderEngine.setCustomAudioSource) | Set parameters of external audio source |
| [pushCustomAudioFrame](function.md#ThunderEngine.pushCustomAudioFrame) | Pushing an external audio frame |

## Custom Video Capture

| Method | Function |
| :---| :--- |
| [setCustomVideoSource](function.md#ThunderEngine.setCustomVideoSource) | Set customized video source |

- Monitor the callback through [ThunderCustomVideoSource](notification.md#ThunderCustomVideoSource) interface.

| Callback | Function |
| :--- | :--- |
| [onInitialize](notification.md#ThunderCustomVideoSource.onInitialize) | Initialize the video source |
| [onStart](notification.md#ThunderCustomVideoSource.onStart) | Start the video source   |
| [onStop](notification.md#ThunderCustomVideoSource.onStop) | Stop the video source   |
| [onDispose](notification.md#ThunderCustomVideoSource.onDispose) | Release the video source |

- Push external video data through [ThunderVideoFrameConsumer](notification.md#ThunderVideoFrameConsumer) interface.

| Callback | Function |
| :--- | :--- |
| [consumeByteArrayFrame](notification.md#ThunderVideoFrameConsumer.consumeByteArrayFrame) | Method for pushing external raw video data |

## Custom Messages

| Method | Function |
| :---| :--- |
| [sendUserAppMsgData](function.md#ThunderEngine.sendUserAppMsgData) | Sending developer's custom broadcast messages |

| Callback | Function |
| :---| :--- |
| [onRecvUserAppMsgData](notification.md#ThunderEventHandler.onRecvUserAppMsgData) | Callback when received developer's custom broadcast messages |
| [onSendAppMsgDataFailedStatus](notification.md#ThunderEventHandler.onSendAppMsgDataFailedStatus) | Callback when failure in sending deveploper's custom broadcast messages |

## Log Management

| Method | Function |
| :---| :--- |
| [setLogFilePath](function.md#ThunderEngine.setLogFilePath) | Set directory for SDK to output log files |
| [setLogLevel](function.md#ThunderEngine.setLogLevel) | Set log levels |
| [setLogCallback](function.md#ThunderEngine.setLogCallback) | Set log callback interface [IThunderLogCallback](notification.md#IThunderLogCallback) |

- Monitoring the callback through [IThunderLogCallback](notification.md#IThunderLogCallback) interface

| Callback | Function |
| :---| :--- |
| [onThunderLogWithLevel](notification.md#IThunderLogCallback.onThunderLogWithLevel) | Report the log information |

## Other methods

| Method | Function |
| :---| :--- |
| [enableWebSdkCompatibility](function.md#ThunderEngine.enableWebSdkCompatibility) | Enable/Disable WebSDK compatibility |
