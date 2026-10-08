# Privacy Policy

Last updated: October 8, 2026

This Privacy Policy applies to the Android app **Delovni cikel**, also known as **WorkCycle**, package name **com.dante.abworkdaywidget**, published on Google Play by **Dante produkcija**.

WorkCycle is designed so its core local features remain usable without sign-in or cloud sync. Team/cloud features are optional. If you do not create or join a team, you can use the app locally without Team Sync.

## Local data stored on your device

WorkCycle stores local app data using Android local storage, including SharedPreferences and Room database storage.

Local data may include:

- schedules, cycles, statuses, labels and calendar settings
- Work Log events, notes, recognized-time calculations and manual correction data
- Local pickups
- Travel Orders
- Fleet / vehicle data such as vehicle display name, registration number, VIN, manual odometer entries, document/reminder metadata, service/maintenance metadata and notes
- widget and app settings
- Work Profile / Workplace / Unit information and manually entered work location or address details
- local backup or export files that you choose to create, such as WorkCycle ZIP backups or Work Log CSV exports where available
- device-local Team helper data, such as active-team and known-team information, pending Team attendance or Team Schedule retries, a cached personal Team Schedule view, deadline shortcuts and recent Team task templates; recent templates may contain task titles, customer names, addresses and task details

If you use team/cloud features, the Firebase SDK may also keep an offline cache on your device of team data you have opened. Clearing app data or uninstalling the app removes this device cache but does not delete the corresponding cloud data.

Depending on Android system backup settings and WorkCycle backup rules, selected local settings may be included in Android system cloud backup. Android device-to-device transfer may include additional local schedule/settings data and the local Room database, including Work Log evidence. These Android mechanisms are separate from Team Sync/Firebase and are controlled by Android or device settings.

Work Log, Local pickups, Travel Orders, Fleet, local schedules, local status labels, widget settings and most other local settings are not automatically uploaded to WorkCycle Cloud. They can leave the device if you explicitly export, back up, transfer or share them.

Fleet / Vozni park is local-only in the current release. It does not use GPS tracking, telematics or OBD data, does not upload document files or driver-license scans, and does not sync vehicle data to Firebase.

WorkCycle does not request location permission and does not collect GPS or live location data. Location and address fields in Work Profile, Travel Orders, Local pickups, Team Tasks, saved customer records or Team QR assets are manually entered text. Team QR/NFC attendance does not verify or record your location. Opening navigation or phone actions uses external apps only after user action.

## Device permissions

- Notifications are used for Work Log, schedule and optional team notifications.
- Run at startup (boot completed) is used to refresh widgets and reschedule local updates after a restart.
- NFC is used only while you use the QR and NFC scan screen to read a WorkCycle workplace or vehicle tag. WorkCycle does not write NFC tags. NFC is optional.
- QR scanning uses the Google Play services code scanner. WorkCycle does not request camera permission and receives only the scanned code value.
- WorkCycle does not request location, contacts, phone, SMS or broad file-storage permissions.

## Work Log

Work Log is an optional local record of actual work events. Raw Work Log events are the source of truth for work-time evidence. Work Log records, notes, recognized-time calculations and manual correction data remain on your device unless you explicitly export, back up, transfer or share them.

Work Log is separate from Team Schedule. Team Schedule assignments may be shown in personal schedule views as display-only information, but they do not write local status labels, local schedule overrides or Work Log records.

Work Log is also separate from Team QR/NFC attendance. Team check-in and check-out events are stored in WorkCycle Cloud for the team; they do not create local Work Log records, and local Work Log records are not uploaded as attendance records.

## Optional team/cloud features

If you enable team/cloud features by creating or joining a team, WorkCycle uses Firebase services:

- Firebase Authentication for app identity, including anonymous identity and optional Google account linking
- Cloud Firestore for team data, team members, Team Schedule, Team Tasks, Projects and Team attendance
- Firebase Cloud Functions for selected server-side team actions
- Firebase Cloud Messaging for team notifications when notification features are enabled
- Firebase App Check with Google Play Integrity to help protect cloud services from abuse

Depending on the features you use, team/cloud data may include:

- Firebase user identifiers and optional linked Google provider information
- team names, Team codes, owner/admin references, settings and permissions
- team membership, roles, statuses, display names, employee/internal numbers, roster names and unit roster numbers
- Team Schedule work areas, member skills, assignments, member name snapshots, work statuses, notes, standby-member references, settings and published/unpublished day state
- people added to Team Schedule without using the app, including their names, active/archive state and creator/updater references
- optional Team Schedule notification contacts, including e-mail, phone and notification preference; these contacts are readable only by the team owner, and sending notifications to them is not enabled in the current version
- shift swap requests, including proposer/target identifiers and name snapshots, assignment references, dates, optional notes, status and decision metadata; under normal in-app access, a shift swap is readable by the Team owner and by the proposing and target members, not by other team admins
- team requests such as vacation, sick leave, free day, preferred shift, field work or a general note, including dates, optional notes, requester identifiers and snapshots, status and decision metadata; under normal in-app access, a request, including sick-leave information and optional notes, is readable by the requesting member and the Team owner, not by other team admins
- Team task settings, including enabled/default task types and audit metadata such as updater UID and timestamp
- Team Tasks / Field Tasks, including title, location/address, phone, details, priority, deadline, task type, passenger-transport details, customer snapshots, assignment/completion/archive metadata, problem notes, comments, coordination notes and history
- saved customer records, including customer/contact names, addresses, phone numbers, aliases and creator/updater references
- a private Team Task contact phone, readable only by the team owner and the member assigned to that task
- Team Task history events, including action, actor UID and name snapshot, previous-assignee reference, task-type snapshot, app version and timestamp
- Projects, including project names/descriptions, manager/member identifiers and name snapshots, status and dates; project tasks can include titles, descriptions, due dates, responsible members, assignees and collaborators; project events include actor identifiers and name snapshots
- Team QR assets for workplaces or vehicles, including display name, vehicle registration where entered, active state, token version and creator/updater identifiers
- Team attendance check-in and check-out events created with Team QR/NFC, including member UID, session and workplace/QR asset references, server/device times, request ID, app version, check-out method and an optional override reason; current attendance state and the team's check-out policy are also stored; under normal in-app access, an attendance event and the affected member's current attendance state are readable by that member and by Team owners/admins, while approved Team members can read the Team check-out policy
- Team Schedule assignment mutation receipts containing actor UID, team/mutation/assignment identifiers, action, request fingerprint, result state and timestamp; the fingerprint is a digest rather than a copy of free-text notes, and receipts support idempotent retries and audit of assignment mutations
- Firebase Cloud Messaging tokens, device platform and app version when team notifications are enabled
- Firebase App Check / Play Integrity tokens and service metadata processed to protect Firebase services; WorkCycle does not store App Check tokens in Firestore

Team data is shared with members of the same team according to role, permissions and feature settings. Some records are restricted more narrowly, such as Team Schedule notification contacts and private Team Task contacts.

Team comments, requests, notes and task details should be used for operational coordination. Avoid entering sensitive personal or medical details unless needed for the team workflow. Deleted comments may remain as deleted placeholders so the team conversation stays understandable.

Member visibility settings affect how the app displays Team Schedule information. They are not end-to-end encryption or field-level server-side privacy for every stored field.

WorkCycle does not upload files, photos or document scans to WorkCycle Cloud.

## Sign-in and account linking

Team Sync can use an anonymous Firebase identity. Linking a Google account is optional and can help recover the same team identity after reinstalling the app or changing phones.

Your e-mail is not shown in the normal team member list. If you link a Google account, Firebase Authentication and Google process the account identifiers needed for sign-in and linking.

## Notifications

If team notifications are enabled, WorkCycle may store a Firebase Cloud Messaging token so notifications can be delivered to your device.

Notifications may include basic Team Task information. Delivery can depend on notification permission, device settings, internet connection and battery restrictions.

## Third-party services

WorkCycle uses Firebase for optional authentication, team cloud storage, Cloud Functions, App Check and notifications. Firebase and Google services may process identifiers and service metadata needed for authentication, database access, messaging, diagnostics, security and abuse prevention.

WorkCycle does not use advertising tracking or sell user data.

## Administrator access to cloud data

The app author or an authorized Firebase project administrator can technically access cloud-stored team data. Such access is limited to cases where it is necessary for service operation, support, debugging, security, abuse prevention, maintenance or legal obligations. Cloud data is not inspected without a relevant operational, support, security or legal reason.

Local-only data stored on your device is not automatically available to the developer.

## Data sharing

Data is shared only as needed for optional team/cloud features that you choose to use. Team data is visible according to team role, permissions and feature settings. Firebase and Google process data as service providers for the functions described above.

WorkCycle does not sell your data.

## Account and data deletion

To request deletion or minimization of a cloud account or Team Sync data, send an e-mail to danteprodukcija@gmail.com with the subject "WorkCycle data deletion request". The app also includes an Account and data deletion screen that can prepare identifying details for the request.

For details, see [DATA_DELETION.md](DATA_DELETION.md).

Deletion of cloud/team data is a verified manual process. The app does not provide automatic deletion of all cloud account and team data. Leaving or archiving a team does not delete its cloud data.

Shared team records may need to be retained, minimized or anonymized for team continuity, security, abuse prevention, support, legal obligations or shared-history consistency. Mutation receipts require an explicit retention/deletion decision because removing or altering them can undermine retry safety and audit history.

Local-only data can be removed from your device by clearing app data, deleting local backup/export files, removing relevant Android backup/transfer copies where applicable, or uninstalling the app.

## Contact

For privacy questions or data deletion requests, contact:

**Dante produkcija**  
App: **Delovni cikel / WorkCycle**  
Package name: **com.dante.abworkdaywidget**  
E-mail: danteprodukcija@gmail.com
