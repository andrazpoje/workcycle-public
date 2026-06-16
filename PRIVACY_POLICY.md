# Privacy Policy

Last updated: June 16, 2026

This Privacy Policy applies to the Android app **Delovni cikel**, also known as **WorkCycle**, package name **com.dante.abworkdaywidget**, published on Google Play by **Dante produkcija**.

WorkCycle is designed so the core local features stay usable without sign-in or cloud sync. Team/cloud features are optional. If you do not create or join a team, you can use the app locally without Team Sync.

## Local data stored on your device

WorkCycle stores local app data using Android local storage, including SharedPreferences and Room database storage.

Local data may include:

- schedules, cycles, statuses and calendar settings
- Work Log entries and notes
- Local pickups
- Travel Orders
- vehicle settings for Travel Orders
- widget and app settings
- Workplace / Unit information
- local backup or export files that you choose to create

Work Log, Local pickups, Travel Orders, vehicles, local schedules, local status labels, widget settings and most settings are not automatically shared with a team.

## Work Log

Work Log is an optional local record of actual work events. Raw Work Log events are the source of truth for work-time evidence. Work Log records, notes, recognized-time calculations and manual correction data remain on your device unless you explicitly export or back up that data yourself.

Work Log is separate from Team Schedule. Team Schedule assignments may be shown in personal schedule views as display-only information, but they do not write local status labels, local schedule overrides or Work Log records.

## Optional team/cloud features

If you enable team/cloud features by creating or joining a team, WorkCycle uses Firebase services:

- Firebase Authentication for the app user identity
- Cloud Firestore for team data, team members, Team Schedule and Field Tasks / Team Tasks
- Firebase Cloud Messaging for team notifications when notification features are enabled

Team/cloud features may store and sync data such as:

- active team information
- team membership, roles, permissions and settings
- team member display names, statuses and roster metadata such as roster name and unit roster number
- Team codes used for joining a team
- Team Schedule work areas, member skills, assignments, work statuses, daily standby member, settings and published/unpublished day state
- Field Tasks / Team Tasks, assignments, completion, comments, coordination notes and history data
- notification-related metadata such as Firebase Cloud Messaging tokens when notification features are enabled

Team Schedule, Field Tasks / Team Tasks and team comments are shared with the active team according to team role, permissions and feature settings. Comments and task details should be used for short operational coordination, and users should avoid entering sensitive personal data unless it is needed for the team work. Deleted comments may remain as deleted placeholders so the team conversation stays understandable.

Member visibility settings may affect how the app displays Team Schedule information to other team members. These settings should not be treated as end-to-end encryption or field-level server-side privacy for every field. Do not enter sensitive absence or health details unless they are needed for the team planning workflow.

Local Work Log data, local schedules, local status labels, Local pickups, Travel Orders, vehicles and local widget settings are not automatically shared with Team Sync.

## Sign-in and account linking

Team Sync can use an anonymous Firebase identity. Linking a Google account is optional and can help recover the same team identity after reinstalling the app or changing phones.

Your email is not shown to other team members in the normal team member list.

## Notifications

If team notifications are enabled, WorkCycle may store a Firebase Cloud Messaging token so notifications can be delivered to your device.

Notifications may include basic team task information. Delivery can depend on notification permission, device settings, internet connection and battery restrictions.

## Third-party services

WorkCycle uses Firebase for optional Team Sync, authentication, cloud storage of team data and team notifications.

WorkCycle does not use advertising tracking or sell user data.

## Administrator access to cloud data

The app author or an authorized Firebase project administrator can technically access cloud-stored team data. Such access is limited to cases where it is necessary for service operation, support, debugging, security, abuse prevention, maintenance, or legal obligations. Cloud data is not inspected without a relevant operational, support, security, or legal reason.

Local-only data stored on your device is not automatically available to the developer.

## Data sharing

Data is shared only as needed for optional team/cloud features that you choose to use. Team data is visible to members of the same team according to their team role, permissions and feature settings.

WorkCycle does not sell your data.

## Account and data deletion

To request deletion of cloud account or Team Sync data, send an email to danteprodukcija@gmail.com with the subject "WorkCycle data deletion request".

For details, see [DATA_DELETION.md](DATA_DELETION.md).

Local-only data can be removed from your device by clearing app data, deleting local backup/export files, or uninstalling the app. Cloud/team data requires a cloud account, team or support deletion process.

## Contact

For privacy questions or data deletion requests, contact:

**Dante produkcija**  
App: **Delovni cikel / WorkCycle**  
Package name: **com.dante.abworkdaywidget**  
Email: danteprodukcija@gmail.com


