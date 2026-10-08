# Account and Data Deletion

App: Delovni cikel / WorkCycle  
Developer: Dante produkcija

This page explains how to request deletion or minimization of cloud account and Team Sync data for Delovni cikel / WorkCycle.

Core local app data is stored on your device. Team/cloud data is stored in Firebase only when you create or join a team or use team features.

Depending on Android system backup settings and WorkCycle backup rules, selected local settings may be included in Android system cloud backup. Android device-to-device transfer may include additional local schedule/settings data and the local Room database, including Work Log evidence. These Android mechanisms are separate from Team Sync/Firebase and are controlled by Android or device settings.

## How to request deletion

Send an e-mail to:

danteprodukcija@gmail.com

Use this subject:

WorkCycle data deletion request

Include enough information to identify the correct Team Sync data:

- the Google account or e-mail used for Team Sync, if applicable
- the Firebase UID shown in the app's Account and data deletion screen, if available
- if you used only anonymous Team Sync, the team name, Team code, display name or other identifying details
- any active Team ID, member display name, roster name, internal number, task/project title, schedule date or other detail that can identify the relevant records
- a short description of the data you want deleted or minimized

Do not send passwords, authentication tokens, QR/NFC tag values, medical documents or unnecessary personal data.

The request must be verified before cloud data is changed. If a verified request asks to delete the app account, the developer deletes the Firebase Authentication identity through the manual operator process. There is no automatic in-app process that deletes all Firebase account and team data.

## Cloud data that must be reviewed

When the data can be identified, associated cloud records are reviewed for deletion, minimization, anonymization or justified retention:

- Firebase Authentication account and Team Sync identity
- team membership, roles, display names, employee/internal numbers, roster names, unit roster numbers and team permissions
- FCM notification tokens linked to the user or team
- Team Schedule areas, member skills, assignments, member/name snapshots, notes, settings, day state, standby-member and publication metadata
- Team Schedule people added without the app and their optional notification e-mail/phone details
- shift swap requests and team requests, including vacation/sick-leave/free-day types, dates, optional notes, name snapshots and decision metadata
- Team task settings and updater audit metadata
- Team Tasks, saved customer records, private task contact phones, comments, task history and creator/assignee/completion/archive references
- Projects, project tasks and project activity events, including member/actor identifiers and name snapshots
- Team QR assets and Team attendance check-in/check-out records, current attendance state and related member/workplace/asset references
- other cloud records linked to Team Sync

Deletion or minimization of shared records depends on the request, other team members' data, operational continuity, security and legal obligations. A record may be retained with personal fields minimized when deleting the entire shared record would affect other users or team history.

Leaving a team or archiving a team does not delete cloud data. An archived team remains stored and becomes read-only for normal team operations.

## Team Schedule mutation receipts

Successful Team Schedule assignment mutations create receipts that can contain the acting user's Firebase UID, Team ID, mutation and assignment identifiers, action, request fingerprint, result state and timestamp.

These receipts support idempotent retry/reconciliation and provide mutation audit context. The fingerprint is a request digest, not a copy of free-text notes.

Every relevant deletion request requires an explicit decision to retain, minimize or delete matching receipts. Receipts must not be deleted blindly: removing a successful receipt can allow an old mutation ID to be processed again, while altering identity, fingerprint or result fields can break exact replay validation. Any justified change requires a reviewed procedure that preserves replay safety. Retained personal identifiers and the reason for retention must be recorded in the request outcome.

## Local and device data

Most WorkCycle data is stored only on your device. This can include:

- Work Log events, notes, recognized-time calculations and manual correction data
- Local pickups
- Travel Orders
- Fleet / vehicle data such as vehicle display name, registration number, VIN, odometer entries, document/reminder metadata, service/maintenance metadata and notes
- Work Profile / Workplace / Unit information and manually entered work location/address details
- local schedules, status labels, app settings and widget settings
- local backup or export files that you create, such as WorkCycle ZIP backups or Work Log CSV exports where available
- device-local Team helper data such as active/known-team information, pending retries, a cached personal Team Schedule view, deadline shortcuts and recent Team task templates

If Team features were used, the Firebase SDK may also keep an offline device cache of team data previously opened in the app.

The developer cannot remotely delete local data or a Firebase offline cache from your device. Remove it by clearing WorkCycle app data in Android settings or uninstalling the app. Delete local backup/export files and relevant Android backup copies separately where applicable.

Uninstalling the app or clearing app data does not automatically delete cloud/team data already stored in Firebase. Cloud data still requires the verified manual process described above.

Fleet / Vozni park is local-only in the current release. It does not use GPS tracking, does not upload document files or driver-license scans, and does not sync vehicle data to Firebase.

## What may be retained

Some data may be retained when required for security, abuse prevention, debugging, legal compliance, shared team history or team continuity.

Team Task, Team Schedule, shift swap, team request, Project, attendance and comment records may be retained, minimized, anonymized or kept as deleted placeholders depending on the request and team context. Where practical, personal identifiers and free-text details will be removed or minimized.

Mutation receipts may be retained when necessary for idempotency, retry safety or audit integrity. The retention decision and any remaining personal identifiers must be documented when handling the request.

Anonymized or non-identifiable records may be retained when they can no longer be linked to a specific person.

## Timing

Deletion requests are normally processed within 30 days after the request can be verified and the relevant data can be identified. If a shared record cannot be deleted as requested, the response should explain whether it was retained, minimized or anonymized and why.

## Privacy policy

For more information, see [PRIVACY_POLICY.md](PRIVACY_POLICY.md).
