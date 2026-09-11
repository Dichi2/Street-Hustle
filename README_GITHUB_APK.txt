STREET HUSTLE — GITHUB APK + ONLINE BACKEND

ANDROID APK
1. Create/open a GitHub repository named Street-Hustle.
2. Upload the complete project, including .github/workflows/build-apk.yml.
3. Open Actions -> Build Street Hustle APK -> Run workflow.
4. Wait for the green check.
5. Open the run -> Artifacts -> Street-Hustle-APK.
6. Download the artifact ZIP and install app-debug.apk on Android.

ONLINE MODE
The APK is now prepared to talk to the backend in /backend.
1. Deploy backend/server.js on an HTTPS Node.js service.
2. Configure .env from .env.example.
3. Set a JWT_SECRET of at least 32 random characters.
4. Configure SMTP_HOST/SMTP_USER/SMTP_PASS/MAIL_FROM for real verification and reset emails.
5. Put the backend URL into Street Hustle -> Me -> Backend.
6. Create an account and verify the email.

IMPORTANT
- Never commit .env, passwords, JWT secrets, SMTP passwords, or production database files.
- Offline Mode is only a local test mode. It does not provide cross-device saves or secure competitive play.
- The server validates the main economy actions. A complete commercial MMO-scale anti-cheat system still needs
  server-authoritative handling for every gameplay action, immutable transaction/event logs, moderation and monitoring.
- Real-money purchases/Google Play Billing are not activated because they require your own Play Console product IDs,
  merchant setup and signing credentials.
