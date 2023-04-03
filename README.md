# AirAPI_Mac-Dist
Pre-release versions of AirAPI apps.

## Releases

- 0.1.0, build 1: Pre-alpha releae of test bench & telemetry API project for Nreal Air.

## How to install

Disclaimer: this project is aimed at fellow developers and power users, proceed with caution.

1. Download the latest release from the "releases" option on the right sidebar ->

2. Unzip on your Mac

3. You will find AirAPI_Example.app and some library files in `libs/` that you will need move to some location on-path, that is, discoverable by your system so this app can run (it will crash if don't have these in your enironment):

- all of the files in `libs/` need to go in a library folder (or aliased to one) within macOS, like `/usr/local/lib`

- once moved, make sure both libs have +x, or use `chmod +x (lib)` for both

- all of the header files in `include/` folder will need move to some location on-path like `/usr/local/include`

- once done with the libraries, simply move the .app to `~/Applications`

- In the next step you will be warnied by Apple that this app is unsafe etc-- it's safe, just go to `~/Applications` in Finder and use `option + right-click` and then click "open". Then clock "open" again, this will by-pass gatekeeper

    - If the above doesn't work and you can't open it, to to your settings and [make sure you allow apps from "trusted developers"](https://support.apple.com/guide/mac-help/open-a-mac-app-from-an-unidentified-developer-mh40616/mac) and click this link if you have any more issues

That's it, now plug in your Nreal Air to you Mac and click "connect" if the globe does not automatically start tracking your glasses positional data.

Note: if it is crashing on launch or not opening, go back and [make sure your libs are on your $PATH](https://www.macgasm.net/news/tips/adding-a-new-location-to-your-path-variable-within-terminal/)

## Compatibility

This SDK is verified compatible with the following:

- macOS Ventura
- Swift v5^ & and Xcode 14^
- SceneKit
- RealityKit

We need your feedback about M-Series-- did it work for you? If not, please get in touch.
