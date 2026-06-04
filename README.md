# WegVPN

WegVPN is the Android VPN client for the Weg ecosystem.

## Public repository contents

This repository intentionally contains only:
- `README.md`
- GitHub Release assets with the signed Android APK

Source code is not published in this repository.

## Download

Use the latest GitHub Release to download `WegVPN-release.apk`.

## Current Android build

- Native Google sign-in through Android Credential Manager
- Telegram sign-in support
- Account and subscription sync with [lk-weg.space](https://lk-weg.space)
- VPN servers and protocols are loaded from the active subscription
- Xray-core is bundled through `libv2ray`
- TUN traffic is bridged with bundled `libhev-socks5-tunnel`
- Release package: `com.wegcorp.wegapp`

## Notes

If the app shows no servers, sign in and refresh the profile so the subscription can sync from the Weg account backend.
