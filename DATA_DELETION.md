# Account and Data Deletion

App: Delovni cikel / WorkCycle  
Developer: Dante Produkcija

This page explains how to request deletion of cloud account and Team Sync data for Delovni cikel / WorkCycle.

Core local app data is stored on your device. Team/cloud data is stored in Firebase only when you create or join a team or use team features.

## How to request deletion

Send an email to:

danteprodukcija@gmail.com

Use this subject:

WorkCycle data deletion request

In your email, include the information needed to identify your Team Sync data:

- the Google account or email used for Team Sync, if applicable
- if you used only anonymous Team Sync, include the team name, team code, display name, or other details that can help identify the data
- any active team ID, member display name, roster name, internal number, task title, schedule date, or other details that can help identify the relevant cloud/team records
- a short description of what you want deleted

## What can be deleted

When the data can be identified, the developer can delete or remove:

- Firebase Auth account / Team Sync identity
- Team membership data, roles, display names and roster metadata such as roster name and unit roster number
- Team Schedule data where identifiable and technically possible, including work areas, member-area skills, schedule assignments, Team Schedule settings, day states, standby member fields and published/unpublished day state
- Field Tasks / Team Tasks created by or assigned to the user, where identifiable and technically possible
- Field Task / Team Task comments, history text and author references, where identifiable and technically possible
- FCM notification token linked to the team or user
- other cloud data linked to Team Sync

## Local-only data

Most WorkCycle data is stored only on your device. This includes:

- Work Log data
- Local pickups
- Travel Orders
- vehicles
- local schedules, status labels and app settings
- widget settings
- local backup or export files that you choose to create
- most app settings

Local-only data is not stored by the developer and cannot be deleted remotely. You can delete local-only data by clearing app data in Android settings, deleting local backup/export files, or uninstalling the app.

Uninstalling the app or clearing app data removes local data from that device. It does not automatically delete cloud/team data that was already stored in Firebase. Cloud/team data requires the account, team or support deletion process described above.

## What may be retained

Some data may be retained when required for security, abuse prevention, debugging, legal compliance, or shared team history consistency.

Some team records may remain if they are needed to preserve shared team history, owner/admin continuity, team access continuity, security, or legal obligations. Team task records, Team Schedule records and comments may be retained, minimized, anonymized, or kept as deleted placeholders depending on the request and team context. Where possible, personal identifiers will be removed or minimized.

Anonymized or non-identifiable records may be retained when they can no longer be linked to a specific user.

## Timing

Deletion requests are normally processed within 30 days after the request can be verified and the relevant data can be identified.

## Privacy policy

For more information, see [PRIVACY_POLICY.md](PRIVACY_POLICY.md).
