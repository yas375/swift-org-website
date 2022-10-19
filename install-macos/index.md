---
layout: page
title: Installing Swift.org toolchain on macOS
---

Xcode includes a release of Swift that is supported by Apple.
You can install an alternative toolchain from Swift.org to try out new language features.

<div class="danger" markdown="1">
To submit to the App Store you must build your app using the version of Swift that comes included within Xcode.
</div>

## Installation

1. Run the package installer, which will install an Xcode toolchain into `/Library/Developer/Toolchains/`.

2. Add the Swift toolchain to your path as follows:
 ~~~ shell
 $ export PATH=/Library/Developer/Toolchains/swift-latest.xctoolchain/usr/bin:"${PATH}"
 ~~~

## Configure Xcode to use the new toolchain

1. Open Xcode's `Preferences`, navigate to `Components > Toolchains`, and select the installed Swift toolchain.

1. Xcode uses the selected toolchain for building Swift code, debugging, and even code completion and syntax coloring.

   You'll see a new toolchain indicator in Xcode's toolbar when Xcode is using a Swift toolchain. Select the Xcode toolchain to go back to Xcode's built-in tools.

1. Selecting a Swift toolchain affects the Xcode IDE only. To use the Swift toolchain with command-line tools, use `xcrun --toolchain swift` and `xcodebuild -toolchain swift`.

## Code Signing on macOS

The macOS `.pkg` files are digitally signed by the developer ID of the Swift open source project to allow verification that they have not been tampered with.
All binaries in the package are signed as well.

The Swift toolchain installer on macOS should display a lock icon on the right side of the title bar.
Clicking the lock brings up detailed information about the signature.
The signature should be produced by `Developer ID Installer: Swift Open Source (V9AUD2URP3)`.

<div class="warning" markdown="1">
If the lock is not displayed or the signature is not produced by the Swift open source developer ID, do not proceed with the installation.
Instead, quit the installer and please email <swift-infrastructure@forums.swift.org> with as much detail as possible, so that we can investigate the problem.
</div>
