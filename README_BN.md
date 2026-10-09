# TukTuk Ads Simulator — Android App Project

এই প্রজেক্টে TukTuk Meta Ads Simulator V6-কে Android WebView অ্যাপের মধ্যে রাখা হয়েছে। HTML ফাইল অ্যাপের ভেতরেই থাকে; অ্যাপ চালাতে আলাদা ওয়েবসাইট/ইন্টারনেট লাগে না। WebView local storage-এ সংরক্ষিত ডেটা অ্যাপের পরেরবার খোলার সময়ও থাকার কথা।

## APK বানানোর ধাপ
1. কম্পিউটারে Android Studio ইনস্টল করুন।
2. Android Studio খুলে **Open** নির্বাচন করুন এবং এই ফোল্ডারটি (`TukTukAdsSimulatorAndroid`) খুলুন।
3. Gradle sync শেষ হওয়া পর্যন্ত অপেক্ষা করুন; SDK Platform 35 এবং JDK 17 প্রয়োজন হতে পারে।
4. **Build → Build Bundle(s) / APK(s) → Build APK(s)** নির্বাচন করুন।
5. Build সফল হলে Android Studio-র notification থেকে **Locate** চাপুন। APK সাধারণত `app/build/outputs/apk/debug/app-debug.apk`-এ থাকবে.
6. APK Android ফোনে পাঠিয়ে ইনস্টল করুন. Unknown apps permission চাইলে নিজের তৈরি APK-এর জন্য অনুমতি দিন.

## নোট
- App name: TukTuk Ads Simulator
- Credit: Developed by Tipu / © Copyright Tipu (HTML UI-তে আছে)
- CSV/JSON export Android-এর Downloads ফোল্ডারে সেভ হবে (Android 10+).
- Restore Backup JSON চাপলে Android file picker খুলবে.
- Meta Ads live API integration নেই; actual ad data ম্যানুয়ালি লিখতে হবে.
- পুরোনো ব্রাউজারের localStorage ডেটা স্বয়ংক্রিয়ভাবে অ্যাপে স্থানান্তর হবে না. আগে browser থেকে JSON backup export করে রাখুন; তারপর অ্যাপে Restore Backup JSON ব্যবহার করে import করার চেষ্টা করুন.
