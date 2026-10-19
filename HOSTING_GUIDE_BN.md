# THE LAST SIGNAL v2.0.0 — বাংলায় চালানো ও হোস্টিং

## ১. ZIP extract করো
ZIP-এর ভেতরের সব ফাইল একই ফোল্ডারে রাখবে। `index.html` যেন `game.js`, `style.css`, `manifest.webmanifest`, `sw.js`, `scenes/` এবং `icons/`-এর পাশে থাকে। শুধু `index.html` আপলোড করলে গেম চলবে না।

## ২. GitHub Pages-এ ফ্রি হোস্টিং
1. GitHub-এ লগইন করে **New repository**-তে যাও। নাম দাও `the-last-signal`, Public নির্বাচন করো এবং repository তৈরি করো।
2. **Add file → Upload files**-এ গিয়ে ZIP extract করা ফোল্ডারের *ভেতরের সব ফাইল* আপলোড করো। repository-র root-এ `index.html` দেখা চাই।
3. repository-র **Settings → Pages** খুলো। **Deploy from a branch**, Branch `main`, Folder `/(root)` নির্বাচন করে Save করো।
4. deployment সম্পন্ন হলে GitHub যে URL দেবে, সেটি খুলো। সাধারণত URL-এর ফরম্যাট `https://তোমার-ইউজারনেম.github.io/the-last-signal/`। ইউজারনেম নিজেরটা দিয়ে বদলাবে।
5. ফোনে Chrome দিয়ে সাইট খোলো → ⋮ menu → **Add to Home screen**। একবার অনলাইনে লোড হলে গেমের ফাইল service worker cache করে রাখতে পারে।

## ৩. গেমে কীভাবে খেলবে
- Scene-এর hotspot বা নিচের **Available actions** কার্ডে tap করো। Desktop-এ `1–9` চাপলেও action নির্বাচন হবে।
- `J` = Journal, `M` = Map, `I` = Inventory, `Esc` = Pause। ফোনে নিচে Journal/Items/Map/Pause dock আছে।
- Cabin-এর desk note পড়ে safe-এ `742` দাও। Safe থেকে fuse ও cellar key নিয়ে generator চালু করো।
- Cellar-এ shadow figure-এর মুখোমুখি হলে flashlight দিয়ে তাড়াও অথবা লুকাও। Research annex-এ relay core আর report সংগ্রহ করো। Tower cipher `417`।
- Transmitter room-এ চূড়ান্ত সিদ্ধান্ত নিয়ে তিনটি ending-এর একটি দেখো।

## ৪. SQL লাগবে?
না—এই সংস্করণে user account বা server database নেই। Save browser-এর localStorage-এ থাকে। GitHub Pages static hosting, তাই PHP/MySQL চালায় না। Online accounts ও cross-device cloud saves যোগ করতে চাইলে আলাদা backend এবং নিরাপদ database architecture দরকার হবে।

## সতর্কতা
ফাইল আপলোডের সময় folder nesting যেন `the-last-signal/the-last-signal/index.html` না হয়ে যায়। `index.html` সরাসরি repository root-এ রাখতে হবে। প্রথম লোডে ইন্টারনেট লাগবে; offline cache সক্রিয় হতে HTTPS বা localhost দরকার।
