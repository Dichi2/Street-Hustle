# Street Hustle v4.0.0

This build continues the game beyond the account/economy foundation.

## New gameplay systems
- Mission and achievement-style objectives with server-validated rewards.
- Heat/reputation pressure system. Legitimate delivery jobs reduce heat; laying low costs 250 SC and reduces heat by 15.
- Heat affects delivery-job payout, creating a meaningful risk/reward loop.
- Mission screen with eight progression objectives.
- Online game actions now send an idempotency key from the client, making retries safer.
- Offline mode includes mission tracking and heat.

## Existing systems retained
- Accounts, email verification, password reset and session invalidation.
- Cloud saves and server-authoritative economy actions.
- Banking, daily rewards, contracts, marketplace, virtual exchange, travel, leaderboard, disputes and activity ledger.
- GitHub Actions APK build.

## Still required for a production launch
- Deploy backend behind HTTPS.
- Configure SMTP and production secrets.
- Add real multiplayer transport/presence (WebSocket or equivalent) and authoritative matchmaking.
- Configure Play Console signing/release credentials.
- Add production database/backup/monitoring strategy if scaling beyond a single-server SQLite deployment.
