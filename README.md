# रसोई साथी - बुंदेलखंडी रसोई (Rasoi Saathi)
**Hindi-First, Mobile-First Installable PWA for Indian Home Cooks**

"घर में क्या है? आज क्या बनाएं?" — भारतीय परिवारों और गृहणियों के लिए घर में रखी उपलब्ध सामग्री से तुरंत बनने वाले पारंपरिक बुंदेलखंडी और उत्तर भारतीय व्यंजन सुझाने वाला वेब ऐप।

---

## 📖 विषय सूची / Table of Contents
1. [मुख्य विशेषताएं (Key Features)](#-मुख्य-विशेषताएं-key-features)
2. [शुरू कैसे करें (How to Run Locally)](#-शुरू-कैसे-करें-how-to-run-locally)
3. [नए व्यंजन कैसे जोड़ें (How to Add Recipes to JSON)](#-नए-व्यंजन-कैसे-जोड़ें-how-to-add-recipes-to-json)
4. [मुफ़्त में डिप्लॉय कैसे करें (Free Deployment Guide - Vercel / Netlify)](#-मुफ़्त-में-डिप्लॉय-कैसे-करें-free-deployment-guide)
5. [फोन में ऐप कैसे जोड़ें (Add to Home Screen - PWA)](#-फोन-में-ऐप-कैसे-जोड़ें-add-to-home-screen)
6. [English Documentation](#-english-documentation)

---

## 🌟 मुख्य विशेषताएं (Key Features)

- **सामग्री मिलान इंजन (Ingredient Matching Engine)**: घर में रखी सामग्री (आलू, टमाटर, बेसन आदि) चुनते ही ऐप व्यंजनों को ३ श्रेणियों में दिखाता है:
  - 🟢 **अभी बना सकते हैं** (१००% सामग्री मौजूद)
  - 🟡 **सिर्फ़ १-२ चीज़ें कम हैं** (कम सामग्री लाल रंग में स्पष्ट दिखेगी)
  - ⚪ **और विकल्प**
- **बुंदेलखंडी पारंपरिक व्यंजन**: बफौरी, मंगौड़ी की सब्ज़ी, कढ़ी-फरा, दाल-बफला, महुआ के गुलगुले/खीर, बरा, बेसन के गट्टे, सत्तू पराठा व शरबत, ज्वार/बाजरा/मक्के की रोटी, बेर की चटनी आदि (६०+ प्रामाणिक व्यंजन)।
- **देसी घरेलू माप एवं ऑटो-स्केलिंग**: कटोरी, चम्मच, मुट्ठी, चुटकी + ग्राम/मिली। २, ४, ६, ८ लोगों के लिए १-टैप में मात्रा का पुनः हिसाब।
- **हैंड्स-फ्री कुकिंग**:
  - 🔊 **"पढ़कर सुनाओ"**: खाना बनाते समय हिंदी आवाज़ (Web Speech API) में चरण दर चरण सुनना।
  - ⏱️ **स्मार्ट इन-स्टेप टाइमर**: समय वाले चरणों के लिए स्वचालित टाइमर व अलार्म।
  - 🔥 **स्क्रीन वेक लॉक**: कुकिंग के दौरान फोन की स्क्रीन बंद नहीं होगी।
- **मेरी रेसिपी जोड़ें (Mom's Recipes)**: बोलकर (वॉइस टाइपिंग) या लिखकर मां और नानी-दादी के पारंपरिक नुस्खों को हमेशा के लिए सुरक्षित सहेजें।
- **त्योहार / व्रत मोड**: १-क्लिक में एकादशी, नवरात्रि व सावन व्रत के अनुकूल व्यंजन (साबूदाना, कुट्टू, मखाना आदि)।
- **साप्ताहिक भोजन योजना एवं खरीदारी सूची**: ७ दिन का मील प्लानर + व्हाट्सएप पर १-क्लिक में लिस्ट शेयर करने की सुविधा।
- **१००% ऑफ़लाइन PWA**: एक बार लोड होने के बाद बिना इंटरनेट भी पूरा ऐप सुचारू रूप से चलता है।
- **वरिष्ठ नागरिकों हेतु सुलभता**: न्यूनतम १८px बॉडी टेक्स्ट, A- / A / A+ फॉन्ट स्केलर, न्यूनतम ४८px बड़े स्पर्श बिंदु, वार्म अर्थी पैलेट (हल्दी पीला, टेराकोटा, पत्ती हरा)।

---

## 🚀 शुरू कैसे करें (How to Run Locally)

### पूर्वापेक्षाएं (Prerequisites):
- Node.js (v18+)
- npm या pnpm

### चलाने के चरण:
```bash
# 1. प्रोजेक्ट फ़ोल्डर में जाएं
cd rasoi-saathi

# 2. आवश्यक पैकेज इंस्टॉल करें
npm install

# 3. डेवलपमेंट सर्वर शुरू करें
npm run dev

# 4. ब्राउज़र में खोलें
# http://localhost:5173/
```

### प्रोडक्शन बिल्ड बनाने हेतु:
```bash
npm run build
npm run preview
```

---

## 🍲 नए व्यंजन कैसे जोड़ें (How to Add Recipes to JSON)

ऐप का संपूर्ण डेटा `src/data/recipes.json` में संग्रहीत है। आप सीधे इस फ़ाइल में नया व्यंजन जोड़ सकते हैं:

```json
{
  "id": "meri_anokhi_sabzi",
  "hindi_name": "मेरी खास सब्ज़ी",
  "english_name": "My Special Sabzi",
  "bundelkhandi_name": "देसी खास सब्ज़ी",
  "region": "बुंदेलखंड / मध्य प्रदेश",
  "is_traditional": true,
  "diet_tags": ["शाकाहारी"],
  "meal_type": ["दोपहर का खाना", "रात का खाना"],
  "season": ["सभी मौसम"],
  "occasion": ["रोज़ का खाना"],
  "cook_time_min": 25,
  "prep_time_min": 10,
  "difficulty": "सरल",
  "serves": 4,
  "cooking_method": ["कढ़ाई"],
  "image": "🍲",
  "ingredients": [
    {
      "ingredient_id": "aloo",
      "quantity": 2,
      "unit": "नग (पीस)",
      "metric_equivalent": "लगभग २०० ग्राम",
      "optional": false
    },
    {
      "ingredient_id": "tamatar",
      "quantity": 2,
      "unit": "नग (पीस)",
      "metric_equivalent": "कटे हुए",
      "optional": false
    }
  ],
  "steps_hindi": [
    "कढ़ाई में तेल गरम करके जीरा-हींग तड़काएं।",
    "आलू और टमाटर डालकर धीमी आंच पर १० मिनट पकाएं।"
  ],
  "steps_english": [
    "Heat oil in a pan, add cumin and hing.",
    "Add potatoes and tomatoes, cook on low heat for 10 minutes."
  ],
  "tips_hindi": "मसाला भूनते समय १ चम्मच देसी घी अवश्य डालें।",
  "substitutions": [
    {
      "ingredient_id": "tamatar",
      "substitute_hindi": "आधा कटोरी दही या अमचूर",
      "substitute_english": "Curd or dry mango powder"
    }
  ]
}
```
> **टिप**: नई सामग्री का `ingredient_id` हमेशा `src/data/ingredients.json` में मौजूद आईडी से मेल खाना चाहिए।

---

## 🌐 मुफ़्त में डिप्लॉय कैसे करें (Free Deployment Guide)

आप अपनी माताजी या परिवार के साथ इस ऐप को साझा करने के लिए Vercel या Netlify पर बिल्कुल मुफ़्त में डिप्लॉय कर सकते हैं:

### विकल्प १: Vercel पर डिप्लॉय (सुझावित)
1. अपने कोड को GitHub पर पुश करें।
2. [vercel.com](https://vercel.com) पर जाएं और अपने GitHub खाते से साइन इन करें।
3. **"Add New..."** ➜ **"Project"** चुनें और अपने `rasoi-saathi` रिपॉजिटरी को आयात (Import) करें।
4. Framework Preset में **"Vite"** अपने आप चुन लिया जाएगा।
5. **"Deploy"** पर क्लिक करें। २ मिनट में आपको एक लाइव लिंक मिल जाएगा (उदा: `https://rasoi-saathi.vercel.app`) जिसे आप किसी को भी व्हाट्सएप पर भेज सकते हैं!

### विकल्प २: Netlify पर डिप्लॉय
1. [netlify.com](https://netlify.com) पर जाएं और लॉगिन करें।
2. **"Add new site"** ➜ **"Import an existing project"** ➜ GitHub चुनें।
3. बिल्ड सेटिंग्स:
   - Build Command: `npm run build`
   - Publish directory: `dist`
4. **"Deploy site"** पर क्लिक करें।

---

## 📱 फोन में ऐप कैसे जोड़ें (Add to Home Screen)

लाइव लिंक मिलने के बाद अपनी माताजी या फोन उपयोगकर्ता से कहें:
1. फोन के Chrome या Safari ब्राउज़र में लिंक खोलें।
2. ऊपर दाईं ओर तीन बिंदुओं **(⋮)** या Safari में नीचे शेयर बटन **(Share)** पर टैप करें।
3. **"Add to Home Screen"** (होम स्क्रीन पर जोड़ें) या **"Install App"** चुनें।
4. अब फोन की होम स्क्रीन पर "रसोई साथी" का खूबसूरत मिट्टी के बर्तन वाला आइकॉन बन जाएगा। यह बिना इंटरनेट के भी सुपरफ़ास्ट खुलेगा!

---

## 🌐 English Documentation

### Overview
**Rasoi Saathi (Kitchen Companion)** is a Hindi-first, mobile-first Progressive Web App (PWA) created for Indian households with a spotlight on authentic Bundelkhandi (Madhya Pradesh & Uttar Pradesh) regional recipes and everyday North Indian food.

### Features
1. **Pantry-Matching Algorithm**: Select available ingredients at home and see matching recipes partitioned into "Ready to Cook", "Missing 1-2 Items", and "More Alternatives".
2. **Substitutions**: Automatic non-intrusive culinary substitutes (e.g. curd -> lemon + milk or amchur).
3. **Household Measurement Scaling**: Uses traditional units (katori, spoon, fistful, pinch) scalable dynamically for 2, 4, 6, or 8 people.
4. **Hands-free Cooking**: Hindi voice read-aloud via Web Speech API, step timers, and screen wake lock to keep screen illuminated while hands are messy.
5. **Save Family Recipes**: Built-in voice dictation for home cooks to save personal recipes locally.
6. **Vrat / Fasting Mode**: 1-tap filter for onion-free, garlic-free, fasting-friendly dishes.
7. **Weekly Meal Planner & WhatsApp Sharing**: 7-day breakfast/lunch/dinner grid with 1-click consolidated grocery list shareable directly via WhatsApp.
8. **100% Offline PWA**: Powered by Workbox service worker caching all assets and recipe JSON for instant offline loading.

### Technical Stack
- React 18
- Vite 5
- Tailwind CSS
- Lucide React
- Vite Plugin PWA (Workbox precache)
- Web Speech API (TTS & STT)
- Screen Wake Lock API
- Web Share API
