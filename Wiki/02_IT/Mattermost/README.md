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
2. **First time only:** open this invite link in a browser and create your
   account:

   http://100.105.81.57:8065/signup_user_complete/?id=68pa9zbqy7rtjd63u14rqcye3a

   Without this link you cannot create an account: the normal login page has
   no sign-up option. Username and password are your own choice and personal:
   they are not the lab's Gmail credentials used for Tailscale.
3. Open the app, enter exactly `http://100.105.81.57:8065` as the server URL
   and log in with the account you just created.

Once logged in, you are in the group server.

If the link or the server URL does not open at all, Tailscale is not active
on that device.
