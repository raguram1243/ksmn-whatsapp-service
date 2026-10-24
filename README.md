# KSMN WhatsApp Service (installer)

Windows installer for the shop PC's automatic WhatsApp sending service used by the KSMN Kanakku-Book app.
This repository only hosts the installer download. It is not the application source.

## Install

1. Download `KSMN-WhatsApp-Service-Setup-1.0.0.exe` from the [latest release](../../releases/latest).
2. Run it on the shop PC. Windows may say "Windows protected your PC" because the file is not code-signed: choose **More info**, then **Run anyway**.
3. In the KSMN app, open **Settings -> Automatic WhatsApp sending**, press **Make a pairing code**, and type the code into the installer.
4. Scan the QR code shown in Settings with the shop phone (WhatsApp -> Linked devices -> Link a device).

The installer does nothing useful without a pairing code from an app administrator.

## What it installs

A small helper that starts when the PC user signs in, [OpenWA](https://github.com/rmyndharis/OpenWA) (MIT licence), a private copy of Node.js, and a Chromium browser. The helper only makes outgoing connections to the app's server; nothing on the PC is reachable from the internet.

## Important

OpenWA is an unofficial tool that drives WhatsApp Web. WhatsApp can restrict a number that uses it. Use a dedicated shop number and message only customers you already deal with.

Third-party components keep their own licences (OpenWA: MIT, Node.js: MIT, Chromium: BSD-style and others).
