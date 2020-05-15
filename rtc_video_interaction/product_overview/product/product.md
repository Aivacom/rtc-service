# Product Overview

AIVACOM real-time video interaction  is a product that allows real-time video call and distribution of interactive live streaming among users.

Based on years’ accumulation of AIVACOM in network and audio/video technologies as well as self-developed real-time network (RTN) and audio/video engines, this product delivers seamless, multi-platform compatible, low-latency and high-currency real-time audio/video call capability across globe. It aims to facilitate developers to quickly implement one-to-one, one-to-many, many-to-many, and live streaming distribution, thereby satisfying scenario-specific requirements in industries such as social media, live streaming, education, and collaboration.


## Product Architecture
![](/resources/en/rtc_service/Real-time-network.png)


## Technological Scenarios

Oriented to specific scenarios of different services, AIVACOM real-time video interaction (AIVACOM-Video-Interaction) provides two basic technological capabilities:

| Technological Scenario Category | Capability | Scenarios |
| ------ | ------ | ------ |
| Real-Time Video Call | One-to-one or many-to-many video call | One-to-one or one-to-many video chat, party held in video chat room, video conference, small class teaching, and large class teaching[] |
| Live video Broadcasting | Sharing of single-person video publishing or group video interaction to CDN | Microphone connection between anchor and audience and between anchors for PK in show live streaming and large open classes |

## Major Functions

Adapting to major technological scenarios, AIVACOM real-time video interaction (AIVACOM-Video-Interaction) provides abundant sets of underlying function interfaces, from which developers can choose to integrate to satisfy specific service scenarios.

### Basic Functions

| Functional categories | Major Functions | Function Description | Scenarios |
| ------ | ------ | ------ | ------ |
| Interaction function  | Host-in on client side | Low-latency interaction between clients in a room | All scenarios |
| Interaction function | Host-in across rooms  | Low-latency interaction between clients in different rooms | Commonly used in show live streaming scenarios where anchors in two rooms are connected on microphone for talent PK |
| Audio function | Hi-Fi tone quality | High tone quality and 2-channel stereo with audios sampled at 48 kHz | Commonly used in scenarios including high-quality audio radio, karaoke, and music teaching |
| Audio function | 3A processing | 3A: Acoustic Echo Chancellor (AEC), Automatic Noise Suppression (ANS), and Automatic Gain Control (AGC), assuring sound tone quality in scenarios such as dual-talk and noise mitigation | All scenarios |
| Audio function | Accompaniment mixing | Local or online audio files and user voice are sent to other users in the room for play in a synchronous manner | Commonly used in scenarios such as show live streaming, audio chat room, matchmaking video chat involving multiple people, karaoke room, audio radio, small class teaching, and large class teaching |
| Audio function | Voice Change and Reverb | Voice change effect is pre-defined with 14 modes and 10 scenarios provided. The 14 modes include girly, mature-man, heavy metal effects. The 10 scenarios include karaoke, recording studio, and concert. | Commonly used in scenarios such as show live streaming, audio chat room, matchmaking video chat involving multiple people, karaoke room, and audio radio |
| Audio function | Volume Prompt | Provides volume indication for local and remote users to display waveform or loudspeaker volume indication | Commonly used in scenarios such as show live streaming, audio chat room, matchmaking video chat involving multiple people, karaoke room, and audio radio |
| Audio function | Voice Positioning | Supports configuration of voice occurrence position of remote users, which allows users to distinguish direction during gaming. This reproduces the real gaming scenario. | Commonly used in game voice scenarios and the like |
| Audio function | Original audio data | Original audio data collected through SDK is processed in a customized manner. For example, in pre-processing phase, the user can optimize original audio data before submitting it to SDK for encoding and transmission | Commonly used in the scenario that users have their audio/video libraries and audio data modification such as voice change is required |
| Video function | HD image quality | 720P and 1080P HD image quality | All video scenarios |
| Video function | Screen Sharing | Video content is displayed to other users in the room synchronously. Users can specify the screen, program window, and area for sharing | Commonly used in game live streaming, large class teaching, small class teaching, one-to-one teaching, kid programming, and video conference |
| Video function | Raw Video Data | Original video data collected through SDK is processed in a customized manner. For example, in pre-processing phase, the user can optimize original video data before submitting it to SDK for encoding and transmission | Commonly used in scenarios such as video call, video chat room, and interactive live streaming where users optimize video data by using various tools |
| Live streaming | Audio and image mixing | Multiple channels of audio/video streams in a room are treated with audio and video mixing as well as customized image integration layout, and one channel is output | Commonly used in interactive live streaming scenarios |
| Live streaming | RTMP Streaming | Audio/Video streams in a room are pushed to other RTMP servers through CDN and are distributed by CDN by using third-party implementation | Commonly used in interactive live streaming scenarios where users require sharing on social media |
| Live streaming | Extra information | During transmission of audio/video stream data, some user-defined information is synchronized to the media stream through SEI/DSE frames. This allows synchronization of service information, such as layout information, lyric information, and volume indication | Applicable to scenarios where user-defined information, layout data or volume indication defaulted to be carried are present |

### Auxiliary Functions

| Functional categories | Major Functions | Function Description | Scenarios |
| ------ | ------ | ------ | ------ |
| Auxiliary Functions | Cloud recording | Audio/Video content is recorded at server and is stored to a third party through file write | Online education, social entertainment, and financial customer service |
| Auxiliary Functions | Chatroom&Real-Time Signaling | Reliable transmission channel for real-time message and status synchronization | All scenarios |
| Auxiliary Functions | Audio audit | Security check is performed to ensure the audio content does not contain pornographic content, improper political points, and the like | Service compliance check |
| Auxiliary Functions | Video audit | Security check is performed to ensure the video content does not contain pornographic content, improper political points, and the like | Service compliance check |


## Product Advantages

AIVACOM real-time video interaction provides industry-leading product quality:

| Advantage | Description |
| ------ | ------ |
| Full coverage and high concurrency | RTN dedicated for bidirectional real-time transmission and self-established IDC equipment room+public cloud provide high-quality audio/video real-time network system that covers globe. Intelligent route algorithms guarantee optimal end-to-end transmission path and support millions of concurrencies, providing best ever service experience to users. |
| Compatibility with all platforms and multiple terminals | Industry-leading compatibility: SDK APIs covering iOS, Android, Windows, and MacOS are provided. Interconnection with WebRTC and WeChat applets is supported. Compatible with over 5000 terminal models, this product delivers superior power consumption and audio/video quality performance when used on low-configuration terminal models. |
| High quality and low latency | Self-developed audio/video engine excels the industry in audio, video, and network algorithm performance. It provides an average end-to-end latency range of 200 ms, supports HD image quality of 720P and 1080P, and normal video service in case of 50% packet loss rate. It supports 48 kHz high tone quality, normal audio service in case of 70% packet loss rate, and excellent 3A processing. It also helps eliminate echo, howling, and background noise. |
| Multiple scenarios and easy combination | One SDK and one set of APIs for collection, pre-processing, encoding, transmission, decoding, post-processing, and rendering playback. Abundant functional interface types and complete event information callback satisfy various requirements of different industry scenarios. |
| Low cost and easy access | Complete interface documents and access documents allow low latency interaction in a mere 30 minutes, making the product cost-effective. |


### Key Features

AIVACOM real-time video interaction  provides stable and reliable audio/video performance and allows developers to implement real-time audio/video interaction in various basic network conditions.

| Characteristics | Indicator |
| ------ | ------ |
| SDK package size | 8 to 10 MB |
| Users allowed in a video interaction | 9 persons |
| Users allowed in an audio interaction | Unlimited |
| Number of audience | 1 million |
| Regional path coverage | Global |
| Video attribute | SDK collection supports 1080P resolution and 30 FPS frame rate, and user collection supports 4k coding transmission |
| Audio Profiles | Audio sampling rate: 16 kHz to 48 kHz, number of sound tracks: single track or dual tracks |
| Latency range | Audio latency: 200 ms to 500 ms, video latency: 200 ms to 500 ms |
| Lip sync | –100 ms to +25 ms |
| Packet loss prevention rate | Uplink/Downlink packet loss prevention rate for audio: 70%, Uplink/Downlink packet loss prevention rate for video: 50% |

### Platform Compatibility

AIVACOM real-time video interaction  features compatibility to various platforms and supports interconnection between different platforms: Following is the platform compatibility details:

| Platform | Supported Version | Supported Architecture |
| ------ | ------ | ------ |
| iOS | 8.0+ | armv7, arm64, x86 |
| Android | 4.0.3+ | armeabi-v7a, arm64-v8a, x86, x86_64, and simulator (x86) |
| Windows | 7.0+ | x86 |
| macOS | 10.12+ | x86_64 |
| Web | Chrome 72+ native browser, Chrome 72+ kernel series of browsers | N/A |
| Wechat applets | Supported | N/A |
| Electron | Supported | N/A |
