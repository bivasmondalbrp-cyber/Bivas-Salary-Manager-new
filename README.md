# Bivas Salary Manager Android project

This project contains the offline attendance and salary calculator and a GitHub Actions workflow to build a debug APK.

## Build in GitHub
1. Upload the contents of this ZIP to the root of the intended GitHub repository (replace the unrelated placeholder app files only after checking them).
2. Open **Actions** and run **Build Android APK** (or push to `main`/`master`).
3. Open the completed workflow run and download the `Bivas-Salary-Manager-APK` artifact.

## Salary rules implemented
- Daily basic = monthly basic / 25.
- Hourly rate = daily basic / daily duty hours.
- Required hours = count of Normal days × daily duty hours.
- Sunday/Holiday work hours count fully as OT; Normal-day OT is time beyond daily duty hours.
- Shortfall is adjusted against the configured CL hours first; remaining shortfall is deducted at the hourly rate.
- 1st payment = basic − EPF − Mediclaim − Professional Tax − remaining shortfall deduction.
- 2nd payment = OT amount only (CL is not added a second time).
- Worked, Regular and OT time are shown as hours and minutes.
- Monthly attendance is stored separately on the device; changes are auto-saved locally.

## Important
The time-entry password is a basic on-device edit lock, not strong device/account security. Do not rely on it to protect highly sensitive information. Data is stored in the app's local storage on this device; back it up regularly.
