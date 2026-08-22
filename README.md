# Stock & Billing Android App — v2

Native Android starter using Kotlin + Jetpack Compose + Room.

## Added in v2
- Camera barcode scanner using ML Kit
- Automatic barcode reading
- Product barcode field
- Purchase rate, selling rate, MRP and expiry fields
- Batch/expiry-ready product model
- Stock decreases automatically when a bill is saved
- Estimated profit shown on billing screen

## Important limitation
A normal EAN/UPC barcode generally identifies a product; it does **not** universally contain MRP, purchase rate or expiry. To fetch those automatically, production mode should use:
1. GS1-encoded barcodes where those fields are encoded,
2. OCR from the package label for MRP/expiry, and/or
3. a product database/API.

The current scanner reads the barcode reliably and stores it. The next production step is to connect the barcode to OCR/database lookup and a batch-wise stock ledger so profit is calculated from the actual purchase cost of the exact batch sold.

Open in Android Studio, sync Gradle, and run on an Android phone with camera permission.
