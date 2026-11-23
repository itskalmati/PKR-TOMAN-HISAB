# PKR Toman Hisab (Android project)

This is an Android Studio project wrapping the offline PKR–Toman ledger in a native Android WebView.

## Features
- Buy Toman: enter PKR paid and Toman-per-PKR rate; Toman quantity is calculated.
- Sell Toman: enter Toman sold and rate; PKR received is calculated.
- Moving weighted-average cost in PKR per Toman.
- Realized profit/loss in PKR on each sale.
- Current Toman stock and remaining inventory cost.
- Daily/overall dashboard, transaction history, edit/delete.
- Local device storage (WebView localStorage).
- JSON backup/restore and CSV export.

## Rate convention
A rate of 930 means 1 PKR = 930 Toman.
BUY: Toman = PKR paid × rate.
SELL: PKR received = Toman sold ÷ rate.
Profit on sale = PKR received − moving-average PKR cost of Toman sold.

## Build APK
1. Open this folder in Android Studio (Giraffe or newer).
2. Let Android Studio sync Gradle and install the Android SDK Platform 35 if prompted.
3. Select Build > Build Bundle(s) / APK(s) > Build APK(s).
4. APK will be under `app/build/outputs/apk/debug/app-debug.apk`.

## Important
This workspace contains the complete Android source project, not a compiled/signed APK. Build it in Android Studio to produce the installable APK. No network permission is requested; transaction data stays on this device. Export backups regularly. Clearing app data or uninstalling can remove locally stored transactions.

## Accounting note
The app uses moving weighted-average inventory costing. Sales are valued at the average PKR cost immediately before each sale. Fees, commissions and transfer costs are not yet included in net profit.
