---
layout: page
title: Installing Swift
---

{% assign latest = site.data.install.latest %}

To install the latest version of Swift ({{ latest.label }}):

**macOS**: Install <a href="{{ latest.distributions.xcode.url }}" title="Download" download>{{ latest.distributions.xcode.label }}</a>, or download <a href="{{ latest.distributions.macos.url }}" title="Download" download>Swift {{ latest.distributions.macos.label }} macOS installer</a>.

**Linux**: Use docker: <code>docker run swift</code>

**Windows 10**: Use the Windows Package Manager: <code>winget install Swift.Toolchain</code>, or download <a href="{{ latest.distributions.windows10.url }}" title="Download" download>Swift {{ latest.distributions.windows10.label }} Windows 10 installer</a>.

After downloading the release suitable for your system, please follow the installation instructions.

## Installation instructions

A toolchain includes a copy of the Swift compiler and other related tools needed to provide a cohesive development experience for working in a specific version of Swift.

**macOS**

The easiest way to install Swift on macOS is by installing Xcode.
For example, install <a href="{{ latest.distributions.xcode.url }}" title="Download" download>{{ latest.distributions.xcode.label }}</a> which includes the latest Swift toolchain.
You can get other versions of Xcode, including betas, on [developer.apple.com](https://developer.apple.com/xcode).

To install Swift without Xcode, or use an alternative toolchain to the one that came with Xcode, use Swift.org macOS installer.
For example, download <a href="{{ latest.distributions.macos.url }}" title="Download" download>Swift {{ latest.distributions.macos.label }} macOS installer</a> to install the latest Swift toolchain.
You may also need to update Xcode to use this alternative toolchain. [Read more](/install-macos)

**Linux**

Docker is a popular way to use Swift on Linux.
Swift.org publishes Docker images on [docker hub](https://hub.docker.com/_/swift).

The easiest way to install Swift on Linux is using Swift.org official RPMs and Debian packages.

<details style="margin-left: 0">
  <summary>Amazon Linux 2</summary>

  <pre>
  $ curl https://download.swift.org/experimental-use-only/repo/amazonlinux/releases/2/swiftlang.repo > /etc/yum.repos.d/swiftlang.repo
  $ amazon-linux-extras install epel
  $ yum install swiftlang
  </pre>  
</details>

<details style="margin-left: 0">
  <summary>CentOS 7</summary>

  <pre>
  $ curl https://download.swift.org/experimental-use-only/repo/centos/releases/7/swiftlang.repo > /etc/yum.repos.d/swiftlang.repo
  $ yum install epel-release
  $ yum install swiftlang
  </pre>
</details>

To install a Swift toolchain from a prebuilt tarball, download the tarball from the [downloads page](/download) and extract it.
You may also need to confirm `PATH` includes the toolchain location, and that Swift's system dependencies are installed. [Read more](/install-linux-tarball)

**Windows**

The easiest way to install Swift on Windows is using the Windows Package Manager. Note that Windows Package Manager release version may be behind the latest release from Swift.org.

Alternatively, use Swift.org Windows installer.
For example, download <a href="{{ latest.distributions.windows10.url }}" title="Download" download>Swift {{ latest.distributions.windows10.label }} Windows 10 installer</a> to install the latest Swift toolchain.

You may also need to confirm `PATH` includes the toolchain location, and that Swift's system dependencies are installed. [Read more](/install-windows)

**Other**

Older versions of Swift, nightly toolchains, and additional information about installing Swift can be found on the [downloads page](/download).

Alternatively, tools like [swiftenv](https://github.com/kylef/swiftenv) help install and manage multiple Swift toolchain versions on the same system.
