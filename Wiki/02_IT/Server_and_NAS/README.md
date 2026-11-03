# Workstation and NAS

The workstation and the NAS are both on the department network. Your NAS
**username and password are the same** as on the workstation.

## NAS folders on the workstation

Every time you [log in to the workstation](../SSH_Keys/README.md), the NAS
shared folders `Public` and `Multimedia` are mounted automatically in your
home:

- `~/nas_public` → NAS `Public`
- `~/nas_multimedia` → NAS `Multimedia`

These are not copies: whatever you do in these folders (create, edit, move or
delete files) happens **directly on the NAS**, immediately. Deleting a file
there deletes it from the NAS.

## Do not use SSH on the NAS

Logging into your NAS home with SSH is **strongly discouraged**. The
workstation and your computers reach the NAS through SMB, the file-sharing
protocol that keeps track of permissions and of who has a file open. SSH
bypasses SMB and works directly on the NAS disk, so files changed that way can
end up with the wrong permissions, become unreadable from the workstation, or
clash with someone using them at the same time.

Use the mounted folders on the workstation instead.
