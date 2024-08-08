# Bangla Grammatical Error Detection

## CSE 472 Term Project

Models used - 
- BanglaBERT
- BanglaT5
- BanglaNLG

Generated predictions can be found in the `./data` folder
Results are available in the `./results` folder

### Description

We synthetically added grammatical error to a grammatically coherent dataset collected from newspapers. We find the part of speech of each word in a sentence and randomly add/edit/exchange relevant parts of speech to create our erroneous dataset. We then split the dataset into `train`, `validation`, `test` sets and train our models. After training our models, we evaluate the amount of detected errors.

### Dataset example

|Sentence                                                                                                       |Label|
|---------------------------------------------------------------------------------------------------------------|------|
|অক্টোবর ১৭ চলবে পর্যন্ত                                                                                             |neg|
|বিদ্যালয়ের ১১ শিক্ষকের মধ্যে আটজন অনুপস্থিত থাকায় কার্যত বন্ধ কার্যক্রম গেছে পাঠদান হয়ে।	                               |neg|
|পরে তাকে যশোর শহরের একটি হাসপাতালে নেওয়া হলে চিকিৎসক শিশুটিকে মৃত ঘোষণা করেন।	                                |pos|
|গোবিন্দগঞ্জ হাইওয়ে থানার ভারপ্রাপ্ত কর্মকর্তা ( ওসি ) ফুয়াদ রোহানী বলেন , নিহত ব্যক্তির পরনে লুঙ্গি ও পাঞ্জাবি সাদা ছিল।	          |neg|
|রাজনীতিক বাদ দিয়েও বিভিন্ন পেশার লোক সমন্বয়ে কমিশন চলে করা।	                                                    |neg|
|গুলশানের কূটনৈতিক এলাকায় আমরা বিভিন্ন সময়ে তাদের উপস্থিতি দেখতে পাচ্ছি।	                                            |pos|
|এ ছাড়া মাটি থেকে সাড়ে তিন ফুট গভীরে গ্যাসলাইন স্থাপনের নিয়ম থাকলেও অনেক স্থানে ছয় ইঞ্চি গভীর রেখে সংযোগ স্থাপন করা হয়। |pos|
