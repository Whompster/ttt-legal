# Privacy Policy

Last updated: 2026-05-04

Hosted at: https://whompster.github.io/ttt-legal/privacy_policy.html

## 1. Who we are

TTT ("we", "our", "us") is operated by Håkon Strand Aandahl.
If you have any questions about this policy, contact us at whompster101+legal@gmail.com.

## 2. What data we collect and why

### Account data (lawful basis: contract)
- **Email address and password hash** — collected when you create an account via Supabase Auth.
  Your password is hashed by Supabase before storage; we never see it in plaintext.
- **User ID (UUID)** — generated at registration, used to associate your game history.

### Game state (lawful basis: contract)
- **Match history, moves, scores, friend relationships** — stored server-side in a
  PostgreSQL database (Supabase Postgres) so you can resume games across devices.

### Telemetry events (lawful basis: legitimate interests)
We emit lightweight diagnostic events to help us identify crashes and usage patterns.
Each event carries:

```
{ ts, release, git_sha, event, app_version, platform, device_id, session_id, source: "client" }
```

- `device_id` is a randomly generated identifier stored locally on your device.
  It is NOT linked to advertising identifiers (IDFA / GAID).
- `session_id` resets on every app launch.
- No user-identifiable fields (name, email) are included in telemetry payloads.

### Crash diagnostics (lawful basis: legitimate interests)
When the app crashes, **Firebase Crashlytics** (a Google service) collects:
- The exception stack trace and code path that triggered the crash.
- Device model, OS version, app version, available memory at crash time.
- A randomly-generated **Firebase Installation ID** that identifies the
  app instance on your device. This is NOT linked to advertising
  identifiers (IDFA / GAID) and is not your account email or User ID.

We do **not** call Firebase's `setUserId` API, so crash reports cannot
be tied back to your TTT account. The data is sent over HTTPS to
Google's servers and processed under Google's
[Firebase data processing terms](https://firebase.google.com/terms/data-processing-terms).

## 3. What we do NOT collect
- We do not run any advertising SDK.
- We do not sell data to third parties.
- We do not collect location, contacts, camera, or microphone data.
- We do not use in-app purchases or payment data (none implemented).
- We do not call Firebase's `setUserId` API, so the diagnostic data above
  cannot be tied to your account.

## 4. Data storage and transfers
- Account and game data is stored in Supabase (EU region).
- Telemetry events are sent to our own backend at `https://ttt.whompster101.com`.
- Crash diagnostics are sent to Google Firebase Crashlytics (US region by
  default; Google may process at any of its data centres).
- Data may be processed in countries outside your own. By using the app you consent to this.

## 5. Data retention
- Account data is retained until you delete your account.
- Telemetry events are retained for 90 days then purged.
- Firebase Crashlytics retains crash data for **90 days**, after which
  reports are aggregated and anonymous counters are kept indefinitely
  per Google's defaults.

## 6. Your rights (GDPR and equivalent)
If you are in the EEA, UK, or another jurisdiction with data protection law, you have the right to:

- **Access** — request a copy of the personal data we hold about you.
- **Correction** — ask us to fix inaccurate data.
- **Deletion** — delete your account through the app (or contact us at whompster101+legal@gmail.com).
  Account deletion removes your profile and game history; telemetry events are
  anonymised (device_id zeroed) within 30 days.
- **Portability** — receive your data in a machine-readable format.
- **Object** — object to processing based on legitimate interests.

To exercise any right, contact us at whompster101+legal@gmail.com.
We will respond within 30 days.

## 7. Cookies and local storage
The app stores a session token in Android's EncryptedSharedPreferences /
iOS Keychain (platform secure storage). No browser cookies are used.

## 8. Children
The app is not directed at children under 13 (US) / 16 (EEA).
We do not knowingly collect data from children.

## 9. Changes to this policy
We will update the `Last updated` date at the top of this document when
the policy changes. Continued use of the app after a change constitutes
acceptance.
