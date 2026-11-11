# LinkUp — Direct Screen Share

LinkUp pairs two browsers and streams a live screen over peer-to-peer WebRTC. It uses HTTPS GitHub Pages, has no account or signaling server, and supports both QR pairing and manual copy/paste codes.

**Open the app:** https://rajeshwar01-01.github.io/screen-share-app/

## Pair devices with QR

1. Open the app on both devices. On the sharer, choose **Choose screen & create offer** and select the screen/window/tab to share.
2. The sharer displays an offer QR. On the viewer, choose **Scan offer QR** and allow camera access, or use the device camera and paste the offer code manually.
3. The viewer creates an answer and displays an answer QR. On the sharer, choose **Scan answer QR** or paste the answer code.
4. Stop the session on either device when finished.

QR generation runs locally from the bundled QRCode.js library; connection codes are not sent to a QR service. The QR codes contain temporary session connection details: show or send them only to the intended person. QR scanning uses the browser camera only when you press a scan button, and stops when a code is read or scanning is cancelled. Browsers without the Barcode Detection API can use the existing copy/paste fields.

## Device and network limits

The sharer needs a browser/device that supports screen capture; the viewer needs WebRTC video support. Availability varies between browsers and operating systems. Screen capture and camera access require HTTPS and browser permission. A mobile browser may work as a viewer even when it cannot share its own screen.

The app has no TURN relay. Direct connections can fail behind restrictive NATs, firewalls, or corporate networks. It streams one sharer's screen to one viewer at a time; to share back, start a new session with roles reversed. It does not transfer files.

## Publish with GitHub Pages

The site is static. Keep the root `index.html` and `vendor/qrcodejs.min.js` together when publishing the `main` branch from `/(root)`.
