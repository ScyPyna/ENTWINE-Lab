# Mattermost

Mattermost is the chat the group uses to communicate: channels, direct
messages and file sharing, similar to Slack. It runs on the group server, so
it is reachable **only while [Tailscale](../OpenVPN/README.md#tailscale) is
active** on the device you are using.

## Install it

Mattermost works on every device:

- **Computer** (Windows, macOS, Linux): download the desktop app from
  https://mattermost.com/apps/
- **Phone and tablet**: install *Mattermost* from the
  [App Store](https://apps.apple.com/app/mattermost/id1257222717) (iOS) or
  [Google Play](https://play.google.com/store/apps/details?id=com.mattermost.rn) (Android)

## Join the group server

1. Turn on Tailscale.
2. Open the app and enter exactly `http://100.105.81.57:8065` as the server URL.
3. The first time, create your account. Username and password are your own
   choice and personal: they are not the lab's Gmail credentials used for
   Tailscale.

Once logged in, you are in the group server.
