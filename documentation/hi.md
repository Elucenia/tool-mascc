<!-- ELUCENIA technical documentation · mascc · hi · no clinical/professional/rights approval -->

# MASCC सूचकांक

[शर्तें, स्रोत और अनुमतियाँ](https://elucenia.org/hi/tools/mascc)

## उपयोग कैसे करें

पोर्टल पर उपकरण का उपयोग करें या स्थानीय HTTP सर्वर के माध्यम से index.html खोलें। भाषा चुनें, फ़ील्ड भरें और गणना करें।

## इनपुट और इकाइयाँ

### रोग का भार (बुखार वाले प्रकरण के लक्षण)

`carga`

- `0` — गंभीर या मरणासन्न
- `3` — मध्यम
- `5` — नहीं या हल्के

### हाइपोटेंशन (सिस्टोलिक रक्तचाप \< 90 mmHg)

`hipotensao`

- `0` — हाँ
- `5` — नहीं

### सक्रिय क्रॉनिक ऑब्सट्रक्टिव पल्मोनरी डिज़ीज़

`dpoc`

- `0` — हाँ
- `4` — नहीं

### कैंसर का प्रकार

`tumor`

- `0` — पूर्व फंगल संक्रमण के साथ रक्त संबंधी कैंसर
- `4` — ठोस ट्यूमर, या पूर्व फंगल संक्रमण के बिना रक्त संबंधी कैंसर

### IV फ़्लूइड की आवश्यकता वाला निर्जलीकरण

`desidratacao`

- `0` — हाँ
- `3` — नहीं

### बुखार कहाँ शुरू हुआ

`local`

- `0` — अस्पताल में भर्ती के दौरान
- `3` — बाह्य रोगी

### आयु

`idade`

- `0` — ≥ 60 वर्ष
- `2` — \< 60 वर्ष

## विधि का संस्करण

MASCC/Klastersky 2000: 7 क्षेत्र, कुल 0–26, कटऑफ ≥21; ASCO/IDSA 2018 संदर्भ

## दस्तावेज़ित सूत्र

रोग भार: नहीं/हल्का 5, मध्यम 3, गंभीर 0 · हाइपोटेंशन नहीं 5 · COPD नहीं 4 · ठोस ट्यूमर 4, या पूर्व फंगल संक्रमण रहित रक्त कैंसर 4 · निर्जलीकरण नहीं 3 · बाह्यरोगी 3 · आयु \<60 वर्ष 2। अधिकतम 26।

## सीमाएँ और जनसमूह

MASCC ≥21 जटिलताओं के कम जोखिम को दर्शाता है, लेकिन अकेले छुट्टी, मौखिक एंटीबायोटिक या बाह्य रोगी प्रबंधन की अनुमति नहीं देता। ASCO/IDSA 2018 के संदर्भ में चयन नैदानिक आकलन, स्थिरता, सहवर्ती रोगों, तय समय पर वापस आने की क्षमता, घर में देखभालकर्ता तथा फोन और परिवहन की उपलब्धता पर निर्भर है। बाह्य रोगी प्रबंधन के उम्मीदवारों को छुट्टी से पहले कम से कम 4 घंटे निगरानी में रखना चाहिए और उनका अनुवर्ती आकलन आवश्यक है। इस कार्यान्वयन में निम्न रक्तचाप का मानदंड 2000 के मूल चर के अनुसार है: सिस्टोलिक रक्तचाप \<90 mmHg।

## संदर्भ

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## तकनीकी परीक्षण दोहराएँ

दर्ज कृत्रिम मामलों को दोहराने के लिए इस रिपॉज़िटरी की मूल निर्देशिका में node test.cjs चलाएँ। मूल इनपुट, अपेक्षित परिणाम और सहनशीलता सीमाएँ सुरक्षित रखी गई हैं। तकनीकी परीक्षण नैदानिक सत्यापन नहीं हैं।

```sh
node test.cjs
```

tool.json में स्रोत, संस्करण और समीक्षा का दायरा दिया गया है। examples.json में कृत्रिम इनपुट और अपेक्षित परिणाम सुरक्षित हैं; results.json में प्राप्त परिणाम दर्ज हैं।

[रिकॉर्ड और संदर्भ](../tool.json) · [JavaScript कोड](../calculator.js) · [संदर्भ मामले](../examples.json) · [results.json](../results.json)

## समीक्षा और उपयोग की शर्तें

स्वतंत्र नैदानिक समीक्षा नहीं की गई है।

यह इंटरफ़ेस लेखकों द्वारा किया गया अनुवाद है, कोई आधिकारिक या प्रमाणित संस्करण नहीं। स्वतंत्र नैदानिक समीक्षा, पेशेवर भाषाई समीक्षा और उपकरणों के अधिकारों की अनुमति की प्रक्रिया पूरी नहीं हुई है।

सूत्र या वर्गीकरण का परिणाम। व्याख्या, कार्यवाही और उपयुक्तता पेशेवर मूल्यांकन और चुने गए स्रोत पर निर्भर है।

## लाइसेंस और श्रेय

Apache-2.0 केवल ELUCENIA के कोड पर लागू होता है। उपकरणों, प्रकाशनों, अनुवादों और डेटा के अधिकार उनके संबंधित अधिकारधारकों के पास रहते हैं। LICENSE और NOTICE सुरक्षित रखें।

ELUCENIA · Felipe Guedes · Copyright © 2026
