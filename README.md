# AirVR

AirVR is an open source remote VR display for Gear VR and Oculus Go/Quest. With it, you can play SteamVR games in your standalone headset.

## Discord server

Check the latest new about AirVR in [Discord server](https://discord.gg/KbKk3UM)

## This repository is no longer maintained

This repository is not maintained for a long time.

Fork version is actively developed on the following repository.
Go is now supported on the repository as well as Quest/Quest2.

[https://github.com/AirVR-org/AirVR](https://github.com/AirVR-org/AirVR)

For GearVR users: You can get unmaintained version on this repository (See below).

## Description

AirVR streams VR display output from your PC to Gear VR / Oculus Go / Oculus Quest via Wi-Fi. This is similar to Riftcat or Trinus VR, but our purpose is optimization for Gear VR. AirVR provides smooth head-tracking compared to other apps in a Wi-Fi environment using Asynchronous Timewarp.

Note that many PCVR games require 6DoF controller or multiple buttons, so you might not able to play those games.
You can find playable games in [List of tested VR games and experiences](https://github.com/JoshAtticus/AirVR/wiki/List-of-tested-VR-games-and-experiences).

## Requirements

AirVR requires any of the following headsets:

- Gear VR (SM-R325)
- Gear VR (SM-R324)

Controllers:
- ET-YO324 (Gear VR controller 1st Generation)

And phones:

- Galaxy S6 / S6 Edge
- Galaxy S7
- Galaxy S8 / S8+
- Galaxy S9 / S9+
- Galaxy Note 8

The following devices should work but are untested

- Galaxy S7 Edge
- Galaxy Note5
- Galaxy Note9
- Galaxy S10 / S10+


|Device|Working?|
|---|---|
|GalaxyS9/S9+|OK|
|GalaxyS8/S8+|OK|
|Galaxy Note 8|OK|
|GalaxyS7|OK|
|GalaxyS6(Edge)|OK|

- High-end gaming PC
    - with NVIDIA GPU which supports NVENC ([Supported GPUs](https://github.com/JoshAtticus/AirVR/wiki/Supported-GPU))
    - (or with AMD GPU which supports AMF VCE)
    - Windows 10 is recommended
    - Currently only NVIDIA GPU is supported on Windows 7
- 802.11n/ac wireless or ethernet wired connection
    - It is recommended to use 802.11ac for the headset and ethernet for PC
        - You need to connect both to the same router
- SteamVR

## Install AirVR server for PC

1. Install SteamVR
2. Download installer from [Releases](https://github.com/JoshAtticus/AirVR/releases)
3. Run the installer
4. Open AirVR Launcher

## Usage

- Launch AirVR.exe
- Press "Start Server" button or launch VR game
- SteamVR's small window will appear. You should see a headset icon in the SteamVR status window that looks like a green block with a bold S in the middle
- Launch AirVR Client in your headset
- IP Address of headset will appear in the server tab of AirVR.exe
- Press "Connect" button

## Troubleshoot

- If you got some error, please check [Troubleshooting](https://github.com/JoshAtticus/AirVR/wiki/Troubleshooting)

## Uninstallation

- Execute driver\_uninstall.bat in the driver folder
- Delete the install folder (AirVR does not use the registry)
- If you already deleted the folder without executing driver\_uninstall.bat:
    - Open C:\Users\\%USERNAME%\AppData\Local\openvr\openvrpaths.vrpath and check install directory
    - Execute
    `"C:\Program Files (x86)\Steam\steamapps\common\SteamVR\bin\win32\vrpathreg.exe" removedriver (install folder)`
    in Command Prompt

## Future work

- SteamVR dashboard to control AirVR
- Cloud streaming

## Build

### AirVR Server and GUI (Launcher)

- Open AirVR.sln with Visual Studio 2017 and build
    - AirVR\_server project is the driver for SteamVR written in C++
    - AirVR project is the launcher GUI written in C#

### AirVR Client

- Clone [AirVR Client](https://github.com/JoshAtticus/AirVRClient)
- Put your [osig file](https://developer.oculus.com/documentation/mobilesdk/latest/concepts/mobile-submission-sig-file/) on assets folder (only for Gear VR)
- Build with Android Studio
- Install apk via adb

## License

AirVR is licensed under MIT License.