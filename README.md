# ttt-legal

Public-facing legal documents for the [TTT](https://github.com/Whompster/ttt-client)
mobile app — privacy policy, terms of service, and EULA — served via
GitHub Pages at
[whompster.github.io/ttt-legal](https://whompster.github.io/ttt-legal/).

This repo exists separately from the (private) client + server repos so
that:

- The docs live on GitHub's infrastructure rather than behind a
  self-hosted tunnel — they stay reachable when the home VM is offline
  or the ISP does maintenance, which is what Play Console wants from a
  privacy-policy URL.
- The client and server source repos can stay private without paying
  for GitHub Pro just to surface a few markdown files publicly.

## Updating

Edit the `.md` files at the repo root, commit, push to `main`. Pages
rebuilds within a couple of minutes.

The `Last updated:` date at the top of each doc should be bumped to
match. Material changes (data collection, retention, governing law)
should be reflected in the corresponding fields on the Play Console
Data Safety form too.
