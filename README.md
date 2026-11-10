# LinkUp — Direct Screen Share

LinkUp is a single-page WebRTC demo for sharing a screen between two browsers without an account or application server. The sharer and viewer exchange SDP connection codes manually by copy and paste.

## Use
1. Publish this repository to GitHub Pages (HTTPS) and open the URL on both devices.
2. On the sharer device, choose **Choose screen & create offer** and approve the browser's screen-sharing prompt.
3. Privately send the offer code to the viewer. The viewer pastes it and chooses **Create answer**.
4. The viewer privately sends the answer code back. The sharer pastes it and chooses **Connect viewer**.
5. Stop sharing from the sharer page when finished.

## Limits and privacy
- There is no automatic signaling service, backend, account, recording, or data storage.
- A public STUN service helps peers discover network routes; this demo has no TURN relay. Strict NAT, firewall, or corporate networks can prevent direct connection.
- Screen capture needs browser permission and a secure context (HTTPS or localhost). The browser owns the permission prompt.
- Treat offer and answer codes as private session details. Do not post them publicly.
- WebRTC encrypts media in transit, but the app does not add an identity or recipient verification layer. Only exchange codes with a person you trust.

## Publish with GitHub Pages
Open **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, and save. Once enabled, the URL will be:
https://rajeshwar01-01.github.io/screen-share-app/
