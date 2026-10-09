# ফোন দিয়ে APK বানানোর গাইড

এই প্রজেক্টে GitHub Actions workflow যোগ করা আছে। এটি GitHub-এর cloud computer-এ Android APK তৈরি করবে; ফোনে Android Studio লাগবে না।

## ধাপ
1. ZIP ফাইলটি ফোনে ডাউনলোড করে Extract করুন। Extract করার পর `TukTukAdsSimulatorAndroid` ফোল্ডারের ভেতরের ফাইলগুলো ব্যবহার করতে হবে।
2. ব্রাউজারে github.com খুলে সাইন ইন করুন বা অ্যাকাউন্ট তৈরি করুন।
3. নতুন repository তৈরি করুন, নাম দিন `tuktuk-ads-simulator`, চাইলে Private রাখুন।
4. repository-র **Add file → Upload files** থেকে `TukTukAdsSimulatorAndroid` ফোল্ডারের ভেতরের সব ফাইল ও `.github` ফোল্ডার আপলোড করুন। `.github/workflows/build-apk.yml` যেন ঠিক ওই পথেই থাকে। মোবাইলে hidden `.github` ফোল্ডার আপলোড করা অসুবিধা হলে ZIP-টি আগে Extract করে এমন ফাইল ম্যানেজার ব্যবহার করুন যা hidden folder দেখায়।
5. সব ফাইল `main` branch-এ commit করুন। Push workflow স্বয়ংক্রিয়ভাবে চলবে। না চললে repository-র **Actions** ট্যাব → **Build TukTuk Ads Simulator APK** → **Run workflow** চাপুন।
6. Actions-এ চলমান build খুলে সবুজ tick হওয়া পর্যন্ত অপেক্ষা করুন। তারপর ওই run-এর নিচে **Artifacts** অংশ থেকে `TukTuk-Ads-Simulator-APK` ডাউনলোড করুন।
7. ZIP artifact Extract করে `app-debug.apk` ফাইলটি খুলে install করুন। Android চাইলে এই উৎস থেকে install করার অনুমতি দিন।

## নোট
- প্রথমবার APK install করতে Android-এর “Install unknown apps” অনুমতি চাইতে পারে। শুধুমাত্র নিজের তৈরি/বিশ্বস্ত APK-র জন্য অনুমতি দিন।
- এটি debug APK, Play Store release package নয়।
- এই build প্রজেক্টের বর্তমান source-কে compile করবে; build সফল হলেই সব ফিচার ফোনে পুরোপুরি পরীক্ষা হয়েছে—এমন নয়।
