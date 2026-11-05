# Camera Hub

Watch your home cameras live on your phone, keep recordings, and get motion alerts — at home or away. A Windows PC at home runs the camera server; the Camera Hub app on your Android phone connects to it.

## Downloads

| What | Download |
|---|---|
| **PC setup** (start here) | [**CameraHubSetup.zip**](https://github.com/ggm8boss-droid/CamHub-releases/releases/latest/download/CameraHubSetup.zip) |
| Android app (most phones) | [camerahub-arm64-v8a.apk](https://github.com/ggm8boss-droid/CamHub-releases/releases/latest/download/camerahub-arm64-v8a.apk) |
| Android app (older 32-bit phones) | [camerahub-armeabi-v7a.apk](https://github.com/ggm8boss-droid/CamHub-releases/releases/latest/download/camerahub-armeabi-v7a.apk) |

All versions: [Releases](https://github.com/ggm8boss-droid/CamHub-releases/releases)

You usually don't need to download the app by hand. The PC setup can install it on your phone over a USB cable.

## What you need

- A Windows 10 (22H2) or Windows 11 PC, 64-bit, that stays on at home. It records the cameras.
- Administrator rights on that PC (Windows asks once).
- Plenty of free disk space for recordings, and about 2 GB for the first download.
- An Android phone, and a USB cable (or use the QR code instead).
- About 20–40 minutes, mostly waiting for downloads.

## Set up the PC

1. Download **CameraHubSetup.zip** on the PC that will be the camera server.
2. Right-click the zip → **Extract All**, then open the extracted folder and run **camerahub_setup.exe**.
   - If Windows shows *"Windows protected your PC"*, click **More info → Run anyway**. (The app isn't code-signed yet.)
3. Follow the steps in the window:
   1. **Check this PC.** Choose where to keep the server and recordings (pick a drive with lots of space).
   2. **Windows settings and Docker.** Approve the changes; Docker Desktop is installed if you don't have it.
      If Windows needs to restart, setup opens again by itself after you sign back in and carries on.
   3. **Start Docker**, **Download the server**, **Set up the server**, **Test the server** run on their own.
   4. **Watching from anywhere** (optional). Sign in to a free Tailscale account so your phone can reach the cameras away from home, without router changes. You can skip this if you only watch at home.
   5. **Connect your phone.** See below.

## Connect your phone

**With a USB cable (easiest):** press **Use USB** in setup and follow the on-screen steps to turn on USB debugging on the phone once. Setup installs the Camera Hub app if needed and pairs it, with no typing.

**With a QR code:** install the app (links above), open it, tap **Connect home server**, and scan the QR code shown in setup.

## Adding cameras

Once paired, add cameras from the app (**Add camera**) or from the server. The phone shows live view, recordings and motion alerts.

## Troubleshooting

- **A step failed:** read the message, fix what it says (often the internet connection), then press **Retry**.
- **"A different build of Camera Hub is already on the phone":** uninstall Camera Hub on the phone, then press Install again.
- **Phone not found over USB:** unlock the phone, check that USB debugging is on, and accept the *"Allow USB debugging?"* prompt on the phone.
