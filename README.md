# SIGNAL — Student Search Mobile

A mobile-first Flutter conversion of **Student Search Tool v16**.

## What was carried over
- Student name search
- Other-details search with selectable scope
- Exact text / Contains
- Similar spelling
- Field-group filters
- Multi-select filter values
- Numeric ranges
- Date matching
- Student detail view
- TXT export + phone share
- Dark/light mode
- 4,490 student records and 81 labelled fields from the v16 dataset

## Mobile UI
This is intentionally **not a shrunken desktop UI**. Results are touch-friendly cards, filters open as a bottom sheet, student records open in a detail sheet, and save/export is optimized for a phone.

## Build an APK online — no Flutter installation needed
### GitHub Actions
1. Create a new GitHub repository.
2. Upload this whole project to it.
3. Push to the `main` branch, or open **Actions → Build SIGNAL APK → Run workflow**.
4. When the workflow finishes, open the run and download the **signal-student-search-apk** artifact.

The workflow creates the Android platform files in the cloud, so this ZIP does not need a local Android Studio installation.

### Codemagic
You can also connect the repository to Codemagic. The included `codemagic.yaml` builds `app-release.apk` in the cloud.

## Important privacy note
The current mobile build bundles the v16 student dataset inside the app so it works offline. Treat the APK as private. If the app will be distributed to other people, the next version should read the data from your existing Render API instead of shipping the raw student records inside the APK.
