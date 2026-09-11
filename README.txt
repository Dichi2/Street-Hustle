STREET HUSTLE — ANDROID + ONLINE BACKEND BUILD

Version 2.0 adds the missing production foundation around the original prototype:
- Secure account registration and login with server-side bcrypt password hashing.
- Unique game name + email accounts so progress can follow a player across devices.
- Email verification and password recovery via SMTP (or development token logging).
- Login throttling/temporary lockout and session invalidation after password reset/logout-all.
- Server-side game state and server-authoritative core actions for jobs, travel, purchases,
  sales, investments and disputes, rather than trusting arbitrary client balance edits.
- Cloud save/load, global leaderboard, player marketplace and player contract foundation.
- Major starting cities across Africa, Europe, North America, South America, Asia and Oceania.
- Offline test mode remains available, but offline progress is device-only and is not secure for competition.
- No real-money cash-out: Street Exchange is virtual in-game currency only.

WHAT STILL REQUIRES YOUR EXTERNAL SERVICES / CONFIGURATION
- Deploy backend/server.js and set a strong JWT_SECRET.
- Configure HTTPS and CORS_ORIGIN for your production game domain/app.
- Configure SMTP so verification and password-reset emails are actually delivered.
- For a production-scale game, move from SQLite to PostgreSQL and add Redis/queues, monitoring,
  backups, moderation/admin tools, transactional ledgers and stronger anti-fraud telemetry.
- Google Play Billing/signing, push notifications, analytics and crash reporting require your own
  Google Play/Cloud project credentials and product IDs; they are intentionally not fabricated here.

ANDROID BUILD
1. Open this folder in Android Studio, or use GitHub Actions.
2. GitHub Actions installs Gradle 8.9 and runs :app:assembleDebug.
3. The APK is a DEBUG/test APK. For Play Store release, create a release keystore and signing setup.

BACKEND BUILD
cd backend
cp .env.example .env
npm install
node server.js

The APK's Me -> Backend screen accepts your deployed HTTPS API base URL.

VERSION 3.0 ADDITIONS
- Android INTERNET permission for online backend connectivity.
- Idempotency keys for game actions to reduce accidental double submissions.
- Transaction/activity ledger for auditing player economy actions.
- Daily rewards, bank deposit/withdraw and account activity UI.
- Achievement API foundation.
- Protected admin metrics endpoint using ADMIN_KEY.
- Production environment template and launch checklist.
- Release APK GitHub Actions workflow with keystore secrets; no signing credentials are committed.

EXTERNAL ITEMS THAT CANNOT BE CREATED WITHOUT YOUR ACCOUNTS/SECRETS
- Your real SMTP account, production HTTPS domain/server, database hosting, Play Console account,
  Firebase project credentials, payment product IDs and release keystore. The project contains
  configuration points and documentation for these instead of fake credentials.


## v4 gameplay update
See CHANGELOG_V4.md for the latest mission, heat, and reliability improvements.
