# Delete your TTT account

Last updated: 2026-05-04

Hosted at: https://whompster.github.io/ttt-legal/delete_account.html

This page explains how to delete your account and the personal data
associated with it in the **TTT** mobile app
(`com.whompster.ttt.client`), published by Håkon Strand Aandahl.

## How to request account deletion

Send an email to **whompster101+legal@gmail.com** with:

- **Subject**: `Account deletion request`
- **Body**: include the email address you signed up with so we can
  identify your account.

We respond within **30 days** of receiving the request, per GDPR
Article 12 obligations.

(In-app deletion is on the roadmap. Until that ships, the email route
above is the one supported method.)

## What gets deleted

When your deletion is processed, the following are removed from our
servers:

- Your account record in Supabase Auth (email address, password hash,
  user ID).
- Your profile (display name, handle).
- Your match history, scores, and any friend relationships.
- Any private rooms you created.

## What is retained, and for how long

- **Telemetry events** (the lightweight diagnostic events described in
  the privacy policy) are anonymised within **30 days** of account
  deletion — the `device_id` field is zeroed so events can no longer
  be linked back to you.
- **Firebase Crashlytics crash reports** are retained for **90 days**
  per Google's defaults, then aggregated. We do not call Firebase's
  `setUserId` API, so crash reports were never linked to your account
  in the first place — they cannot be removed individually.

## Other rights

To request access, correction, portability, or to object to
processing, see the
[Privacy Policy](https://whompster.github.io/ttt-legal/privacy_policy.html)
or contact us at the same email above.
