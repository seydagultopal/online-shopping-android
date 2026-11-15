# Online Shopping Android App

A Java-based Android shopping application prototype. The currently published repository snapshot contains catalogue data and reusable cart/persistence helpers.

> **Repository status:** This public snapshot is incomplete as a standalone Android Studio project. The Gradle wrapper/build files, Android manifest, and complete conventional Android source tree are not present, so a reproducible app build cannot currently be verified from this repository alone.

## What is represented in the source

- Product catalogue data with categories, product descriptions, prices, ratings, and reviews.
- Product and banner image references hosted in Firebase Storage.
- A cart-management helper (ManagmentCart) for adding items, updating quantities, removing items, and calculating the cart total.
- Local cart persistence through Android SharedPreferences, with object serialization handled by Gson via TinyDB.

## Technology visible in the repository

- Java
- Android SDK APIs, including Context and SharedPreferences
- Gson
- Firebase Storage asset URLs referenced by the catalogue data

The current files do not provide enough project configuration to verify the complete Android dependency set or Firebase integration workflow.

## Repository contents

| File | Purpose |
|---|---|
| ManagmentCart.java | Cart operations and total calculation |
| TinyDB.java | SharedPreferences persistence and Gson object serialization |
| project175.json | Sample banners, categories, products, and reviews, including image URLs |

## Current limitations

- Android Gradle build files and wrapper are not present in the published snapshot.
- The Android manifest and complete application source hierarchy are not present.
- No automated tests or reproducible build instructions are included.
- Firebase Storage URLs are embedded in the sample catalogue. Review their access settings; if their download tokens were not intended to be public, rotate them and replace the references.
- The cart is stored locally on the device; this repository does not demonstrate server-side cart synchronisation or checkout/payment processing.

## Restoring a reproducible Android project

To make this repository buildable, restore the original Android Studio project structure, including:

1. Root and app-level Gradle configuration plus the Gradle wrapper.
2. settings.gradle and Android manifest.
3. Complete Java source packages and required resources.
4. A documented Firebase setup using environment-specific configuration rather than committed private credentials.
5. Unit or instrumentation tests for cart operations and persistence.

Once those files are restored, document the minimum Android Studio version, JDK/Gradle/Android Gradle Plugin versions, required SDK level, and exact build/run commands here.

## License

No repository-level license is currently provided. The existing TinyDB.java file includes an Apache License 2.0 notice; preserve that attribution and its license terms if the file is retained or modified. No broader license for this repository is implied.
