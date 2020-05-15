# Overview

AIVACOM provides various client SDKs with APIs that can be flexibly combined. SDK-based connection to globally-deployed real-time communication networks guarantees stable and reliable real-time audio/video communication services.

The Aivacom SDK has a code of `Thunderbolt`, and a pure audio SDK for a mobile terminal has a code of `Thunder`.

- [The IThunderEngine](function.md#IThunderEngine) interface class provides all functions that can be called by application.
- [The IThunderEventHandler](notification.md#IThunderEventHandler) interface class is used to send callbacks to the application.

> Note: Unless otherwise stated, event callbacks in this document are monitored through the [IThunderEventHandler](notification.md#IThunderEventHandler) interface.

## Basic Method

| Method | Function |
| :---| :--- |
| [createEngine](function.md#IThunderEngine::createEngine) | Create the IThunderEngine instance |
| [initialize](function.md#IThunderEngine::initialize) | Initialize the IThunderEngine object |
| [destroyEngine](function.md#IThunderEngine::destroyEngine) | Destroy the IThunderEngine object |

## Room Management

| Method | Function |
| :---| :--- |
| [setArea](function.md#IThunderEngine::setArea) | Set user’s area |
| [setMediaMode](function.md#IThunderEngine::setMediaMode) | Set media mode |
| [setRoomMode](function.md#IThunderEngine::setRoomMode) | Set room mode |
| [joinRoom](function.md#IThunderEngine::joinRoom) | Join a room |
| [leaveRoom](function.md#IThunderEngine::leaveRoom) | Leave a room |
| [updateToken](function.md#IThunderEngine::updateToken) | Update Token |

| Callback | Function |
| :---| :--- |
| [onJoinRoomSuccess](notification.md#IThunderEventHandler::onJoinRoomSuccess) | Callback when the local user joins a room |
| [onLeaveRoom](notification.md#IThunderEventHandler::onLeaveRoom) | Callback after the local user leaves a room |
| [onSdkAuthResult](notification.md#IThunderEventHandler::onSdkAuthResult) | Callback on SDK authentication result. For authentication details, refer to “User Authentication Description” on official website. |
| [onUserBanned](notification.md#IThunderEventHandler::onUserBanned) | Callback when a user is banned |
| [onUserJoined](notification.md#IThunderEventHandler::onUserJoined) | Callback when a remote user joins the current room |
| [onUserOffline](notification.md#IThunderEventHandler::onUserOffline) | Callback on user leaving a current room |
| [onRoomStats](notification.md#IThunderEventHandler::onRoomStats) | Callback on uplink/downlink traffic (periodic callback at an interval of 2s) |
| [onBizAuthResult](notification.md#IThunderEventHandler::onBizAuthResult) | Callback on service authentication results |
| [onTokenWillExpire](notification.md#IThunderEventHandler::onTokenWillExpire) | Callback on token to be expired |
| [onTokenRequest](notification.md#IThunderEventHandler::onTokenRequest) | Callback when token expires |

## Audio Publishing

| Method | Function |
| :---| :--- |
| [setAudioConfig](function.md#IThunderEngine::setAudioConfig) | Sets audio parameters and application scenarios. |
| [adjustRecordingSignalVolume](function.md#IThunderEngine::adjustRecordingSignalVolume) | Set microphone volume |
| [stopLocalAudioStream](function.md#IThunderEngine::stopLocalAudioStream) | Stop broadcasting/Publishing audio (including starting collection, encoding, and stream publishing) |
| [enableLoopbackRecording](function.md#IThunderEngine::enableLoopbackRecording) | Enable/Disable graphic card capture. |
| [setAudioSourceType](function.md#IThunderEngine::setAudioSourceType) | Set audio publishing type |

| Callback | Function |
| :---| :--- |
| [onFirstLocalAudioFrameSent](notification.md#IThunderEventHandler::onFirstLocalVideoFrameSent) | Callback on first local audio frame sent successfully |
| [onLocalAudioStats](notification.md#IThunderEventHandler::onLocalAudioStats) | Reporting audio streaming sending statistics in every 2s |

## Audio Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteAudioStreams](function.md#IThunderEngine::stopAllRemoteAudioStreams) | Stop/Receive all audio streaming data |
| [stopRemoteAudioStream](function.md#IThunderEngine::stopRemoteAudioStream) | Stop/Receive audio streaming data of a specified user |
| [adjustPlaybackSignalVolume](function.md#IThunderEngine::adjustPlaybackSignalVolume) | Set local playing volume |

| Callback | Function |
| :---| :--- |
| [onRemoteAudioStopped](notification.md#IThunderEventHandler::onRemoteAudioStopped) | Callback when a remote user stops broadcasting/publishing audio streams |
| [onRemoteAudioStatsOfUid](notification.md#IThunderEventHandler::onRemoteAudioStatsOfUid) | Reporting remote audio streams statistics by user in every 2s |

## Video Publishing

| Method | Function |
| :---| :--- |
| [setVideoEncoderConfig](function.md#IThunderEngine::setVideoEncoderConfig) | Set video encoding configuration |
| [enableLocalVideoCapture](function.md#IThunderEngine::enableLocalVideoCapture) | Enable/Disable local video capture |
| [setLocalVideoCanvas](function.md#IThunderEngine::setLocalVideoCanvas) | Set the rendering canvas of a local video |
| [startVideoPreview](function.md#IThunderEngine::startVideoPreview) | Enable video preview |
| [stopVideoPreview](function.md#IThunderEngine::stopVideoPreview) | Disable video preview |
| [setLocalCanvasScaleMode](function.md#IThunderEngine::setLocalCanvasScaleMode) | Set a scaling mode of a local canvas |
| [setLocalVideoMirrorMode](function.md#IThunderEngine::setLocalVideoMirrorMode) | Set local video mirror mode |
| [stopLocalVideoStream](function.md#IThunderEngine::stopLocalVideoStream) | Stop/Start the sending of a local video streaming (codes included) |

| Callback | Function |
| :---| :--- |
| [onFirstLocalVideoFrameSent](notification.md#IThunderEventHandler::onFirstLocalVideoFrameSent) | Callback when the first video frame is successfully sent |
| [onLocalVideoStats](notification.md#IThunderEventHandler::onLocalVideoStats) | Callback every 2s, reporting video streaming sending statistics |

## Video Subscription

| Method | Function |
| :---| :--- |
| [stopAllRemoteVideoStreams](function.md#IThunderEngine::stopAllRemoteVideoStreams) | Stop/Receive all video stream data |
| [stopRemoteVideoStream](function.md#IThunderEngine::stopRemoteVideoStream) | Stop/Receive video stream data of a specified user |
| [setRemoteCanvasScaleMode](function.md#IThunderEngine::setRemoteCanvasScaleMode) | Set a scaling mode of a remote canvas |
| [setRemoteVideoCanvas](function.md#IThunderEngine::setRemoteVideoCanvas) | Set the rendering view of remote video stream. |

| Callback | Function |
| :---| :--- |
| [onRemoteVideoStopped](notification.md#IThunderEventHandler::onRemoteVideoStopped) | Callback on stopping/publishing user’s video stream |
| [onRemoteVideoStatsOfUid](notification.md#IThunderEventHandler::onRemoteVideoStatsOfUid) | Reporting remote video streams statistics by user in every 2s |
| [onRemoteVideoPlay](notification.md#IThunderEventHandler::onRemoteVideoPlay) | Callback on displayed first remote video frame |
| [onVideoSizeChanged](notification.md#IThunderEventHandler::onVideoSizeChanged) | Callback on change in local/remote video resolution |

## Network status

| Callback | Function |
| :---| :--- |
| [onNetworkQuality](notification.md#IThunderEventHandler::onNetworkQuality) | Reporting the network statistics in every 2s|
| [onNetworkTypeChanged](notification.md#IThunderEventHandler::onNetworkTypeChanged) | Callback on network status change |
| [onConnectionStatus](notification.md#IThunderEventHandler::onConnectionStatus) | Callback on server network connection status change |
| [onConnectionLost](notification.md#IThunderEventHandler::onConnectionLost) | Callback on lost network connection with a server |

## Publishing detection

N/A

## Video mixing and stream publishing

| Method | Function |
| :---| :--- |
| [setLiveTranscodingTask](function.md#IThunderEngine::setLiveTranscodingTask) | Add/update transcoding task |
| [removeLiveTranscodingTask](function.md#IThunderEngine::removeLiveTranscodingTask) | Remove a transcoding task |
| [removePublishTranscodingStreamUrl](function.md#IThunderEngine::removePublishTranscodingStreamUrl) | Remove a stream publishing address of a transcoding stream |
| [addPublishTranscodingStreamUrl](function.md#IThunderEngine::addPublishTranscodingStreamUrl) | Add a stream publishing address of a transcoding stream |
| [addPublishOriginStreamUrl](function.md#IThunderEngine::addPublishOriginStreamUrl) | Add the source stream publishing address |
| [removePublishOriginStreamUrl](function.md#IThunderEngine::removePublishOriginStreamUrl) | Remove the source stream publishing address |
| [enableMixVideoExtraInfo](function.md#IThunderEngine::enableMixVideoExtraInfo) | Enable video mixing with media extra information |

| Callback | Function |
| :---| :--- |
| [onPublishStreamToCDNStatus](notification.md#IThunderEventHandler::onPublishStreamToCDNStatus) | Reporting CDN stream publishing result |

## Audio Recording

| Method | Function |
| :---| :--- |
| [startAudioRecording](function.md#IThunderEngine::startAudioRecording) | Start audio recording |
| [stopAudioRecording](function.md#IThunderEngine::stopAudioRecording) | Stop audio recording |

## Cross-room Microphone Connection

| Method | Function |
| :---| :--- |
| [addSubscribe](function.md#IThunderEngine::addSubscribe) | Subscribe a stream of the specified user in other rooms |
| [removeSubscribe](function.md#IThunderEngine::removeSubscribe) | UnSubscribe a stream stream of the specified user in other rooms |

## Camera Management

N/A

## Screen Sharing

| Method | Function |
| :---| :--- |
| [startScreenCaptureForHwnd](function.md#IThunderEngine::startScreenCaptureForHwnd) | Start screen capturing specific window |
| [startScreenCaptureForScreen](function.md#IThunderEngine::startScreenCaptureForScreen) | Start screen capturing a specific region on desktop |
| [updateScreenCaptureRect](function.md#IThunderEngine::updateScreenCaptureRect) | Update the region of screen capturing |
| [stopScreenCapture](function.md#IThunderEngine::stopScreenCapture) | Stop screen capturing the desktop or window |
| [pauseScreenCapture](function.md#IThunderEngine::pauseScreenCapture) | Pause screen capturing the desktop or window |
| [resumeScreenCapture](function.md#IThunderEngine::resumeScreenCapture) | Resume screen capturing the desktop or window |

## Real-time Watermark

| Method | Function |
| :---| :--- |
| [setVideoWatermark](function.md#IThunderEngine::setVideoWatermark) | Set video watermark |
| [removeVideoWatermarks](function.md#IThunderEngine::removeVideoWatermarks) | Remove video watermark |

## Video Dual Stream

N/A

## Audio Player

| Method | Function |
| :---| :--- |
| [createThunderAudioPlayer](function.md#IThunderEngine::createThunderAudioPlayer) | Create audio file player object[IThunderAudioPlayer](function.md#IThunderAudioPlayer) |
| [destroyThunderAudioPlayer](function.md#IThunderEngine::destroyThunderAudioPlayer) | Destroy the audio file player object[IThunderAudioPlayer](function.md#IThunderAudioPlayer) |

- [Methods in the IThunderAudioPlayer](function.md#IThunderAudioPlayer) interface class

| Method | Function |
| :---| :--- |
| [open](function.md#IThunderAudioPlayer::open) | Open an file for accompaniment |
| [close](function.md#IThunderAudioPlayer::close) | Close an file for accompaniment|
| [play](function.md#IThunderAudioPlayer::play) | Start playing the file |
| [Stop](function.md#IThunderAudioPlayer::stop) | Stop playing the file |
| [pause](function.md#IThunderAudioPlayer::pause) | Pause playing the file |
| [resume](function.md#IThunderAudioPlayer::resume) | Resume playing the file |
| [seek](function.md#IThunderAudioPlayer::seek) | Seek time for playing the file |
| [getTotalPlayTimeMS](function.md#IThunderAudioPlayer::getTotalPlayTimeMS) | Obtain the total duration of the audio file |
| [getCurrentPlayTimeMS](function.md#IThunderAudioPlayer::getCurrentPlayTimeMS) | Obtain the current playback duration of the audio file |
| [setPlayerLocalVolume](function.md#IThunderAudioPlayer::setPlayerLocalVolume) | Set the local playing volume of the audio file |
| [setPlayerPublishVolume](function.md#IThunderAudioPlayer::setPlayerPublishVolume) | Set the remote playing volume of the audio file |
| [getPlayerLocalVolume](function.md#IThunderAudioPlayer::getPlayerLocalVolume) | Obtain the local playing volume of the audio file |
| [getPlayerPublishVolume](function.md#IThunderAudioPlayer::getPlayerPublishVolume) | Get the remote playing volume of the audio file |
| [setLooping](function.md#IThunderAudioPlayer::setLooping) | Set a looping count |
| [SetFilePlayerNotify](function.md#IThunderAudioPlayer::SetFilePlayerNotify) | Callback when the audio file player is configured |

- Callback of monitoring through [IThunderAudioPlayerNotify](notification.md#IThunderAudioPlayerNotify)

| Callback | Function |
| :---| :--- |
| [onAudioFileVolume](notification.md#IThunderAudioPlayerNotify::onAudioFileVolume) | Reporting the playing progress |
| [onAudioFilePlayEnd](notification.md#IThunderAudioPlayerNotify::onAudioFilePlayEnd) | Reporting the playing-end status |


## Voice Change and Reverb

N/A

## Voice Positioning

N/A

## Volume Prompt

| Method | Function |
| :---| :--- |
| [setAudioVolumeIndication](function.md#IThunderEngine::setAudioVolumeIndication) | Enable/Disable speaker volume callback |

| Callback | Function |
| :---| :--- |
| [onPlayVolumeIndication](notification.md#IThunderEventHandler::onPlayVolumeIndication) | Reporting the speakers' volume |

## Voice Routing

N/A

## In-ear Monitor

N/A


## Audio Device Management

Major methods are encapsulated in the [IAudioDeviceManager](function.md#IAudioDeviceManager) interface class and obtain object pointers through the [getAudioDeviceMgr](function.md#IThunderEngine::getAudioDeviceMgr) interface.

| Method | Function |
| :---| :--- |
| [getAudioDeviceMgr](function.md#IThunderEngine::getAudioDeviceMgr) | Get pointers of audio/video device management objects |

- [Methods in the IAudioDeviceManager](function.md#IAudioDeviceManager) interface class

| Method | Function |
| :---| :--- |
| [enumInputDevices](function.md#IAudioDeviceManager::enumInputDevices) | Enumerate audio input devices |
| [setInputtingDevice](function.md#IAudioDeviceManager::setInputtingDevice) | Set audio input devices for capturing|
| [getInputtingDevice](function.md#IAudioDeviceManager::getInputtingDevice) | Get the currently selected audio input device |
| [setInputtingVolume](function.md#IAudioDeviceManager::setInputtingVolume) | Set the volume of the current audio input device |
| [getInputtingVolume](function.md#IAudioDeviceManager::getInputtingVolume) | Get the volume of the current audio input device |
| [setInputtingMute](function.md#IAudioDeviceManager::setInputtingMute) | Mute or unmute the current audio input device |
| [getInputtingMute](function.md#IAudioDeviceManager::getInputtingMute) | Get the mute status of the current audio input device |
| [startInputDeviceTest](function.md#IAudioDeviceManager::startInputDeviceTest) | Start testing the current audio input device |
| [stopInputDeviceTest](function.md#IAudioDeviceManager::stopInputDeviceTest) | Stop testing the current audio input device |
| [enumOutputDevices](function.md#IAudioDeviceManager::enumOutputDevices) | Enumerate audio playback devices |
| [setOutputtingDevice](function.md#IAudioDeviceManager::setOutputtingDevice) | Specify the audio playback device |
| [getOutputtingDevice](function.md#IAudioDeviceManager::getOutputtingDevice) | Get the current audio playback device |
| [setOuttingVolume](function.md#IAudioDeviceManager::setOuttingVolume) | Set the volume of the current playback device |
| [getOuttingVolume](function.md#IAudioDeviceManager::getOuttingVolume) | Get the volume of the current playback device |
| [setOutputtingMute](function.md#IAudioDeviceManager::setOutputtingMute) | Mute/Unmute the current playback device |
| [getOutputtingMute](function.md#IAudioDeviceManager::getOutputtingMute) | Get the mute status of the current playback device |
| [startOutputDeviceTest](function.md#IAudioDeviceManager::startOutputDeviceTest) | Start testing the current audio playback device |
| [stopOutputDeviceTest](function.md#IAudioDeviceManager::stopOutputDeviceTest) | Stop testing the current audio playback device |
| [enableMicEnhancement](function.md#IAudioDeviceManager::enableMicEnhancement) | Enable/Disable microphone enhancement |
| [enableMicDenoise](function.md#IAudioDeviceManager::enableMicDenoise) | Enable/Disable microphone noise reduction |
| [enableAEC](function.md#IAudioDeviceManager::enableAEC) | Enable/Disable AEC |
| [enableAGC](function.md#IAudioDeviceManager::enableAGC) | Enable/Disable Automatic Gain Control (AGC) |

| Callback | Function |
| :---| :--- |
| [onAudioCaptureStatus](notification.md#IThunderEventHandler::onAudioCaptureStatus) | Callback on changes in audio device capture status |
| [onInputVolume](notification.md#IThunderEventHandler::onInputVolume) | Callback on test volume of the current audio input device |
| [onOutputVolume](notification.md#IThunderEventHandler::onOutputVolume) | Callback on test volume of the current audio playback device |

## Video Device Management

Major methods are encapsulated in the [IVideoDeviceManager](function.md#IVideoDeviceManager) interface class and obtain object pointers through the [getVideoDeviceMgr](function.md#IThunderEngine::getVideoDeviceMgr) interface.

| Method | Function |
| :---| :--- |
| [getVideoDeviceMgr](function.md#IThunderEngine::getVideoDeviceMgr) | Get the pointer of the video device management object |

- [Methods in the IVideoDeviceManager](function.md#IVideoDeviceManager) interface class

| Method | Function |
| :---| :--- |
| [enumVideoDevices](function.md#IVideoDeviceManager::enumVideoDevices) | Enumerate video input devices |
| [startVideoDeviceCapture](function.md#IVideoDeviceManager::startVideoDeviceCapture) | Start video device capturing |
| [stopVideoDeviceCapture](function.md#IVideoDeviceManager::stopVideoDeviceCapture) | Stop video device capturing |
| [enumMonitorDevices](function.md#IVideoDeviceManager::enumMonitorDevices) | Enumerate monitor input devices |

| Callback | Function |
| :---| :--- |
| [onVideoCaptureStatus](notification.md#IThunderEventHandler::onVideoCaptureStatus) | Reporting the camera capturing status |

## Media extra information

| Method | Function |
| :---| :--- |
| [registerMediaExtraInfoObserver](function.md#IThunderEngine::registerMediaExtraInfoObserver) | Register the monitored object of media extra information [IThunderMediaExtraInfoObserver](notification.md#IThunderMediaExtraInfoObserver) |
| [sendMediaExtraInfo](function.md#IThunderEngine::sendMediaExtraInfo) | Send media extra information |

- the [IThunderMediaExtraInfoObserver](notification.md#IThunderMediaExtraInfoObserver) interface class reports the status and informations of the MediaExtraInfo.

| Callback | Function |
| :---| :--- |
| [onSendMediaExtraInfoFailedStatus](notification.md#IThunderMediaExtraInfoObserver::onSendMediaExtraInfoFailedStatus) | Callback on failure in sending media extra information |
| [onRecvMediaExtraInfo](notification.md#IThunderMediaExtraInfoObserver::onRecvMediaExtraInfo) | Received media extra information |
| [onRecvMixAudioInfo](notification.md#IThunderMediaExtraInfoObserver::onRecvMixAudioInfo) | Received extra information of mixed audio stream |
| [onRecvMixVideoInfo](notification.md#IThunderMediaExtraInfoObserver::onRecvMixVideoInfo) | Received extra information of mixed video stream |

## Audio Raw Data

| Method | Function |
| :---| :--- |
| [registerAudioFrameObserver](function.md#IThunderEngine::registerAudioFrameObserver) | Register a observer [IAudioFrameObserver](notification.md#IAudioFrameObserver) |
| [setRecordingAudioFrameParameters](function.md#IThunderEngine::setRecordingAudioFrameParameters) | Set the mode for using raw audio recording data during callback [onRecordAudioFrame](notification.md#IAudioFrameObserver::onRecordAudioFrame) |
| [setPlaybackAudioFrameParameters](function.md#IThunderEngine::setPlaybackAudioFrameParameters) | Set the mode for using raw audio playback data during callback [onPlaybackAudioFrame](notification.md#IAudioFrameObserver::onPlaybackAudioFrame) |

- the [IAudioFrameObserver](notification.md#IAudioFrameObserver) interface class reports the information of the Audio Raw Data information.

| Callback | Function |
| :---| :--- |
| [onRecordAudioFrame](notification.md#IAudioFrameObserver::onRecordAudioFrame) | Callback on raw audio capture data |
| [onPlaybackAudioFrame](notification.md#IAudioFrameObserver::onPlaybackAudioFrame) | Callback on raw audio play data |
| [onPlaybackAudioFrameBeforeMixing](notification.md#IAudioFrameObserver::onPlaybackAudioFrameBeforeMixing) | Callback on raw data after the audio remote data decoding (differentiated among users) |

## Video Raw Data

| Method | Function |
| :---| :--- |
| [registerVideoFrameObserver](function.md#IThunderEngine::registerVideoFrameObserver) | Register video monitor object [IVideoFrameObserver](notification.md#IVideoFrameObserver) |
| [registerVideoCaptureObserver](function.md#IThunderEngine::registerVideoCaptureObserver) | Register monitoring object for camera data capture [IVideoCaptureObserver.](notification.md#IVideoCaptureObserver) |

- the [IVideoFrameObserver](notification.md#IVideoFrameObserver) interface class reports the Video Raw Data (rendering & preview)information.

| Callback | Function |
| :---| :--- |
| [onPreviewVideoFrame](notification.md#IVideoFrameObserver::onPreviewVideoFrame) | Occurs when local video preview data is returned. |
| [onRenderVideoFrame](notification.md#IVideoFrameObserver::onRenderVideoFrame) | Callback on rendering video data of other users |

- the [IVideoCaptureObserver](notification.md#IVideoCaptureObserver) interface class reports the Video Raw Data (capturing) information.

| Callback | Function |
| :---| :--- |
| [onCaptureVideoFrame](notification.md#IVideoCaptureObserver::onCaptureVideoFrame) | Callback on video data collected locally |

## Custom Audio Capture

| Method | Function |
| :---| :--- |
| [setCustomAudioSource](function.md#IThunderEngine::setCustomAudioSource) | Set parameters of external audio capturing |
| [pushCustomAudioFrame](function.md#IThunderEngine::pushCustomAudioFrame) | Publishing an external audio frame |

## Custom Video Capture

| Method | Function |
| :---| :--- |
| [setCustomVideoSource](function.md#IThunderEngine::setCustomVideoSource) | Set parameters for external video capturing |
| [pushCustomVideoFrame](function.md#IThunderEngine::pushCustomVideoFrame) | Publishing external video frame |

## Audio Self-rendering

N/A

## Video Self-rendering

N/A

## Custom Messages

| Method | Function |
| :---| :--- |
| [sendUserAppMsgData](function.md#IThunderEngine::sendUserAppMsgData) | Send custom broadcasting message |

| Callback | Function |
| :---| :--- |
| [onRecvUserAppMsgData](notification.md#IThunderEventHandler::onRecvUserAppMsgData) | Reporting custom broadcasting message |
| [onSendAppMsgDataFailedStatus](notification.md#IThunderEventHandler::onSendAppMsgDataFailedStatus) | Callback on failure when sending broadcasting message |

## Log Management

| Method | Function |
| :---| :--- |
| [setLogFilePath](function.md#IThunderEngine::setLogFilePath) | Set a directory for SDK to write the log files |
| [setLogLevel](function.md#IThunderEngine::setLogLevel) | Set the log levels |

## Other methods

| Method | Function |
| :---| :--- |
| [enableWebSdkCompatibility](function.md#IThunderEngine::enableWebSdkCompatibility) | Enable/Disable WebSDK compatibility |
