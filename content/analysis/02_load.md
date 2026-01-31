---
Title: Load
Description: Alla kursens rapporter.
---

# Load

# Laddningstider

Denna rapport undersöker laddningstider på tre olika golf webbplatser. För att utvärdera vilka som har bäst optimerad webbplats gällande laddningstider och mediahantering. Rapporten jämför även skillnaden mellan amerikanska och svenska golfsajter.

## Urval

---

De webbplatser som valts att undersöka är:

- [GolfDigest](https://golfdigest.com)
- [Golf.com](https://golf.com)
- [Svensk Golf](https://svenskgolf.se)

Urvalet baserades på jämförbara webbplatser med liknande innehåll men från olika geografiska marknader (USA och Sverige). Alla tre av dessa har miljontals visningar per månad och är ledande inom sitt segment.

## Metod

---

**PageSpeed Insights** [1]

- Mäter Performance Score för både mobil och desktop.
- Core Web Vital: LCP, INP och CLS [2]

**Firefox Devtools - Network** [3]

- Mäter laddningstid (load-värdet)
- Antal resurser/requests
- Total sidstorlek (MB)
- Varje sida mättes 3 gånger och medelvärdet beräknades

För varje webbplats testades tre olika sidor: startsida, nyhetssida och utrustningssida.

## Resultat

---

## Golf Digest

<figure style="margin: 0; display: inline-block; max-width:100%;">
    <img src="../image/golfdigest.png?w=700&q=70" alt="Golf digest webbplats">
    <figcaption style="text-align: center; font-style: italic;">
    Figur 1: Golf Digest webbplats
    </figcaption>
</figure>

**Testade sidor:**

- [Startsida](https://www.golfdigest.com/)
- [News](https://www.golfdigest.com/news)
- [Equipment](https://www.golfdigest.com/equipment)

## Golf

<figure style="margin: 0; display: inline-block; max-width:100%;">
    <img src="../image/golf.png?w=700&q=70" alt="Golf.com webbplats">
    <figcaption style="text-align: center; font-style: italic;">
    Figur 2: Golf.com webbplats
    </figcaption>
</figure>

**Testade sidor:**

- [Startsida](https://golf.com/)
- [News](https://golf.com/news/)
- [Equipment](https://golf.com/gear/)

## Svensk Golf

<figure style="margin: 0; display: inline-block; max-width:100%;">
    <img src="../image/svenskgolf.png?w=700&q=70" alt="Svensk Golf webbplats" width="700">
    <figcaption style="text-align: center; font-style: italic;">
    Figur 3: Svensk Golf webbplats
    </figcaption>
</figure>

**Testade sidor:**

- [Startsida](https://www.svenskgolf.se/)
- [News](https://www.svenskgolf.se/kategori/tournytt/)
- [Equipment](https://www.svenskgolf.se/kategori/utrustning/)

**Mätvärden resultat:**

(M) = Mobilt läge
(D) = Desktop läge

Core Web vitals (LCP, INP, CLS):

(LCP) Largest Contentful Paint

(INP) Interaction to Next Paint

(CLS) Cumulative Layout Shift

(PS) Performance Score

<div class="spreadsheet">
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vThkxTJuMBw2iieLlGCxl3F4f06CO-EcGhVCHgzfXKfJ8hbXxVYvSJVzu1XVhb4xpdM2jxwjjFQBHUY/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false" frameborder="0"></iframe>
</div>

## Analys

---

Efter att ha analyserat alla tre webbplatser så kommer här en sammanfattning på specifika problem och förbättringsområden.

### Golf Digest

Identifierade problem:

**1. Mobile Performance Score (42-55) är lågt** - mycket sämre än desktop-versionen.

**2. LCP värdet på Equipment-sidan är lågt, 2.2 på mobila versionen** - vilket är nära gränsen för att behöva förbättringar.

**3. Saknar INP-data på Equipment-sidan** - kan tyda på tekniska problem som bör åtgärdas..

**Eventuella orsaker:**

Stora bilder, startsidan är 12 MB.

Third parts scripts som t.ex. annonser.

Saknar lazy-loading för bilder

### Golf.com

Identifierande problem:

**1. Sämst Mobile Performance Score (28-33)** - kritiskt lågt.

**2. Väldigt stort startsida (13.8 MB)** - och Equipment-sidan har väldigt många requests (414).

**3. Desktop Performance Score är acceptabelt (60-62)** , men den mobilversionen presterar mycket dåligt.

**Eventuella orsaker:**

Tung startsidan är 12 MB.

Många annonser

Saknar lazy-loading för bilder

### Svensk Golf

Identifierande problem:

**1. Väldigt lång laddningstid på startsidan (23 s)** - överlägset längst av alla testade webbplatser.

**2. Mycket tung startsida (28.7 MB)** - nästan dubbelt så stor som de övriga webbplatserna.

**3. Bra Desktop Performance Score (52-93)** , trots långsam laddning - tyder på att huvudinnehållet visas fort men stora mängder data fortsätter laddas i bakgrunden.

**Eventuella orsaker:**

Okomprimerade bilder

Saknar caching eller effektiv CDN

Hade färre request (151) men storleken är mycket större vilket tyder på att varje fil är stor.

### Förbättringsåtgärder

Baserat på analysen finns det tre huvudsakliga förbättringsområden som är gemensamma för alla tre webbplatser:

**1. Bildoptimering**

Responsiva bilder med olika storlekar för mobil/desktop

Lazy-loading för bilder som inte syns direkt

Komprimera bilder

**2. Mobil-optimering**

Alla tre webbplatserna har mycket sämre mobil-prestanda jämfört med desktop. Detta är det största förbättringsområdet, särskilt för Golf.com som har väldigt låga mobila värden (28-33). Med tanke på att majoriteten av användare idag surfar via mobila enheter så är detta kritiskt.

**3. Caching och CDN**

Bättre caching-policies

Använda Content Delivery Network (CDN) för snabbare leverans globalt.

Optimera server-responstider

## Rangordning

Baserat på mätvärderna rangordnas webbplatserna enligt följande:

### 1:a plats: Svensk Golf

**Mobile Performance Score:** 52-55

**Desktop Performance Score:** 62-93

**Genomsnittlig laddningstid:** 23.04 s

**Core Web Vitals:** Alla gröna värden

Tar förstaplatsen tack vare genomgående bra Performance Scores, särskilt på desktop där webbplatsen når upp till 93 poäng.

### 2:a plats: Golf Digest

**Mobile Performance Score:** 42-55

**Desktop Performance Score:** 51-66

**Genomsnittlig laddningstid:** 4.55 s

**Core Web Vitals:** Mestadels gröna värden

Golf Digest tar andraplatsen med stabila resultat.
Webbplatsen har en bra prestanda och klart snabbast laddingstid (3-5.5s).

### 3:e plats: Golf

**Mobile Performance Score:** 28-33

**Desktop Performance Score:** 60-62

**Genomsnittlig laddningstid:** 4.49 s

**Core Web Vitals:** Alla gröna värden

Golf.com hamnar sist på grund av väldigt dåliga mobila Performance Scores (28-33). Med tanke på att majoriteten surfar via mobil är detta kritiskt.

## Personlig reflektering om laddningstid

Jag uppfattar laddningstider under 3 sekunder som snabba, och av de testade webbplatserna klarar endast Golf Digest startsida (3.05s) denna gräns medan Svensk Golf (23s) är extremt långsam. Dock kändes alla webbplatser generellt responsiva tack vare bra Core Web Vitals som gör att huvudinnehållet visas snabbt.

## Referenser

---

[1] Google PageSpeed Insights - https://pagespeed.web.dev/

[2] Web.dev - Core Web Vitals - https://web.dev/articles/vitals

[3] Mozilla Developer Network - Network Monitor - https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor

## Övrigt

---

**Författare:** Mats Jonströmer
