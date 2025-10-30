---
title: Freedesktop SDK
addedAt: 2025-10-29
category: os
tags: linux-distribution
iconSlug: freedesktopdotorg
permalink: /freedesktop-sdk
versionCommand: cat /etc/os-release
releasePolicyLink: https://freedesktop-sdk.gitlab.io/documentation/updating-sdk/release-notes/
latestColumn: true

auto:
  methods:
    # Cross check with the GitLab releases
    # https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/releases
    - git: https://gitlab.com/freedesktop-sdk/freedesktop-sdk.git
      regex: ' freedesktop-sdk-(?P<version>\d{2}[.]\d{2}[.]\d{1})'
      template: "{{version}}"

# eol(r) = releaseDate(r) + 2 years
releases:
  - releaseCycle: "25.08"
    releaseDate: 2025-09-01
    eol: false
    latest: 25.08.2
    latestReleaseDate: 2025-10-16
    link: https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/releases/freedesktop-sdk-25.08.2

  - releaseCycle: "24.08"
    releaseDate: 2024-09-08
    eol: false
    latest: 24.08.27
    latestReleaseDate: 2025-10-15
    link: https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/releases/freedesktop-sdk-24.08.27

  - releaseCycle: "23.08"
    releaseDate: 2023-09-06
    eol: true
    latest: 23.08.34
    latestReleaseDate: 2025-09-29
    link: https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/releases/freedesktop-sdk-23.08.34

  - releaseCycle: "22.08"
    releaseDate: 2022-09-01
    eol: true
    latest: 22.08.28
    latestReleaseDate: 2025-09-08
    link: https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/tags/freedesktop-sdk-22.08.28

  - releaseCycle: "21.08"
    releaseDate: 2021-09-04
    eol: true
    latest: 21.08.22
    latestReleaseDate: 2023-10-02
    link: https://gitlab.com/freedesktop-sdk/freedesktop-sdk/-/releases/freedesktop-sdk-21.08.22
---

> [Freedesktop SDK](https://freedesktop-sdk.gitlab.io/) provides a Platform and SDK for desktop applications in various forms.

* [OCI image](https://hub.docker.com/r/freedesktopsdk/platform/tags)
* [Flatpak runtime](https://flathub.org/en/apps/org.freedesktop.Platform)
* [Snap runtime](https://freedesktop-sdk.gitlab.io/documentation/using-the-sdk/building-outputs/building-snap-image/)
* [Operating system image](https://freedesktop-sdk.gitlab.io/documentation/using-the-sdk/building-outputs/building-os/)
* [Tarball](https://freedesktop-sdk.gitlab.io/documentation/using-the-sdk/building-outputs/building-tarball/)

Releases are created every year at the end of August.
The release branches receive security updates as necessary.
An old release cylce becomes EOL two years after the first release.
