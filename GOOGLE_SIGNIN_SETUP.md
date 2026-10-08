# Google Sign-In Setup (StudyNote)

1. Firebase Console (https://console.firebase.google.com) ma project banaunuhos.
2. Android app thapnuhos — package name: `com.aistudio.studynote.vqlxpt`
3. SHA-1 fingerprint thapnuhos:
   `./gradlew signingReport`  (debug ra release dubai ko SHA-1 halnuhos)
4. `google-services.json` download garera `app/` folder bhitra rakhnuhos.
5. Authentication > Sign-in method > **Google** Enable garnuhos.
6. Tyahi Google provider bhitra "Web SDK configuration" ko **Web client ID** copy garnuhos.
7. Project root ma `.env` file banayera:
   GOOGLE_WEB_CLIENT_ID=xxxxxxxx.apps.googleusercontent.com
8. Android Studio ma Sync > Run.

Sign out: Settings tab ko mathi Account card ma "Sign out".

## Cloud Sync (Firestore) setup
9. Firebase Console > Build > **Firestore Database** > Create database (production mode).
10. Rules tab ma project root ko `firestore.rules` file ko content paste garera **Publish** garnuhos.
    (Yasle har user lai aafno matra data padhna/lekhna dinchha.)
11. App ma sign in garepachhi notes aafai sync hunchhan. Settings > Cloud Sync ma status ra "Sync now" chha.
