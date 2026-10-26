# Bondhu AI — বাংলা AI সহকারী

একটি মোবাইল-ফ্রেন্ডলি বাংলা AI chat website। Node.js + Express backend ব্যবহার করে Gemini API-তে প্রশ্ন পাঠায়। API key কখনো frontend-এ রাখা হয় না।

## লোকাল কম্পিউটারে চালানো

1. Node.js 18 বা তার নতুন সংস্করণ ইনস্টল করুন: https://nodejs.org/
2. এই ফোল্ডারে টার্মিনাল খুলুন।
3. চালান: `npm install`
4. `.env.example` কপি করে `.env` নাম দিন।
5. Google AI Studio থেকে API key নিয়ে `.env`-এ `GEMINI_API_KEY=আপনার_কি` লিখুন: https://aistudio.google.com/apikey
6. চালান: `npm start`
7. ব্রাউজারে খুলুন: `http://localhost:3000`

## Render-এ লাইভ হোস্টিং (শুরু করার সহজ পথ)

1. GitHub-এ একটি নতুন repository তৈরি করুন।
2. এই ফোল্ডারের ফাইলগুলো repository-তে upload করুন। `.env` বা API key upload করবেন না।
3. https://render.com এ লগইন করে **New → Web Service** বেছে repository connect করুন।
4. Build Command: `npm install`
5. Start Command: `npm start`
6. Environment Variables-এ `GEMINI_API_KEY` নামে variable যোগ করুন এবং API key-এর মান দিন।
7. Deploy চাপুন। Deploy শেষ হলে Render-এর দেওয়া `https://...onrender.com` লিংক খুলুন।

Render-এর free plan-এর সীমাবদ্ধতা/ঘুমিয়ে যাওয়ার নিয়ম বদলাতে পারে। নির্দিষ্ট free hosting availability আগে যাচাই করুন। API provider-এর usage limits বা খরচও প্রযোজ্য হতে পারে।

## নিরাপত্তা

- API key শুধু hosting-এর Environment Variables-এ রাখবেন; HTML/JavaScript বা GitHub-এ নয়।
- এই starter app-এ IP-ভিত্তিক সাধারণ rate limit আছে, তবে এটি বড় public launch-এর জন্য পূর্ণাঙ্গ abuse protection নয়।
- জনসাধারণের জন্য চালুর আগে privacy policy, usage limits, monitoring এবং abuse controls যোগ করুন।

## Android-এ অ্যাপের মতো ইনস্টল করা

1. ওয়েবসাইট HTTPS-এ লাইভ করুন।
2. Android Chrome-এ সাইট খুলুন।
3. Chrome-এর তিন-ডট মেনু থেকে **Install app** বা **Add to Home screen** বেছে নিন (ব্রাউজারভেদে নাম আলাদা হতে পারে)।
4. মনে রাখবেন: অফলাইনে শুধু সাইটের মূল কাঠামো ক্যাশ থেকে খুলতে পারে; AI chat-এর জন্য ইন্টারনেট ও API key লাগবে।

## নিজের ডোমেইন যুক্ত করা

1. আগে ডোমেইন রেজিস্ট্রারের সাইটে নামটি পাওয়া যায় কি না যাচাই করে কিনুন। `.com` ডোমেইনের দাম রেজিস্ট্রার ও নবায়নের শর্ত অনুযায়ী বদলায়।
2. Render-এ আপনার Web Service খুলে **Settings → Custom Domains**-এ ডোমেইন যোগ করুন।
3. Render যে DNS record দেখাবে, সেটিই ডোমেইন রেজিস্ট্রারের DNS সেটিংসে হুবহু যোগ করুন। DNS সক্রিয় হতে কিছু সময় লাগতে পারে।
4. Render-এ domain verification সম্পন্ন হলে HTTPS/SSL সক্রিয় হয়েছে কি না পরীক্ষা করুন।

**গুরুত্বপূর্ণ:** ডোমেইন কেনা ও হোস্টিং অ্যাকাউন্ট তৈরি মালিককেই করতে হবে। কোনো API key, পাসওয়ার্ড বা পেমেন্ট তথ্য GitHub-এ দেবেন না।
