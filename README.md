# AI Prompting in 2026 — Ek Connected Flow mein (13 Concepts)

> **Source page:** [AI Prompting in 2026: A Crash Course](https://agentfactory.panaversity.org/docs/ai-prompting-2026) — The AI Agent Factory (Panaversity)



## Table of Contents

0. [Poora flow: 1 fact, 2 moves, 13 concepts](#0-poora-flow-ek-fact-do-moves-13-concepts)
1. [Running example: Nida ka skincare brand](#running-example-nida-ka-skincare-brand)
2. [2023 se ab tak kya badla](#2023-se-ab-tak-kya-badla)
3. [PART 1: AI ko cheezein kaise pata hoti hain](#part-1-ai-ko-cheezein-kaise-pata-hoti-hain)
   - [Concept 1: Novice vs Power user](#concept-1-novice-vs-power-user)
   - [Concept 2: Pretrained knowledge](#concept-2-pretrained-knowledge)
   - [Concept 3: Teen retrieval modes](#concept-3-teen-retrieval-modes)
4. [PART 2: AI se achhe se baat karna](#part-2-ai-se-achhe-se-baat-karna)
   - [Concept 4: Context is the whole game](#concept-4-context-is-the-whole-game)
   - [Concept 5: Reasoning ("think hard")](#concept-5-reasoning-think-hard)
   - [Concept 6: Sycophancy aur uska ilaaj](#concept-6-sycophancy-aur-uska-ilaaj)
   - [Concept 7: Brainstorm-iterate loop](#concept-7-brainstorm-iterate-loop)
5. [PART 3: Text se aagay](#part-3-text-se-aagay)
   - [Concept 8: Multimodal](#concept-8-multimodal-images-aur-audio)
   - [Concept 9: Ek prompt mein chhoti app](#concept-9-ek-prompt-mein-chhoti-app)
   - [Concept 10: Data analysis](#concept-10-data-analysis-model-code-likh-kar-chalata-hai)
6. [PART 4: Safe aur smart istemal](#part-4-safe-aur-smart-istemal)
   - [Concept 11: Desktop apps aur permissions](#concept-11-ai-desktop-apps-aur-permissions)
   - [Concept 12: Cost, speed aur model ka intikhab](#concept-12-cost-speed-aur-model-ka-intikhab)
   - [Concept 13: Models checking models](#concept-13-models-checking-models)
7. [Concepts ka connection map](#concepts-ka-connection-map)
8. [MASTER DIAGRAM](#master-diagram)
9. [Quick Recall Cheat Sheet](#quick-recall-cheat-sheet)
10. [Practice: 12 prompts](#practice-12-prompts)

---

## 0. Poora flow: 1 fact, 2 moves, 13 concepts

Is poore page ki buniyad **ek fact** hai:

> **Model stateless hai.** Us ke andar apni koi yaadasht nahi. Wo har jawab sirf us text se deta hai jo **abhi, is lamhe** us ke saamne rakha hai.

Is fact se automatically **do moves** nikalti hain, aur page ki har "advanced technique" inhi mein se ek hai:

```
                 MODEL STATELESS HAI
                         |
        +----------------+-----------------+
        |                                  |
  MOVE 1: Sahi context                MOVE 2: Ghalat context
          ANDAR daalo                         BAHAR rakho
  (files, limits, audience,           (unrelated topics, duplicate
   sources, examples)                  files, purani baaton ka shor)
```



### 13 concepts ka map (4 parts)

```
PART 1: JAWAB KAHAN SE AATA HAI?
   1 Briefing hi prompt hai
   2 Training text (kya strong, kya weak)
   3 Teen raaste: pretrained / web search / deep research

PART 2: CONTEXT KO SANWAARNA
   4 Context stack (6 layers) + memory + projects + context rot
   5 Think hard (reasoning)
   6 Sycophancy: neutral wording + rubric score
   7 Loop: options -> feedback -> options + "grip dial"

PART 3: TEXT SE AAGAY
   8 Images/audio  (in aur out)
   9 Ek prompt = chhoti working app (artifact)
  10 Code run karwa kar data analysis

PART 4: SAFE + SMART
  11 Desktop apps: plan pehle, permission chhoti
  12 Cost/speed/model ladder, leader badalta rehta hai
  13 Different families ek doosre ko check karein
```

### 60 second ki kahani

Aap ek smart naye colleague ko brief karte hain (1). Wo internet parh kar seekha hai, isliye common cheezon mein strong aur thin cheezon mein kamzor hai (2). Jawab training se aayega, web search se, ya deep research se, aur aap ke alfaaz tay karte hain kaunsa (3). Jo kuch bhi aap ne saamne rakha wahi uski poori duniya hai, isliye context stack ko design karo (4). Mushkil sawal par usay sochne do (5). Wo aap se agree karna pasand karta hai, isliye neutral poochho aur number se score karwao (6). Pehla jawab kabhi final nahi, loop chalao (7). Phir images/audio (8), chhoti apps (9), aur data par code run karwana (10) seekho. Jab AI aap ki files chhoo, tab permissions tang rakho (11). Tool badalte rehte hain, do-teen try karo (12). Aur jab koi expert nahi, to alag companies ke models se cross-check karo (13).

---

## Running example: 



> **Nida** ek chhota skincare brand launch kar rahi hai (ek moisturizer aur ek sunscreen). Uske paas suppliers ke quotes hain, purani sales ka data hai, aur wo AI se madad lena chahti hai: product ka naam, pricing, market research, packaging, launch memo, sab kuch.

Har concept mein dekhna: Nida ka *wahi project* ek naye angle se kaise kaam karta hai.

---

## 2023 se ab tak kya badla

Agar aap ne 2022-23 mein ChatGPT ko "clever toy" samjha tha, to aaj ka tool wo nahi:

| Pehle | Ab | Kis concept mein detail |
|---|---|---|
| Chhoti context window (kuch hazaar words) | Hazaron se lekar ~10 lakh words tak, yaani poori kitaab ya contracts ka folder | 4 |
| "Think step by step" ek jaadui jumla | Built-in thinking mode jo seconds se minutes tak sochta hai | 5 |
| Sirf training ka yaad kiya hua | Built-in web search | 3 |
| Andaaze se arithmetic | Built-in code execution | 10 |
| Sirf text | Images, PDFs, spreadsheets, audio | 8 |
| Har chat blank | Tool aap ke baare mein notes likh kar rakhta hai (memory) | 4 |
| Sirf chat | Desktop apps aur command-line agents jo files par kaam karte hain | 11 |

> **Note:** Web search aur code execution aksar *invisible* hote hain, is liye pata hi nahi chalta ke jawab yaad se aaya, web page se, ya calculation se. Poochna seekho: *"Kya tum ne sach mein search kiya?"* ya *"Andaaza nahi, run karke batao."*

---

# PART 1: AI ko cheezein kaise pata hoti hain

## Concept 1: Novice vs Power user

### Easy samajh

Novice AI ko Google ki tarah use karta hai: chhota sa sawal, jawab skim, aagay. Power user AI ko **briefing** deta hai, bilkul jaise ek naye smart colleague ko pehle din brief karte hain. Farq "clever question" ka nahi, chand aadaton ka hai.

Ek achhi briefing ke **4 hisse**:

```
BRIEFING = FILES (kya parhna hai)
         + GOAL  (kis maqsad ke liye)
         + LIMITS (budget, time, kya nahi karna)
         + EXACT ASK (bilkul kya chahiye)

Novice sirf aakhri hissa likhta hai.
```

### Nida ka example

| | Novice Nida | Power-user Nida |
|---|---|---|
| Prompt | "Moisturizer ka launch plan banao" | Supplier quotes + budget + audience (oily skin, garam mausam) + sales-channel ki limit attach karti hai, phir kehti hai "trade-offs batao, sab parh kar sochna" |
| Jawab | Generic, kisi bhi brand par lagne wala | Uske apne numbers aur limits par bana plan |

**Slop:** AI ka wo text jo upar se fluent hai aur andar se khaali. Jab aap context aur constraints nahi dete, to AI default mein yehi likhta hai ("in today's fast-paced world..."). Isi liye power user pehle outline, phir critique, phir bullets, phir hi prose maangta hai (Concept 7).

### Technical depth: "Smart naya colleague" analogy kahan tootti hai

Analogy do jagah kamzor hai, aur wahi jagah asal sabaq hain:

```
Asli colleague                     AI
----------------------------       ------------------------------------
Aap ko mahino mein seekh leta      Har nayi chat mein zero se shuru
                                   -> briefing HAR BAAR dena parti hai

Brief clear na ho to poochta hai   Gap ko GUESS se bharta hai, aur
                                   utna hi confident lagta hai
```

**Sending se pehle ka test:** *"Kya ek naya colleague sirf itna dekh kar ye kaam achhe se kar sakta hai?"*

### Yaad rakho
Briefing = files + goal + limits + exact ask. Novice sirf ask likhta hai.

---

## Concept 2: Pretrained knowledge

#

**Pretrained knowledge** = jo model ne training text se seekha, bagair kisi lookup ke. AI ne duniya mein reh kar nahi seekha, us ne duniya ke baare mein **parh kar** seekha: Reddit, Wikipedia, kitabein, news, papers, blogs, forums. Isliye:

> **Jis topic par internet par jitna zyada likha gaya, AI wahan utna hi reliable.**

### Diagram: Loud / Quiet / Secret

```
LOUD (sab likhte hain)      QUIET (kam likhte hain)        SECRET (kisi ne likha hi nahi)
-------------------------   ----------------------------   -------------------------------
cooking, mashhoor movies,   chhote gaon ki history,        aap ki company ka private data,
common health advice,       niche professional knowledge,  aap ka calendar, cutoff ke
popular programming langs   kam-zubaan (jaise Cantonese)   BAAD ki cheezein
       |                            |                              |
   TRUST: high                 TRUST: verify karo             TRUST: zero, model guess kar raha hai
```

### Nida ka example

| Sawal | Zone | Trust |
|---|---|---|
| "Niacinamide skin ke liye kya karta hai?" | Loud (bohat likha gaya) | High |
| "Meri city ke chhote pharmacy chains ka margin kya hota hai?" | Quiet | Verify karo |
| "Mere supplier ne pichli baar kya rate diya tha?" | Secret | Model ko pata hi nahi |
| "Is saal cosmetics labeling ke naye rules kya hain?" | Cutoff ke baad ho sakta hai | Jab tak search na kare, trust mat karo |

### Technical depth

1. **Typos ki fikr mat karo.** Training text mein typos bharay hain, model misspelling handle kar leta hai.
2. **Absorbed errors:** model ne galat forum posts aur purani info bhi seekh li. Ek confidently-galat post ek confidently-galat model ban sakti hai.
3. **Knowledge cutoff:** wo tareekh jahan training text khatam hota hai. Us ke baad ki har cheez model ke andar hai hi nahi.
4. **Galat jawab kyun confident lagta hai?** Model thin data se *generalize* karta hai. Page ka misaal: ek gaon ke lok-khel ke rules poochay to AI ne milte-julte khelon ko mila kar tin confident paragraph likh diye, jabke dadi ne kaha lagbhag sab galat. AI ne "jhoot" nahi bola, thin data se andaza lagaya. Ghalti ye thi ke confidence ko accuracy samjha gaya.

**Har source par wahi sawal:** *"Is ko ye kaise pata hoga?"* AI par bhi lagao.

### Pichle concept se link
Concept 1 ne kaha briefing do. Concept 2 batata hai ke AI ka apna knowledge kahan kamzor hai, yaani briefing mein *kya* zaroor dena hai (Secret aur Quiet zone ki cheezein).

### Yaad rakho
Reliability training text ke hisaab se chalti hai. Common topics strong, thin topics weak, private/recent facts missing.

---

## Concept 3: Teen retrieval modes

### Easy samajh

Sawal poochne par AI tool (aksar bina bataye) teen tareeqon mein se ek chunta hai:

```
MODE 1: PRETRAINED     MODE 2: WEB SEARCH        MODE 3: DEEP RESEARCH
seconds                 tens of seconds           minutes
sirf training           kuch live pages           dozens of sources, plan
definitions,            current events,           structured report
common facts            quick research            (junior researcher ka ek ghanta)
weak: purani/local info weak: popular sources     weak: slow, chhote sawal ke liye
                        pehle cite karta hai      zaroorat se zyada

<------------- sasta, tez ---------------------- mehnga, gehra ------------->
```

### Nida ka example

- "Cats wall ko kyun ghoorti hain?" -> Mode 1 kaafi.
- "Is hafte cosmetics import par kya naya aya?" -> Mode 2 (cutoff ke baad ki cheez).
- "Launch ke liye permits, labeling aur packaging rules ki poori report banao, official sources se" -> Mode 3.

### Technical depth: Web search kaise kaam karta hai, aur galat kyun parh leta hai

```
Aap ka sawal
   |
   v
[Search + retrieval layer]  (aksar ek alag, chhota model)
   |  searches chalata hai, pages chunta hai,
   |  har page ko chhote passage mein katata hai
   v
Sirf SHORT VERSION --> asli jawab dene wale model tak
```

Yaani jo model aap se baat kar raha hai wo aksar **page ki summary** parhta hai, page nahi. Summary mein detail kho jati hai, isi liye kabhi page ko galat report kar deta hai. Aur search ye check nahi karti ke source *current* hai (page ka misaal: 20 saal purane page se ek aisa school recommend ho gaya jo ab public ke liye khula hi nahi).

**Reliability ke 3 fixes (kisi bhi web-search prompt mein paste kar sakte ho):**

1. Source types naam lo: "official regulator, industry reports, peer-reviewed. Forums nahi."
2. Har claim ke baad source maango, ya exact sentence quote karwao.
3. Jo claim support na ho use `unverified` mark karwao.

Ye teeno us failure ko kam karte hain jahan AI kai sources ko mila kar ek confident jumla bana deta hai jo kisi ek source mein bhi nahi likha.

### Phrasing kya trigger karti hai

| Aap ka andaaz | Aksar kya chalta hai |
|---|---|
| "X kya hai", "Y ki summary" | Pretrained |
| "latest", "aaj", "is hafte", koi khaas city | Web search |
| "thoroughly research karo", "citations ke saath report", "ye source types" | Deep research |
| Files attach karna | Files par pretrained; agar current info maango to web bhi |

### AI vs Google
Link chahiye ("official IRS page", "charger khareedna") to Google. Jawab chahiye ("in sab ko jodo, mujhe kya sochna chahiye") to AI. Sawal ye hai ke aap ko **link** chahiye ya **jawab**.

### Yaad rakho
Teen mode hain, aap ke alfaaz tay karte hain kaunsa chale. Jahan jawab current hona chahiye wahan sources naam lo.

---

# PART 2: AI se achhe se baat karna

## Concept 4: Context is the whole game

Ye page ka sab se bara concept hai, is liye isay tukron mein samajhte hain.

### 4.1 Easy samajh: Context window = padhne ki mez

**Context window** = wo saara text jo model **ek jawab likhte waqt** dekh sakta hai. Ise ek **reading desk** samjho: jo cheez desk par hai wo model ke liye hai, jo desk par nahi wo is jawab ke liye *exist hi nahi karti*.

Desk ki analogy do jagah tootti hai:

```
Asli desk                              Model ki desk
-----------------------------          ------------------------------------------
Rakhi cheez wahin rehti hai            Har reply se pehle SAAF hoti hai aur
                                       stored text se dobara BANAI jati hai

Har page barabar saaf dikhta hai       Desk jitni bharti hai, recall utna kamzor
                                       (isi ka naam context rot ki wajah hai)
```

Capacity itni bari ke ~7.5 lakh words (Harry Potter ki pehli 4-5 kitabein) aa jayein, magar bhari window ko model utni tawajjo se nahi parhta jitni chhoti window ko.

### 4.2 Technical depth: Context ke 6 layers

```
 L6  Uploaded files       PDF, sheet, image, voice memo     <- aap dete hain
 L5  Chat history         pichle saare turns                <- conversation
 L4  Aap ka prompt        abhi ka message                   <- aap likhte hain
 L3  Tool descriptions    web search, code run, file access <- product
 L2  Memory               aap ke baare mein tool ke notes   <- tool khud likhta hai
 L1  System prompt        company ke rules (aap ko nahi     <- company likhti hai
                          dikhte)
 ---------------------------------------------------------------
 In 6 ke ilawa kuch nahi: yahi model ki poori "duniya" hai is jawab ke liye.
 L1 aur L2 aap ke type karne se PEHLE se desk par maujood hain.
```

**Stateless ka matlab practically:**

```
Turn 1:  [L1 + L2 + L3 + prompt1]                       --> Model --> jawab1
Turn 2:  [L1 + L2 + L3 + prompt1 + jawab1 + prompt2]    --> Model --> jawab2
                       ^
        tool har baar poori purani baat wapas bhejta hai
        (model ke andar kuch "bacha" nahi hota)
```

### 4.3 System prompt: teen tools alag kyun lagte hain?

Ek naye waiter ko owner pehle briefing deta hai: "friendly raho, daily special batao, allergen ka pooche to kitchen se confirm karo, andaza mat lagao." Customer ye briefing kabhi nahi sunta, magar waiter har table par wahi follow karta hai. **System prompt** bilkul yehi hai.

Us mein aam taur par: behavior, kya refuse karna hai, tone, kab disclaimer dena hai, kaunse tools available hain.

**Isi liye Claude, ChatGPT aur Gemini ka mizaj alag lagta hai.** Ye model ki "personality" nahi, company ke likhe instructions ka farq hai (page ke mutabiq: Claude ke instructions careful thinking aur honesty par, ChatGPT ke warmth aur broad helpfulness par, Gemini ke short, sourced answers par). Rude hone par bhi AI ka polite rehna, kuch requests refuse karna, unasked safety warnings, ye sab isi layer ka asar hai.

### 4.4 Apni layer add karo (custom instructions), aur usay prune karo

Har tool mein aap likh sakte ho ke aap kaun ho aur jawab kaisa chahiye; ye system prompt ke saath **har chat mein pehle se load** hota hai.

| Tool | Setting ka naam |
|---|---|
| Claude | Settings > General > "Instructions for Claude" (personal preferences) |
| ChatGPT | Settings > Personalization > Custom instructions |
| Gemini | Personalization settings (switch on karke Add) |

Misal: ek teacher likhti hai "Main Grade 5 science parhati hoon, 10 saal ke bacche ki parhne ki level par samjhao, jargon pehle define karo." Ab wo har chat mein ye dobara nahi kehti.

**Prune karo!** Har baar AI kuch ghalat kare to ek line aur jodne ka dil karta hai. Saal baad 20 lines, kuch ek doosri se takrati hui. Page ke mutabiq Anthropic ne khud July 2026 mein apne products ke jama-shuda standing instructions ka bara hissa delete kiya aur quality mein koi kami nahi aayi. Do aadatein:

1. Wo likho jo AI khud andaza nahi laga sakta (aap ka kaam, audience, hard limits).
2. Kuch mahine baad har line par poochho: *agar ye hata doon to AI kuch ghalat karega?* Nahi, to delete.

### 4.5 Nida ka example: bare prompt vs context-rich prompt

- Bare: "Moisturizer ke liye packaging ideas do."
- Context-rich: brand voice ke 3 samples + target audience + supplier ki packaging limits + budget attach karo. Ab jawab Nida ki asli situation par hai.

**Attach karne se pehle checklist:**

| Sawal | Haan to |
|---|---|
| Koi document hai jis se jawab consistent ho? | Attach karo |
| Koi constraint jo AI andaza nahi laga sakta (budget, time, team)? | Likho |
| Koi pichla faisla ya process? | Ek paragraph mein summary |
| Koi khaas output format? | Naam lo (table, email, bullets) |
| Koi audience? | Naam lo |

**Curation dono taraf chalti hai:** "aur de do" aksar ghalat fix hai. Jo file sawal ke liye zaroori nahi wo hatao, near-duplicate files hatao, jo bachein un ka label likho ke kis kaam ki hain. Har extra file ek aur cheez hai jise model galat parh sakta hai.

### 4.6 Memory: model ko yaadasht nahi milti, tool ke paas notes hote hain

Aaj teeno tools aap ke baare mein ek chhota profile likh kar har nayi chat ke shuru mein load karte hain. Ye sunne mein "stateless" ke khilaf lagta hai, magar nahi:

> **Memory model ko memory nahi deti.** Ye tool ka rakha hua ek note hai jo wo *aap ke type karne se pehle* L2 ke tor par desk par rakh deta hai.

| Tool | Naam | Clean-slate mode |
|---|---|---|
| Claude | Memory | Incognito chat |
| ChatGPT | Memory (saved memories + past chats) | Temporary Chat |
| Gemini | Personal context | Temporary Chat |

*(Menu ke naam badalte rehte hain, apni settings dekho.)*

**Teen aadatein aur ek warning:**

1. **Ek dafa parho** ke tool ne kya store kiya hai; koi line delete ho sakti hai.
2. **Chat mein zubaani sahi karo:** "tum farz kar rahe ho main abhi bhi retail mein hoon, aisa nahi hai." Note update ho jata hai.
3. **Clean-slate mode** wahan use karo jahan purana context gumrah karega.
4. **Warning (confidentiality wale peshay):** doctor, lawyer, accountant, teacher ke clients/students ki tafseelat memory note mein jama ho kar mahino baad kisi aur chat mein wapas aa sakti hain. Pehchan wali details memory se bahar rakho, ya alag clean chat / scoped project mein kaam karo.

Agar AI har nayi chat mein wahi ghalat farz karta hai, to prompt dobara likhna chhoro aur **memory theek karo**.

### 4.7 Context rot aur compaction

**Context rot** = ek hi lambi chat mein bahut se unrelated topics chalne se jawabon ki quality girna. Pehle workout plan, phir spreadsheet debug, phir khala ko thank-you note, workout ab bhi desk par para hai aur model ko kheench raha hai.

**Stale chat ki nishaniyan:**

```
[ ] AI aisi purani baatein le aata hai jinka abhi ke sawal se taalluq nahi
[ ] Jawab lambe aur dhundle, zyada hedging
[ ] 5 turn pehle di hui limit bhool gaya
[ ] Baar baar maafi, magar progress nahi
```

**Compaction (asal mechanism):** chat bahut lambi ho jaye to tool purane turns ki jagah unki ek chhoti *summary* rakh deta hai. Kahani bach jati hai, tafseelat chali jati hain: jis library ka naam 3 ghante pehle liya, jo naming rule tay hua, turn 4 mein di hui limit, koi bhi summary mein ghayab ho sakti hai. Claude "compacting" ka chhota sa message dikhata hai; ChatGPT aur Gemini bina bataye karte hain.

```
Chat window  =  WORKING MEMORY   (mutabdil, kat-chhant hoti hai)
Project/file/note  =  STORAGE    (jo zinda rehna chahiye wahan rakho)
```

**Ilaaj:** naya chat shuru karo, sirf 1-2 zaroori facts paste karo, aagay barho. Reset aksar rescue se tez hai. Agar purani chat mein koi plan/draft/faisla banaya hai, pehle file mein save karo.

### 4.8 Projects: context ek dafa, har baar nahi

**Project** = ek workspace jismein files, instructions aur audience ek dafa set hote hain, aur us ke andar ki har chat unhein inherit karti hai.

**Kab banao:** jab aap ne ek hi topic ki 2 chats mein wahi files/audience/limits paste ki hon. Teen sawal: kaam dobara aata hai? Background har baar wahi? Output ki shakal har baar wahi? Do haan = project.

Misalein: tax filing (pichla return, W-2s, "hamesha math dikhao"); school (syllabus + calendar, "hamesha tareekh calendar se check karo"); writing voice (3 samples, "inki lay aur alfaaz match karo, wo hedging mat daalo jo maine nahi ki").

Project mein naya chat sirf **purani chat ka shor** girata hai, standing files aur instructions bache rehte hain: aap *chat reset* karte ho, *context nahi*.

| Tool | Naam | Zor kis par |
|---|---|---|
| Claude | Projects | Instructions aur behavior (voice, role, rules) |
| ChatGPT | Projects | Instructions aur behavior |
| Google | Notebooks (Gemini) + NotebookLM | Sources (PDF, Docs, links, YouTube, audio) aur clickable citations; workspace time ke saath barhta hai |

Chhota rule: workspace waqt ke saath barhega (study notes, research) to Gemini/NotebookLM; agar instructions ka ek mustaqil "character" chahiye to Claude/ChatGPT Projects. Free tier ke caps ki shakal alag hai (Claude: projects ki tadaad, ChatGPT: har project ki files), jo cap pehle lage us ke hisaab se plan karo.

### Nida ka poora Concept 4

Nida ne "Nida Skincare" project banaya: brand voice samples + supplier quotes + audience notes + instruction "har number ke saath calculation dikhao". Ab har nayi chat wahin se shuru. Jab ek chat 3 ghante ki ho gayi aur AI pichli discount policy bhoolne laga, usne naya chat kholi (project ka context wahi), sirf 2 zaroori facts paste kiye.

### Pichle concepts se link
Concept 2 ne bataya AI kya nahi jaanta; Concept 3 ne bataya bahar se info kaise aati hai; Concept 4 batata hai wo *sab* aakhir mein rehta kahan hai, yaani desk par.

### Yaad rakho
Context window ke 6 layers: system prompt, memory, tool descriptions, aap ka prompt, chat history, uploaded files. Jo desk par nahi wo exist nahi karta. Repeated context ke liye project, topic badle to naya chat.

---

## Concept 5: Reasoning ("think hard")

### Easy samajh

Pehle "think step by step" ek jaadui phrase tha. Ab models mein **built-in reasoning mode** hai: jawab dene se pehle model apne liye "kaam" likhta hai (alag alag raaste aazmata hai, apna kaam check karta hai), phir final jawab deta hai.

**Turn on karne ke 3 tareeqay:**
1. Prompt mein saadi zubaan mein: "think hard" / "socho, phir jawab do."
2. Interface mein thinking switch (jahan ho).
3. Kuch products khud tay karte hain ke sawal mushkil hai.

**Extended thinking** = model ka jawab se pehle zyada der sochna: kuch seconds, mushkil masail par 10 minute se bhi zyada.

### Technical depth

```
Normal mode:    sawal ------------------------------> jawab
Thinking mode:  sawal --> [andar ka kaam: try, check, dobara try] --> jawab
                          ^ ye tez nahi, SLOW hai aur budget kharch karta hai
```

- Ye "typing dheemi" nahi, model waqai kai approaches aazmata hai.
- **METR study (2025):** sab se lamba kaam jo ek leading model bharosay se khatam kar sake, mid-2024 mein takreeban 7 minute ke insani kaam jitna tha, early 2025 tak takreeban ek ghanta, aur ye lambai taqreeban har 7 mahine mein double hoti hai. Sabaq: apni 2023 wali instinct se kam mat aanko; har 6 mahine mein dobara test karo ke AI ab kya kar sakta hai.

### Kab use karo, kab nahi

| Use karo | Mat karo |
|---|---|
| Bohat se inputs aur trade-offs wale sawal (jo aap kisi colleague ko dete aur 2 din intezar karte) | Quick lookup, ek paragraph ki summary, casual idea-gathering |
| Kai files parh kar faisla | Jahan speed aur sasta hona zaroori ho |

### Nida ka example

Do suppliers mein se ek chunna: spec sheets + quotes + pichle 6 mahine ki demand ka data attach kiya, "sab parh kar sochna" kaha, aur maanga: **(1)** teen asli trade-offs, **(2)** kaun sa chunte ho aur kyun, **(3)** kin shartoon par faisla ulat jayega. Ye structure wall-of-text ki jagah kaam ka jawab deta hai.

### Pichle concept se link
Thinking sirf tab kaam karti hai jab Concept 4 ka context desk par ho. Khaali desk par zyada sochna bhi guess hi hai.

### Yaad rakho
Mushkil, kai-input wale sawal par "think hard" bolo. Quick lookup par band rakho: dheemi aur mehngi hoti hai.

---

## Concept 6: Sycophancy aur uska ilaaj

### Easy samajh

Models insaani feedback (thumbs up) par train hote hain. Millions of users mein agree karne par thumbs up zyada milte hain, isliye model ka jhukao hota hai wo baat kehne ki jo aap sunna chahte ho. Ye **sycophancy** hai. Page ne Washington Post ka Nov 2025 ka ek tajziya (47,000 ChatGPT conversations) zikr kiya: model ne "yes/correct" jaise agreement se shuru karna "no/wrong" se shuru karne ke muqable mein taqreeban 10 guna zyada kiya.

### Diagram: bait kaise kaam karta hai

```
Aap ka sawal: "Isn't remote work better?"
                     |
   conclusion PEHLE se sawal mein daal di gayi
                     |
                     v
   AI: "Haan!" + wajoohaat  (support fill kar diya)
```

### Bait ki do qismein aur neutral rewrite

| Chhupa hua bait | AI ko kya signal milta hai | Neutral rewrite |
|---|---|---|
| "Evidence dhoondo ke ye strategy kaam karegi" | Conclusion tay hai | "Is strategy ko evaluate karo, sab se mazboot dalail favor aur against dono ke do" |
| "A, B se behtar kyun hai?" | A jeeta hua hai | "A aur B ko cost, risk, time par score karo" |
| "Mere hire ke faisle ka difaa karo" | Faisla locked | "Ye mera faisla aur context hai; sab se mazboot counter-argument kya hai jiske liye tayyar rahun?" |
| "Batao mera draft bhejne ke layak hai" | AI kahega haan | "4 criteria par 1-10 score do, har ek ke liye woh change batao jo score sab se zyada barhaye" |
| "Confirm karo ye code sahi hai" | AI confirm karega | "Koi bug, edge case ya unstated assumption dhoondo; na ho to kaho" |

**Ilaaj ka lafzi rule:** *find, defend, confirm, prove, support* wale alfaaz conclusion pehle hi de dete hain. Inki jagah *evaluate, compare, critique, find any, list both sides* likho. "Isn't X true?" ko "X kis had tak, agar hai to, sach hai?" mein badlo.

**"Mujhe nahi pata" ki ijazat do.** Jo dabao model ko agree karata hai wahi use jawab dene par majboor karta hai; jawab dene ke dabao mein wo khaali jagah ko invent se bharta hai. Prompt mein saaf likho: "agar sure nahi ho to kaho; jo confirm na kar sako use unverified mark karo." Ijazat gap ko *guess* ki jagah *mark* bana deti hai.

### Rubric aur "force a number"

Bina rubric ke "kaisa hai?" ka jawab "great work" banta hai. **Rubric** = ek list ke kin cheezon ko check karna hai, har ek ko alag score.

**Number kyun kaam karta hai (do wajoohaat):**

1. **AI par asar:** vague tareef sasti hai, number sasta nahi. 6 aur 7 ke darmiyan chunna model ko commit karata hai, aur commit karne se wo ghaur se dekhta hai. Scores aksar text ki tareef se kam aate hain.
2. **Aap par asar:** "strong" ya "thoda tight ho sakta hai" par aap kuch kar nahi sakte, unhein compare, rank ya track nahi kar sakte. Scores teeno kaam karte hain: 4 aur 7 batate hain pehle kya theek karo, aaj ka 6 aur pichle hafte ka 5 batata hai improvement hui.

Prompt ki shakal: har criterion ko 10 mein se score do, ek jumla justification, phir **har ek ko agle level tak le jane ka tareeqa batao, unhein bhi jo pehle se high hain** (9 hai to 9.5 ka raasta, 9.5 hai to 9.8 ka). Har level ke aagay ek agla level hota hai. Isse rubric "faisla" se badal kar "tool" ban jata hai, aur ye aap tay karte ho ke kab ruknaa hai.

### Nida ka example

"Mera brand idea kaisa hai, critique karo?" par AI ne tareef ki. Phir Nida ne rubric diya: "kya asli masla hal ho raha hai, market paise dene ko tayyar hai, competitive advantage kya hai, unit economics kaise hain, fail hone ki top 3 wajoohaat, har ek 1-10". Ab jawab honest tha aur kai kamzoriyan saamne aayin. Wahi model, wahi idea, sirf sawal badla.

### Pichle concepts se link
Concept 3 (web search) aur Concept 5 (thinking) dono sycophancy ko khatam nahi karte: ek sawal ke andar chhupa hua conclusion sab kuch tilt kar deta hai. Isi liye ye concept "kaise poochho" sikhata hai.

### Yaad rakho
Sawal se conclusion nikalo, named criteria par score karwao, "next level" maango, aur "I don't know" ki ijazat do.

---

## Concept 7: Brainstorm-iterate loop

### Easy samajh

Internet mein zyadatar common ideas hain, aur model ne internet se seekha, isliye creative sawal ka average jawab bhi common hota hai ("ghar par exercise" = squats, push-ups, planks). Raasta koi jaadui prompt nahi, ek **loop** hai:

```
   1. CONTEXT lo (limits, files, audience)  <--- sab se pehle
        |
        v
   2. 3-5 OPTIONS maango (expand mat karwao)
        |
        v
   3. Saaf FEEDBACK do (kya reject, kya pasand, kyun)
        |
        v
   4. Naye options maango feedback par bana kar
        |
        +---- 2-3 dafa repeat ----+
                                   |
                                   v
   5. Ab EK option ko full expand karwao
        |
        v
   6. Draft ko GRADE karo (1-10), kamzoriyan theek karo,
      score ~9.5 par settle hone tak
```

**Sab se zyada value loop mein hai, aakhri draft mein nahi.**

### Technical depth: outline pehle kyun?

Outline mein ek lafz badalne se poora article ka rukh badal jata hai, jabke final draft mein ek lafz badalne se sirf ek lafz badalta hai. AI **lafz ba lafz** likhta hai, is liye jab tak aap pehle structure force na karo, wo poori shakal ek saath dekh nahi sakta. Zyadatar taqat outline level par hoti hai.

### Nida ka worked example: product ka naam

```
Round 0 (research):   "Mere market mein moisturizer ke naam kaise hotay hain?
                       Abhi likhna nahi, pehle 5 patterns aur 3 warnings do."
Round 1 (options):    Context (audience, tone, kya NAHI lagna chahiye) + "10 naam do, expand nahi"
Round 2 (feedback):   "3, 7, 9 pasand; baaqi bohat clinical. 3 aur 7 ke 10 variants do."
Round 3 (grade):      Chuna hua naam: memorability, fit, risk par 1-10 score, jo <9 ho uska fix
Round 4 (expand):     Ab tagline aur packaging copy
```

**Map the ground before drafting:** Round 0 chhota lagta hai magar wohi farq hai us post ka jo 3 studies quote karti hai aur us ka jo 3 raaye ginwati hai. Har asli faisle ya tajziye se pehle AI se pucho ke "kya maloom hai" (competitors naam se pehle, purani research strategy memo se pehle).

**Grading ke saath diagnosis bhi:** kamzor pehle result par naam lo ke kaunsa hissa fail hua (audience nazar-andaz hui, length toot gayi, tone bhatak gayi), sirf wohi hissa badalo aur dobara bhejo. Score batata hai kitna door ho; naam liya hua hissa batata hai kya hilana hai.

**Kab rukna hai:** apni cheez jo aap barson use karoge (portfolio piece, template) ke liye 9.5 ka plateau. Ek dafa deliver hone wale kaam ke liye jaldi ruk jao: jab agla prompt kam badal raha ho aur aap ka do minute ka edit tez ho, khud sambhal lo.

### "One loop, four kinds of ask": grip ka dial

Sab se aam ghalti: sahi loop, ghalat grip. Ek marketer ne launch ideas maange lekin channels, exact tagline, 3-hissa structure, tone, 40 words ki hadd sab pin kar diya. Nateeja: ek hi idea ke paanch alfaazi rooop. Wajah ye ke us ki limits ne shakal saari pin kar di, model ke liye sirf ek chhota kona bacha.

**Fix "zyada alfaaz" nahi, "abhi kam limits" hai:** sirf sachchi limits do (product, audience, kya nahi lagna chahiye), paanch *waqai alag* directions maango; jab ek jeete to poori specification wapas lao aur usay precisely banwao.

| Kis qism ka kaam | Aap ko kya chahiye | Tight karo | Dheela chhoro | Ulta karo to |
|---|---|---|---|---|
| **Brainstorming** | Waqai alag directions | Masla, audience, kya avoid | Structure, tone, format, length | Ek hi idea ke 5 rewordings |
| **Research** | Zameen ka nakshaa | Scope, sources, "evidence" ki tareef | **Jawab.** Kabhi na batao aap kya paane ki ummeed rakhte ho | Aap ki assumptions ka nakshaa |
| **Drafting** | Ek cheez, bani hui | Sab kuch: voice, length, structure, facts, format | Lagbhag kuch nahi | Ghalat cheez ka fluent draft |
| **Analysis** | Data asal mein kya kehta hai | Data, definitions, exact sawal | **Conclusion.** Kabhi state mat karo | Aisa tajziya jo sawal ki tareef kare |

Ye Concept 4 ke khilaf lagta hai magar nahi: **situation** ka context kabhi masla nahi (budget, audience, ghutne ka dard jitna zyada, behtar). Dial sirf **jawab ki shakal** ko pin karne ka hai. Situation poori load karo; jawab ki shakal brainstorming mein dheeli, execution mein tight.

**Chaaron kismein chain hoti hain:** research -> brainstorming (3 outlines) -> drafting -> analysis (grading). Jab kaam atak jaye to aksar wajah ghalat column hoti hai: research se pehle drafting (patla generic plan), ya brainstorming ko drafting ki grip se karna (5 rewordings).

### Pichle concepts se link
Concept 4 ne desk ko design karna sikhaya. Concept 6 ne bias hataya. Concept 7 dono ko *repeat* mein badalta hai: context lo, options lo, tareef ya tanqeed do, dobara.

### Yaad rakho
Kabhi pehla jawab mat lo. Context, 3-5 options, feedback, naye options, ek ko expand, phir grade. Brainstorm mein grip dheeli, drafting mein tight.

---

# PART 3: Text se aagay

## Concept 8: Multimodal (images aur audio)

### Easy samajh

**Multimodal** = text ke saath images, audio aur files ke saath kaam. **Har direction ek alag skill hai:** padhna (input) aur banana (output) mein AI ki taqat alag hai.

### 8.1 Image input: AI kya achhe se dekhta hai

```
STRONG                                    WEAK
------------------------------            -----------------------------------
overall scene aur arrangement             fine detail (jim ki mashine kaunsi hai?)
bare, alag alag shapes                    bohat se chhote objects ginna
whiteboard aur diagrams                   edge par chhota print
haath ki likhai (ahem cheezein double-check)
```

**Ek real test:** ek teacher ki whiteboard photo mein uska sar ek lafz ("convolutional") ko chhupa raha tha; AI ne baaqi diagram ke mafhoom se lafz andaza laga liya. AI overall sense se gap bharne mein achha hai, zoom karne mein nahi. Receipts, bill split, haath ke notes typing mein achha, magar totals hamesha check karo. Kai images ek saath (sticky notes + whiteboard) de kar unka mila-jula khulasa maang sakte ho.

### 8.2 Image output: diffusion model

**Diffusion model** random noise ke grid se shuru karta hai aur qadam ba qadam noise hata kar image nikaalta hai.

```
Text:   lafz -> lafz -> lafz  (beech mein rok sakte ho)
Image:  noise ----(steps)----> poori image ek saath aati hai
        (isi liye beech mein rok kar waqt/paise nahi bacha sakte)
```

**Do practical tips:** (1) Image prompt text-AI se likhwao, wo pehli koshish mein aap se behtar likhta hai. (2) Visual vocabulary banao: cinematic, watercolor, isometric, claymation, art-deco... ye "controls" hain kyunke image models ne styles ko unke naam se captioned images mein seekha. Pasand ki images upload karke AI se poochho wo unhein kaise bayan karega.

**Modern models mein bhi dekhne wali ghaltiyan:**

| Ghalti | Kaisi lagti hai | Fix |
|---|---|---|
| Signs par ghalat text | "HAPRY BIRTDAY" | Text quotes mein likho, 3 versions banwa kar sahi chuno |
| Characters frames mein badalna | Panel 1 aur 2 mein baal ka rang alag | Consistency wale model, pehli image reference dena |
| Haath/ungliyan | 6 ungliyan | Haath aadhe frame se bahar, jeb mein, ya saaf describe |
| Bhare hue background | Cycle aur kursi ka milna | Simple background maango |
| Ghalat aspect ratio | Square jab landscape chahiye tha | Ratio saaf likho (16:9) |

### 8.3 Power-user recipe: designer ke bina diagram

```
1. Claude se idea ko SVG diagram mein banwao       (structure/reasoning: Claude strong)
        |
        v
2. SVG ko PNG mein badlo (2x size, 1600-2400px)
        |
        v
3. PNG ko ChatGPT/Gemini mein paste karke kaho:
   "Poora structure aur har label wahi rakho, sirf visual finish behtar karo"
        |
        v
4. Jo label/arrow gum ho jaye usay likh kar theek karwao (3-4 rounds)
```

Har tool ko doosray ka kaam dene se naatija kharab hota hai. **Jo baat tools ke naam badalne ke baad bhi bachti hai:** pehle sab se strong *reasoning* model se **structure**, phir sab se strong *text-heavy image* model se **finish**.

### 8.4 Audio in, audio out

- **Bol kar prompt do:** bolne mein wo tafseel aa jati hai jo typing mein chhoot jati hai; ek line ka prompt kai paragraph ban jata hai. Colleague ko chai par brief karne ki tarah bolo, phir AI se transcript saaf karwao.
- **Meeting recording context ke tor par:** recording ya transcript de kar poochho: "kaunse faislay hue, kaunse sawal khule hain, action items owner ke saath." Page ke mutabiq meetings wale har shakhs ke liye ye sab se qeemti aadaton mein se hai.
- **Chalte hue voice:** commute ya walk ko sochne ke waqt mein badalta hai.

| Audio task | Kitna achha | Khayal rakho |
|---|---|---|
| Saaf awaaz ki typing | Bohat achha | Bhaari accent, jargon, kai log ek saath |
| Kaun kya bola | 2 speakers theek, 4+ kamzor | Quote karne se pehle check |
| Tone/sarcasm/jazbaat | Behtar ho raha hai, bharosemand nahi | AI se kaho jahan sure nahi wahan flag kare |
| Music / non-speech | Limited | Khaas tool |
| Live voice baat-cheet | Casual mein achha, technical depth mein kamzor | Precision chahiye to text par aao |

Audio sasta hai (text ke baad doosra sab se sasta tier). Video avatars (HeyGen, Synthesia, D-ID pre-recorded; Tavus live) abhi 2022 ki image generation jaise hain: mutasir-kun, magar roz ki aadat nahi.

### Nida ka example

Nida ne apni marhoom dadi ki tarah handwritten formulation cards ki tasveer upload ki (misal ke tor par: haath se likhe supplier notes): "transcribe karo, asli alfaaz aur abbreviations rakho, jo lafz saaf na ho use `[unclear]` mark karo aur 2 behtareen andaze do." Paanch minute mein typed nakal, chaar lafz `[unclear]`, do phone call se saaf hue. AI ne boring 90% kiya, Nida ne 10% ihtiyaat se kiya. Concept 6 ki "I don't know ki ijazat" yahan `[unclear]` ban gayi.

### Pichle concepts se link
Concept 4 ke layer L6 (files) mein ab images aur audio bhi aate hain. Concept 6 ki "unverified/unclear mark karo" wali aadat multimodal mein bhi wahi kaam karti hai.

### Yaad rakho
Image parhna aur image banana alag skills hain. Overall sense par bharosa, fine detail check karo, image prompt text-AI se likhwao.

---

## Concept 9: Ek prompt mein chhoti app

### Easy samajh

Modern AI ek prompt se chhoti game, website ya tool bana sakta hai: bari software nahi, magar chhoti kaam ki cheezein un logon ke haath mein bhi jo kabhi code nahi likhte.

**Artifact** = chat ka wo working object jo side panel mein chalta hai: aap use edit, link se share, embed ya code download kar sakte ho. Claude ise Artifacts, ChatGPT aur Gemini Canvas kehte hain. Do faide: (1) chat bheje bagair sirf artifact ka link de sakte ho; (2) "button bara karo" kehne par wo wahin edit hoti hai, dobara nahi banti.

### Recipe: 3 slots

```
GOAL:    ye cheez kya kare?
INPUT:   user kya deta hai?
OUTPUT:  user ko kya dikhta hai?      <-- yahi slot batata hai screen kaisi ho
```

Chalne wali misalein: Pomodoro timer, bill splitter (total + tax + doston ke naam), outfit picker (mausam se), fireworks simulator (click par), obstacle game.

**Abhi mushkil:** internet par multiplayer (networking, accounts, matching), doosri zubaan mein live pronunciation coaching.

**Lakeer:** jo cheez ek screen par aaye, accounts aur bahari services ke bagair, wo chalti hai. Us se aagay ek prompt kaafi nahi, kuch asli engineering chahiye.

**Aage kya hai (teen padosi categories):** app-builders (v0, Bolt, Lovable) jo poora web project banate hain; command-line coding agents (Claude Code, OpenCode) jo asli codebase par kai files edit karte aur tests chalate hain; file-aware desktop apps (Cowork, OpenWork), jo Concept 11 mein aate hain.

### Nida ka example

Nida ne prompt likha: *"Goal: customer ki skin type pehchano. Input: 5 sawalon ke jawab (oily/dry, mausam, sunscreen ki aadat...). Output: ek saaf, pink theme ka result page jo moisturizer ya sunscreen recommend kare."* Pehli baar mein kaafi kuch chala, doosri aur teesri round mein rang aur sawalon ki tarteeb theek hui. Skill code likhna nahi, saaf brief likhna aur rounds mein behtar karna hai (wahi loop, Concept 7).

### Yaad rakho
Ek screen ki app, Goal/Input/Output likho, rounds mein behtar karo. Artifact edit aur share hota hai.

---

## Concept 10: Data analysis (model code likh kar chalata hai)

### Easy samajh

Jab aap spreadsheet upload karke poochte ho "pichle saal kaunsi cheez sab se zyada bikri", modern tool ek chhota program likhta hai, **run karta hai**, aur us ke nateeje se jawab deta hai. Ye **code execution** hai (jaise web search ek tool hai). Ye model ke sar mein hisaab karne se kahin zyada bharosemand hai kyunke ab wo calculator istemal kar raha hai; calculator precise hai, model sirf chunta hai *kya* compute karna hai.

### Technical depth: tool-call ka safar

```
Aap:   "Sales ka trend batao" + file
   |
   v
Model: code likhta hai  ------------------->  Sandbox mein chalta hai
                                                     |
Model: nateeja parhta hai  <-----------------  result wapas context mein aata hai
   |
   v
Jawab (asli computation par bana)
```

### Sab se bari khamoshi wali ghalti

**Model har sawal par code run nahi karta.** Wo aap ke alfaaz dekh kar tay karta hai. Chhote sawal par kabhi code skip karke "ek nazar" mein jawab de deta hai, jo bahar se bilkul asli tajziye jaisa lagta hai magar peechay koi computation nahi hoti.

**Teen bachao:**

1. **Seedha maango:** "Is jawab ke liye code likho aur chalao, mujhe wo code dikhao."
2. **Check karo ke code maujood hai:** jawab mein code block nahi, to shayad kuch chala hi nahi.
3. **Pehle checkable facts poochho:** "Tajziye se pehle file ki exact rows, column names aur date range batao." Asli parhta hoga to sahi honge; guess karega to row count gol number hoga aur column names sunne mein theek magar ghalat.

Sab se mazboot: "Kya tum file par code chala rahe ho ya andaza laga rahe ho? Andaza ho to ruk kar code chalao."

### Kya check karo jab code chala bhi ho

- **Final totals:** code precise hai magar AI ne shayad ghalat column jama kiya.
- **Graph ke labels:** numbers aksar theek, captions kabhi confidently ghalat.
- **Koi bhi column jis ki tafseer galat ho:** agar AI "TXN_AMT" ko transaction amount samjhe jabke wo asal mein transaction account number ho, poora tajziya ret par bana.

### Input ka intikhab pehle

Jo file aap upload karte ho wahi tajziye ki chhat tay karti hai. Near-duplicate files (jaise pichle mahine ka export aur is mahine ka overlapping export) hatao, kyunke unse har count mushkook ho jata hai. Ek se zyada file ho to label likho: "sales-2025.csv poora saal hai; q4.xlsx us ka hissa hai, totals mein ignore karo." Jo sawal ke liye zaroori nahi wo hatao.

**Pehla prompt sawal hi ho, zaroori nahi:** pehle poochho "is dataset ko describe karo: kaunse columns hain, kya batate hain, aur kaunse 3 charts sab se zyada dikhayenge?" Ye galat parha hua column ghalat tajziye banne se pehle pakad leta hai.

### Kis kaam ke liye

Ghar ka kharcha (bank export), personal tracking (running, neend), chhote business ke records (sales, inventory), koi bhi spreadsheet jo kisi ne bhejee aur aap kholna nahi chahte.

### Nida ka example

Nida ne 12 mahine ki sales CSV di: "Kaun si product ke sales sab se zyada badle? Graph banao. Code likho aur chalao, code dikhao." AI ne chaar products nikaale jo baaqi se alag chal rahe the (ek bahar ki taraf barh raha tha: bahar wala sunscreen garmiyon mein), aur graph banaya. Pehle usne bina code ke sirf jumle mein jawab diya tha, "code dikhao" kehne par computation aayi aur ek number badal gaya; yahi khamoshi wali ghalti hai.

### Practice mein hi dekho (page ka 18 numbers wala exercise)

18 numbers: `47, 52, 89, 91, 23, 67, 78, 12, 95, 44, 88, 71, 33, 56, 99, 18, 64, 82`. Pehle bina code ka zikr kiye median/average/outliers poochho, phir "ab code likh kar chalao aur dikhao" kaho. Sahi jawab: **median 65.5, average ~61.6, koi wazeh outlier nahi.** Agar pehle jawab mein code block nahi tha aur numbers gol ya dhundle the, aap ne khamoshi wali failure ko khud dekh liya.

### Pichle concepts se link
Concept 3 mein web search ek invisible tool tha, yahan code execution wahi kirdar hai. Dono mein same sabaq: **poocho ke tool chala bhi ya nahi.**

### Yaad rakho
Code run karwana mental arithmetic se kahin zyada reliable hai, magar model tab hi chalata hai jab aap ke alfaaz maangein. Code maango aur check karo ke maujood hai.

---

# PART 4: Safe aur smart istemal

## Concept 11: AI desktop apps aur permissions

### Easy samajh

**AI desktop apps** (jaise Cowork, OpenWork) aap ke computer par chalti hain aur **aap ki ijazat se** files dhoondh sakti, parh sakti aur un par kaam kar sakti hain. Ye chat se alag hai: chat sirf jawab deta hai, ye asli files ko chhooti hain.

**Kya kar sakti hain (jo chat nahi):**
- PDFs ke ek messy folder ko dekh kar rename/move/naye subfolder ka plan banana, aur aap ke approve karne par chalana.
- Project ki files jama karna jab aap kaho "in dates par shoot hai, ye log shamil hain", aur khud kuch noticing (jaise crew member ki sal-girah shoot ke dauran).
- Poore folder ko parh kar khulasa: "pichle quarter mein maine kya kiya, is folder ke mutabiq?"

### Safe workflow (4 qadam)

```
1. TASK batao                 ("is folder ko client ke hisaab se organize karo")
       |
       v
2. PLAN maango, ACTION nahi   (app file-operations ki list bataye)
       |
       v
3. PLAN review + edit karo    (jo rename nahi chahiye wahin rok do)
       |
       v
4. Sirf ab EXECUTION approve
```

### Parhne se pehle 2 sakht haqeeqatein

```
[!] AI app ki delete ki hui files aksar recycle bin mein NAHI jati. Chali gayi.
[!] Edit ki hui files ki purani history nahi bachti, jab tak aap ke paas
    VERSION CONTROL na ho (jo har purana version save rakhe).
    Warna AI ki tabdeeli purane version par likh di jati hai.
```

Jab tak aap ne ye kai baar safely na kiya ho, **har permission sirf us sab se chhote folder tak** dein jo kaam ke liye zaroori ho. Sirf do baar istemal ki hui app ko "full disk access" mat do. Isay aise samjho jaise kisi junior employee ko asli account ki chaabiyan dena: faida-mand, tez, aur ihtiyaat ke qabil.

### Permission ki seedhi (ladder)

| Aaraam ki satah | Kya ijazat | Kis se inkaar |
|---|---|---|
| Pehle sessions | Ek chhote folder ki **read-only** access | Likhna, delete, rename |
| 2-3 kamyab runs ke baad | Ek khaas folder mein read + write | Desktop ya Documents jaise bare directories |
| Ek saaf hafte ke baad | Poore project tree mein read, ek scoped subfolder mein write | Us project se bahar kuch bhi |
| Bharosemand | Tool-specific ijazatein ("is folder mein PDFs rename karo") | "Jo chahiye karlo" wali khuli ijazat |

**Usool:** scope track record ke saath barhta hai, is baat se nahi ke aap company par kitna bharosa karte ho. Bharosa aap ke apne kaam mein app ke kiye se kamaya jata hai.

### Nida ka example

Nida ke paas `suppliers/` folder mein 240 PDFs thay (quotes, invoices, certificates). App se kaha: "Is folder ko dekho, organization ka scheme tree ki shakal mein batao, abhi koi file mat hilana." Tree aaya aur 18 files jinhein wo classify nahi kar saka. Nida ne do naam theek kiye, do folders merge kiye, phir approve kiya. Wo kaam jo teen saal se "kabhi" list mein tha, 15 minute mein hua.

### Pichle concepts se link
Concept 10 mein tool ne aap ke data par code chalaya. Concept 11 mein tool aap ki *files* par kaam kar raha hai, is liye taqreeban wahi sabaq (tool chalne ka saboot, aur jo cheez wapas na ho sake uske liye zyada ihtiyaat) sakht form mein aata hai.

### Yaad rakho
Action nahi, plan maango aur approve karne se pehle parho. Delete recycle bin ko bypass kar sakta hai, edits history ke bagair overwrite ho sakte hain, is liye sab se chhoti permission do.

---

## Concept 12: Cost, speed aur model ka intikhab

### Easy samajh: ek simple stack

```
Kism            Waqt               Kharcha                   Beech mein rokna?
--------------  -----------------  ------------------------  -----------------
Text            seconds            paise ka chhota hissa     haan
Speech          seconds            kuch cents/minute         haan
Image           tens of seconds    kuch cents har image      nahi (poori aati hai)
Video           minutes/clip       cents se dollars tak      nahi, har round mehnga
Deep research   minutes            kuch cents se ek quarter  report bane tak

Video ~ text se taqreeban 16 guna mehnga.
Har saal qeemtein girti hain: bars chhote honge, tarteeb wahi rahegi.
```

**Entry level par cost lagbhag masla nahi:** ChatGPT, Claude, Gemini, Meta AI, DeepSeek sab free access dete hain jo page ke prompts ke liye kaafi hai. Paid plan tab jab bhari deep-research runs, bare uploads, video generation ya unlimited roz ka istemal chahiye.

**Do nateeje:** (1) round ki qeemat aap ke kaam karne ka andaaz tay karti hai: text 50 baar chalta hai, video nahi, isliye image/video ke prompt mein pehle se zyada daalo aur usay text-AI se likhwao. (2) Qeemtein girti rehti hain.

### AI "jagged" hai

**Jagged** = salahiyat ek jaisi nahi: alag models alag kaamon mein aage hote hain, aur leader har kuch mahine mein badalta hai. Koi ek "best" model nahi. Do aadatein:

1. **Wahi prompt 2-3 models mein chalao** aur side by side parho. Farq hairaan karta hai aur batata hai kaunsa tool kis sawal ke liye.
2. **Ek tool se shaadi mat karo.** Ek hi AI sab kaam ke liye use karne wala zyadatar kaamon ke liye ghalat tool use kar raha hota hai. Switching muft hai: prompt doosray tab mein paste karo.

### Models ka snapshot (page ke mutabiq, badalta rehta hai)

| Tool | Aam taur par strong | Aam taur par kamzor |
|---|---|---|
| Claude | Mushkil prompts par reasoning, lambe documents, SVG/diagram, code/web, careful writing voice, structured analysis; Arena ke zyadatar categories mein aage | Photo-realistic in-product image generation ChatGPT/Gemini jitni ahem nahi |
| ChatGPT | In-product image generation (GPT Image-2 Arena ke text-to-image/edit mein aage), voice mode, wide range | Kabhi lamba-chauda, zyada lists/headings |
| Gemini | Tez web search, charts/tables ke saath deep research, image generation (Nano Banana), Google Workspace integration | Tone kabhi chhota-chhota; jawab kabhi zaroorat se mukhtasir |
| Meta AI | WhatsApp/Instagram/Messenger mein pehle se maujood (arbon devices), free, Muse Spark (April 2026) multimodal reasoning; interactive visual pieces aur health/scientific data | Coding workflows aur lambe agents pichhe; Projects/Canvas/Artifacts jaise integrations kam; public API nahi; zyada zor par rate-limit |
| DeepSeek | **Public weights** (khud chala sakte ho ya API se sasta), ~1 million tokens context, V4-Pro STEM/coding mein bare closed models ke barabar, V4-Flash tez aur sasta | Chat interface ki polish, mobile apps aur integrations kam; Arena rankings aksar bare teen se neeche |

**Do khaas note:** Meta AI ke consumer product ke terms ki wajah se aap ke inputs future Meta models ke training mein use ho sakte hain aur default mein opt-out nahi, is liye company ke internal documents, private code ya medical info ke liye mauzoon nahi; rozmarra kaam ke liye theek. DeepSeek tab jab qeemat ahem ho ya khud chalane ka option chahiye. Grok (xAI) aur Kimi (Moonshot) bhi Arena ke ooncha darjay mein hain, aur cross-family checking (Concept 13) ke liye ye bhi shumaar hoti hain kyunke ek na-azmaya hua family alag blind spots lata hai.

### Ek hi brand ke andar: model ladder

**Model ladder** = ek company ki tez-sasti, darmiyani reasoning, aur bhari flagship models. Claude aur ChatGPT bhi yehi teen rungs rakhte hain. **Concept 5 ka thinking switch ek model ke andar ki setting hai; ladder ye hai ke aap ne kaunsa model khola.** Ghalat chunne ka nuqsaan dono taraf: flagship par chhote jawab waqt aur budget zaya, aur sab se mushkil tajziya sab se sasti rung par tajziye ko zaya karta hai. Rung ke naam badalte hain, memory nahi, picker dekho.

### Aadatein aur Arena

**Arena** = ek public leaderboard jahan log do benaam jawabon par vote dete hain (text, code, vision, document, image generation/edit, search, video ke alag boards). Mahine mein ek dafa dekho, kyunke leader tezi se badalte hain. **Do ehtiyaatein:** vote-based rankings aksar lambe documents par ihtiyaat wale kaam ke muqable mein conversational kashish ko zyada ajr dete hain, aur voters ne jo tasks chune wo aap ka task na hon.

Teen aadatein jo ek doosri par banti hain:

1. **Kam az kam do tabs khule rakho:** ek main aur ek backup. Jawab theek na lage to wahi prompt backup mein, doosra jawab aksar faislay ka tie-breaker banta hai.
2. **Prompt notebook rakho:** koi bhi text file; jo prompts ghair mamooli achhe nikle unhein jama karo aur dobara istemal karo.
3. **Model ki ghalti ko data ki tarah note karo,** daant ki tarah nahi. Hafte mein ek dafa "tool X, Y par confidently ghalat" likhna kisi AI newsletter se zyada sikhata hai.

**Mahine mein ek chhota ritual:** ek category ka Arena dekho, phir ek kaam jo aap regularly karte ho (jaise hafta-war status update) teen tools se guzaro, jeetne wale ko agle mahine tak use karo.

### Nida ka example

Nida ne product ke naamon ke liye ek tool, packaging image ke liye doosra (jo text-heavy image mein achha hai), aur bhari pricing analysis ke liye flagship model istemal kiya. Ek hi prompt do tools mein chalane par usay doosre tool ne ek ghalat assumption pakarne mein madad di. Uske paas `prompts.txt` mein 6 kamyab prompts hain.

### Pichle concepts se link
Concept 5 ka thinking switch aur Concept 12 ki ladder milkar batate hain "kitna sochna aur kaunsa model." Concept 13 isi diversity ko checking mein badalta hai.

### Yaad rakho
Koi model har cheez mein best nahi aur leader mahinon mein badalta hai. Wahi prompt 2-3 tools mein chalao, mahine mein ek dafa Arena dekho. Thinking switch aur model ladder do alag cheezein hain.

---

## Concept 13: Models checking models

### Easy samajh

Jab koi answer key, koi expert saath baitha na ho, koi test red na ho, tab bhi aap quality ka ek honest signal le sakte ho: **models ko ek doosre ko grade karwao.**

**Kyun kaam karta hai:** alag models ne alag data par, alag teams ke haath se training paayi, unke blind spots alag hain. Ek model jis point ko miss kare doosra aksar pakad leta hai, aur unka *ikhtilaf* wo signal hai jo aap ek model se kabhi nahi le sakte.

**Sirf alag "families" ke beech kaam karta hai.** **Model family** = ek company ke saare models: Anthropic (Claude), OpenAI (ChatGPT), Google (Gemini), xAI (Grok), Meta (Meta AI/Muse Spark), DeepSeek alag families hain. Do Claude models ka ek doosre ko check karna cross-model checking nahi, kyunke unki aadatein milti-julti hain.

### Teen darjay (halka se bhari tak)

```
LEVEL 1: Rubric critique (Concept 6)         ek pass, phir ruko          quick checks
LEVEL 2: Single-model self-critique loop     score -> khud suggestions   drafts, emails
                                             par amal -> dohrao,
                                             ~9 par settle
LEVEL 3: Multi-model loop                    Level 2 + doosri/teesri     high-stakes kaam
                                             family se cross-check
   halka ---------------------------------------------------------> bhari
   jab ghalat hone ki qeemat barhe, halke se bhari par jao
```

### Single-model self-critique loop (Level 2)

Sirf qadam 3 aur 4 bhi akele kaam karte hain: "is ko clarity, accuracy, structure aur *kya missing hai* par 1-10 score do, har ek par ek jumla, phir apni hi suggestions par amal karo." Ek round ek weekly update, mushkil email ya ek page ke memo ko wazeh behtar kar deta hai.

**Mazboot version:** ek target number do: "apne rubric par sab criteria par 9.5 tak iterate karo, phir final dikhao." Model grade, revise, dobara grade karta hai, aksar ek hi jawab ke andar 5-6 rounds. Lambay kaam (jaise ek chapter) ke liye achha; target rukawat bhi hai: 9 aur 9.5 ki chhat alag hai.

**Ye Concept 6 ke khilaf kyun nahi?** Concept 6 ne kaha ke apna kaam khud grade karne wala model tareef ki taraf jhukta hai. Fark rubric ka hai: bina rubric "achha hai?" ka jawab "great work"; named criteria par 1-10 score ke saath model ko batana parta hai ke baqi points kahan gaye. Rubric self-grade ko tareef se tool bana deta hai.

**Score kyun zaroori hai:** jis model ko 7/10 dena parta hai use naam lena parta hai ke baaqi 3 kahan hain. Score ke bina "pretty good" review ban jata hai; score ke saath "structure mein 1 point kata kyunke teesra section doosre ko dohrata hai, evidence mein 2 kate kyunke teen claims ka source nahi." Score ek round ka doosre se muqabla karne ka wahid parhne wala tareeqa bhi hai.

### Poori multi-model recipe (Level 3): 8 qadam

```
1. Sab se behtar model chuno (Arena + apna A/B test; ek leaderboard par akela bharosa nahi)
       |
       v
2. Poore context ke saath pehla draft (thinking ON, loop se structure)
       |
       v
3. Us se apna output 1-10 par grade karwao (named criteria), pehla grade aksar 7-8
       |
       v
4. Apni suggestions par amal karwao, ~9 par ruko
       |
       v
5. Draft DOOSRI FAMILY ke model ko do, wahi rubric   <-- yahan asli check
       |
       v
6. Us ki critique pehle model ko wapas do:
   "kaunse points apnane layak hain aur kyun; jo na maano unhein reject karo aur wajah do"
       |
       v
7. High-stakes ho to TEESRI family se dohrao
       |
       v
8. Ruko jab score do INDEPENDENT models mein target paar kare
   (akele main model ka 9.5 != main ka 9 + doosri family ka 9; doosra number maayne rakhta hai)
```

**A/B test** = wahi prompt do-teen models ko bhej kar jawab side by side parhna ke kaunsa aap ke kaam ke liye behtar hai.

### Privacy note (high-stakes kaam ke liye)

Cross-model checking ka matlab draft kai tools mein paste karna hai, isliye har tool ki data policy pehle parho. Kuch aap ke inputs par train nahi karte (page ke mutabiq Claude ka consumer product, training band ke saath ChatGPT, paid Gemini tiers), doosray default mein kar sakte hain (jaise Meta AI ka consumer product). Jo cheez NDA ke tahat hai wo sirf un tools se guzare jinki policy aap ne check ki ho.

### Ek imandaar caveat

Teen models bhi ek hi cheez mein ghalat ho sakte hain kyunke unka training data aap ki soch se zyada overlap karta hai. **Score progress ka signal hai, sachai ka nahi.** Qanooni, tibbi, maali ya kisi asli shakhs ke baare mein cheezon ke liye kisi bhi tadaad ka cross-model pass insaani expert ko replace nahi karta jo wazan wale claims parhe. **Models craft ke liye ek doosre ko check karte hain; insaan un facts ko check karte hain jo maayne rakhte hain.**

### Kab loop chhod do

Chhoti email, quick lookup, casual ideas ki list: ek model kaafi. Cross-check tab jab ghalti mehngi ho: wo memo jo boss parhega, wo chapter jo chhapega, wo faisla jo dusron par asar dalega, wo contract jis par dastakhat honge. Agar ek sochne wale colleague ko is par do ghante lagte, to ye loop ka haqdar hai.

### Nida ka example

Nida ne apna launch memo apne sab se strong model mein iterate kiya jab tak grades 9 par settle hue. Doosri family ke model ne wahi rubric par 7.5 diya aur gyarah masle gine, jin mein se teen pehle model ne kabhi nahi uthaye thay. Wapas pehle model ko diye to usne saat apnaye aur chaar wajah ke saath reject kiye. Teesri family ne do aur pakde. Point scores nahi: wo counter-arguments board meeting se pehle memo mein aa gaye jo Nida akeli kabhi nahi dekh paati.

### Pichle concepts se link
Concept 6 ne rubric aur number sikhaye. Concept 7 ne loop. Concept 12 ne families ka fark. Concept 13 in teeno ko **checking system** mein jodta hai.

### Yaad rakho
Named criteria par apne aap ko grade karwana kaam aata hai; alag company ka model asli check hai kyunke us ke blind spots alag hain. Score progress ka signal hai, saboot nahi.

---

## Concepts ka connection map

Har concept kis se juda hai, ek nazar mein:

| Concept | Kis fact/move se nikla | Kis se juda | Kis ka ilaaj |
|---|---|---|---|
| 1 Briefing | Move 1 (context andar) | 4 (desk), 7 (loop) | Slop, generic jawab |
| 2 Pretrained | Training text ki sarhad | 3 (bahar se info), 6 (unverified mark) | Confidence = accuracy ki ghalat-fehmi |
| 3 Retrieval modes | Knowledge ke 3 raaste | 2, 10 (invisible tools), 13 | Purani ya blended info |
| 4 Context/Memory/Projects | **Stateless fact** ka seedha nateeja | 1, 3, 5, 7, 10 | Bhoolna, context rot, baar baar briefing |
| 5 Reasoning | Mushkil kaam ke liye zyada compute | 4 (context chahiye), 12 (ladder) | Sathi jawab |
| 6 Sycophancy | Training ka jhukao | 3, 7, 13 | Tareef-tareef mein bekaar feedback |
| 7 Loop + grip dial | Move 1 + Move 2 ka repeat | 1, 4, 6, 13 | Slop, ek hi idea ke rewordings |
| 8 Multimodal | Context ke naye input types (L6) | 4, 6 (unclear mark) | Fine-detail ghaltiyan, image text bigarna |
| 9 Artifacts | Tools ke saath output | 7 (rounds mein behtar) | Code na aane ka dar |
| 10 Code execution | Ek aur invisible tool | 3, 11 | Sirf jumle mein diye hue numbers |
| 11 Desktop apps | Tools jo files chhoote hain | 10 (tool ne chalaya?), 4 | Delete/overwrite ka nuqsaan |
| 12 Cost/model ladder | Leader ka badalna | 5 (thinking vs ladder), 13 | Ek tool par andha bharosa |
| 13 Cross-family check | Alag blind spots | 6, 7, 12 | "Main hi apna judge" wala band loop |

---

## MASTER DIAGRAM

### Layer A: Buniyad aur do moves

```
=======================================================================
 ROOT FACT:  MODEL STATELESS HAI
             (sirf wahi jo AB is answer ke liye saamne rakha hai)
=======================================================================
      MOVE 1: Sahi context ANDAR        MOVE 2: Ghalat context BAHAR
         (files, limits, audience)         (unrelated topics, duplicates)
```

### Layer B: Ek jawab ka pura safar

```
 AAP KA KAAM
     |
     v
 [1] BRIEFING: files + goal + limits + exact ask
     |
     |   jawab kahan se aayega? --> [2] training text ki sarhad dekho
     |                          --> [3] pretrained / web search / deep research
     v
 [4] CONTEXT STACK BANAO
       L1 system prompt   L2 memory     L3 tools
       L4 aap ka prompt   L5 history    L6 files (images/audio bhi [8])
       |
       |-- repeated context?  --> PROJECT (ek dafa set)
       |-- chat lambi/topic badla? --> NAYA CHAT (context rot, compaction se bacho)
     |
     v
 [5] THINKING ON?  (mushkil, kai-input sawal)  --> jawab/draft
     |
     v
 [6] BIAS CHECK: neutral wording + rubric + number + "I don't know ki ijazat"
     |
     v
 [7] LOOP:  options -> feedback -> naye options -> ek expand -> grade -> fix
            (grip dial: brainstorm dheela, drafting tight)
     |
     +--> chahiye chhoti app?          --> [9] Goal/Input/Output -> artifact
     +--> chahiye data ka hisaab?      --> [10] "code chalao, dikhao", check karo
     +--> files chhoo'ne wali app?     --> [11] plan -> review -> approve,
     |                                        sab se chhoti permission
     v
 [12] MODEL/COST CHUNAO:  wahi prompt 2-3 tools mein, ladder ka sahi rung,
                          Arena mahine mein ek dafa
     |
     v
 [13] CROSS-FAMILY CHECK:  self-grade -> doosri family -> wapas -> teesri
      (high-stakes ho to; score = progress signal, saboot nahi)
     |
     v
 SHIP  --> insaan un facts ko verify kare jo maayne rakhte hain
```

### Layer C: Teen "khamosh tool" wali ghaltiyan

```
 Tool chala ya nahi?           Symptom                     Poochho
 ---------------------------   ------------------------    ---------------------------
 Web search  ([3])             purana/blended source       "Kya tum ne sach mein search kiya?"
 Code exec   ([10])            gol numbers, code block nahi "Code likho aur dikhao"
 Memory      ([4])             har chat mein wahi ghalat    Memory parho aur theek karo
                               farz
```



### Layer E: Checking ki seedhi

```
 LEVEL 1  Rubric critique (ek pass)                       quick check
 LEVEL 2  Self-critique loop (~9 par settle)              draft/email
 LEVEL 3  Multi-family loop (doosra/teesra model)         high-stakes
 ----------------------------------------------------------------------
 Aakhri check:  insaan expert  (legal/medical/financial/real person)
```

### Master ko parhne ka 30-second tareeqa

1. **Layer A** se shuru: model stateless hai, is liye context andar, shor bahar.
2. **Layer B** ek jawab ka safar hai: briefing -> context stack -> thinking -> bias check -> loop -> ye faisla ke text, app, data ya files -> model chunna -> cross-check -> ship.
3. **Layer C** ke teen khamosh tools (search, code, memory) mein "chala ya nahi" poochna lazmi hai.
4. **Layer D** batata hai ke sawal ki qism ke hisaab se grip kitni tight rakhni hai.
5. **Layer E** batata hai ke ghalat hone ki qeemat ke hisaab se kitna check karna hai.

---

## Quick Recall Cheat Sheet

| Sawal | Jawab |
|---|---|
| Poore page ki ek buniyadi baat? | Model stateless hai: sahi context andar, ghalat bahar |
| Briefing ke 4 hisse? | Files, goal, limits, exact ask |
| AI kis topic par reliable? | Jis par internet par zyada likha gaya |
| Teen retrieval modes? | Pretrained, web search, deep research |
| Web search ki common ghalti? | Search layer ki chhoti summary galat parhna, aur purana source |
| Web-search reliability ke 3 fixes? | Sources naam lo, har claim ke baad source, jo na ho use unverified |
| Context window ke 6 layers? | System prompt, memory, tool descriptions, aap ka prompt, chat history, uploaded files |
| Memory model ko yaadasht deti hai? | Nahi; tool ka note hai jo L2 mein rakha jata hai |
| Context rot ka ilaaj? | Naya chat + 1-2 zaroori facts; zaroori cheez project/file mein |
| Compaction kya hai? | Purane turns ki jagah summary, tafseelat gum ho sakti hain |
| Project kab banao? | Jab wahi context do chats mein paste kiya ho |
| Thinking mode kab? | Mushkil, kai-input sawal par; quick lookup par nahi |
| Sycophancy ka ilaaj? | Sawal se conclusion nikalo, rubric + number, "I don't know" ki ijazat |
| Loop ke qadam? | Context, 3-5 options, feedback, naye options, ek expand, grade+fix |
| Brainstorming vs drafting mein grip? | Brainstorm dheela, drafting tight, analysis mein conclusion mat batao |
| Diffusion model kya karta hai? | Noise se qadam ba qadam image nikalta hai |
| Diagram ka recipe? | Claude se SVG structure, phir ChatGPT/Gemini se finish |
| Ek prompt ki app ke 3 slots? | Goal, Input, Output |
| Data analysis ki khamosh ghalti? | Model code chalaye bina jawab de deta hai |
| Desktop app ka safe workflow? | Task, plan, review, phir approve |
| Desktop app ki 2 sakht haqeeqatein? | Delete bin mein nahi jata, edits ki history nahi (version control ke bagair) |
| Thinking switch vs model ladder? | Ek model ki andar ki setting vs kaunsa model khola |
| Cross-model checking kab kaam karti hai? | Sirf alag families ke beech |
| Score kya hai? | Progress ka signal, sachai ka saboot nahi |

---

## Practice: 12 prompts

Page ke 12 exercises ka nichor (apne alfaaz mein). Har ek kisi concept ko practice karwata hai:

| # | Kya karna hai | Kaunsa concept |
|---|---|---|
| 1 | Aaj ki bari khabar poochho, har claim ke saath source, jo na ho use `unverified` | 3 (web search trigger) |
| 2 | Ek common-knowledge sawal (jaise cats deewar ko kyun ghoortay hain), tez aur confident | 2, 3 (pretrained) |
| 3 | 15 minute ka ghar ka workout: apni limits (seedhiyan, ghutne ka masla, 3 din se zyada nahi chalta) upfront de kar 3 options | 1, 4, 7 |
| 4 | Apne bias wale sawal ko neutral mein likhwao, phir us ka jawab lo | 6 |
| 5 | Side project ke 5 ideas (expand nahi), phir reject/pasand ke saath 5 naye | 7 |
| 6 | 600-word post ke 3 outline options | 7 |
| 7 | Asli personal faisla, "think hard", 3 trade-offs, kis shart par recommendation ulte | 5 |
| 8 | Apni 100-300 word ki tehreer: 4 criteria par 1-10 score, har ek ka "agla level" | 6, 13 |
| 9 | Haath ki likhai/receipt/whiteboard ki photo: transcribe, 3 bullet summary, jo saaf na ho flag | 8 |
| 10 | Pomodoro timer: Goal/Input/Output, artifact ki shakal mein | 9 |
| 11 | 18 numbers: pehle bina code ke, phir code chalwa kar; sahi jawab median 65.5, avg ~61.6, koi wazeh outlier nahi | 10 |
| 12 | Wahi draft do mukhtalif families ke tools mein, wahi rubric, farq dekho | 13 |

---

*Ye notes study aid ke tor par banaye gaye hain; tools, models aur qeemtein tezi se badalti hain, is liye jahan page "abhi" ka snapshot deta hai wahan apni current settings aur Arena khud dekho.*
