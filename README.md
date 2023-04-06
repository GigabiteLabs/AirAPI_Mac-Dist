# AirAPI_Mac-Dist
Pre-release versions of AirAPI SDK apps for macOS.

## Release Info

- 0.2.0, build 1: Pre-alpha update to the test bench & telemetry project for Nreal Air.

### Latest Release Notes:

Updates / Fixes

- Everything is pre-built and included within the application-- it should "just work"
    
    - After much R&D, the underlying libraries are now compiled and using CMake such that they are directly included with the app-- no more weird developer stuff with installing hidapi, or putting things on path (you can remove them now if you installed 0.1.0)

- Fixed crash on "stop connection"

    - Was due to an underlying c++ threading issue which is now resolved when disconnecting


Notes:

- In order to simplify the R&D, the ability to build for M-Series was temporarily disabled in Xcode-- but it should still run on M-Series with Rosetta
    
    - Please let us know if you are able to run with Rosetta on M-Series

    - If you have any crashes or issues, please [go to issues](https://github.com/GigabiteLabs/AirAPI_Mac-Dist/issues) and create a report-- more information is better, if you can include a crash report that would be 100% best (like this fine tester, [right here](https://github.com/GigabiteLabs/AirAPI_Mac-Dist/issues/1))

- No major changes or improvements to the UI were done in this build, this one is purely about smoothing out the ability to run the app, and making it as accessible to as many mac users as possible.


Known Issues:

- The window is not resizable, and may be too large on some macs to see all of the buttons macs

    - apologies, this is an autolayout bug that was just beyond the goal of this release

    - this will be fixed in the next release.

- Connection status UI does not ever update or reflect the actual status

    - on it, will be resolved in the next release


## How to install

Disclaimer: this project is aimed at fellow developers and power users, proceed with caution.

1. Download the latest release from the "releases" option on the right sidebar ->

2. Unzip on your Mac

3. You will find AirAPI_Example.app

4. Open another finder window and move AirAPIExample.app to your `/Applications` folder

5. Launch it:

    - You will be warnied by Apple that this app is unsafe etc-- it's safe.

    - To launch: go to `~/Applications` in Finder and use `option + right-click` and then click "open". Then clock "open" again, this will by-pass gatekeeper

        - If the above doesn't work and you can't open it, to to your settings and [make sure you allow apps from "trusted developers"](https://support.apple.com/guide/mac-help/open-a-mac-app-from-an-unidentified-developer-mh40616/mac) and click this link if you have any more issues

That's it, now plug in your Nreal Air and click "connect" (if the globe does not automatically start tracking your Nreal Air postitional updates)

## Compatibility

This SDK is verified compatible with the following:

- macOS Ventura (Intel)
- Swift v5^ & and Xcode 14^
- SceneKit
- RealityKit

We need your feedback about M-Series-- did it work for you? If not, please get in touch or submit a [git issue](https://github.com/GigabiteLabs/AirAPI_Mac-Dist/issues)