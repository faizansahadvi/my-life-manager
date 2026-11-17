MY LIFE MANAGER PRO — SETUP GUIDE (Roman Urdu)

1) ZIP extract karein. Andar My_Life_Manager_Pro folder hoga.
2) Folder ke tamam files/folders GitHub repository ke ROOT mein upload karein. index.html root par hona chahiye.
3) GitHub > Repository > Settings > Pages > Deploy from a branch > main > /(root) > Save.
4) GitHub Pages ka HTTPS link open karein. Chrome mein Install app / Add to Home Screen karein.
5) Pehli dafa app online khol kar load hone dein. Phir offline mode test karein.

FEATURES INCLUDED:
- Offline PWA shell + IndexedDB local records
- Income, household, personal, other expense records
- Person-wise lending/borrowing ledger with WhatsApp/SMS/copy confirmation message after each entry
- Photo and voice evidence attachments on transaction and person ledger entries
- Per-person shareable text statement with running outstanding balances
- Ledger payment method and reference number fields
- Salary settings and salary payment history
- Overtime hours/minutes/rate/multiplier calculator
- Budgets, savings goals, reports, CSV, print/PDF
- Full JSON backup including attachment data; restore merges by record ID
- Light and Dark theme toggle

IMPORTANT LIMITATIONS:
- This is a functional first Pro build, not audited financial software.
- Lending ledger currently records entries and calculates net balances. It does not yet enforce repayment caps against original loans or maintain a formal allocation of each partial repayment to a specific loan.
- Google Drive automatic sync is NOT implemented. Download backup and upload it manually to Drive.
- Local records can be lost if browser storage is cleared, browser is uninstalled, or device is lost. Keep backups.
- Voice recording requires HTTPS or localhost and microphone permission. GitHub Pages uses HTTPS.
- Camera/gallery photo selection depends on browser/device permissions.
- Install PWA after first online load. Offline support covers app shell; external font may not load offline.
- No account/login or server sync. Data stays in this browser profile.
- Before real use, test calculations and backup/restore with sample records.

EDITING:
- index.html = app structure and forms
- styles.css = visual design, responsive layout, light/dark colors
- app.js = database, calculations, features and interactions
- sw.js = offline cache; update CACHE name after changing cached app files to force refresh
- manifest.webmanifest = install name, icon and app display settings

When changing code, keep a separate backup of your data JSON and the full project ZIP.

VERSION 1.1 — LEN DEN MESSAGE UPGRADE
- After saving a lending/borrowing/repayment entry, a confirmation message is generated automatically.
- Choose Open WhatsApp, Open SMS, native Share, or Copy. Nothing is sent automatically; you review and tap send in the chosen app.
- Person cards now include Share statement. The statement includes all saved entries and current receivable/payable balances.
- Phone numbers are normalized for WhatsApp links; Pakistani numbers beginning with 03 are converted to 92 format.
- Existing IndexedDB database name and version are preserved. This update is additive and does not intentionally reset existing records.
- Service worker cache version was increased so the browser can fetch the updated application files.

UPGRADE SAFETY:
1) Before replacing files on GitHub, use the app's Backup & Restore > Download full backup.
2) Keep your existing project folder/ZIP as a separate copy.
3) Upload the updated project files to the SAME GitHub repository, replacing matching source files. Do not delete or recreate the repository.
4) Refresh the hosted app. If old code remains, close the app and do a hard refresh / clear only the site cache (not site data).
5) Do not clear site data or browser storage; that can erase IndexedDB financial records.
