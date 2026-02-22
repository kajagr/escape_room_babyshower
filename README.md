# 💕 Mamin Dnevnik Priprav - Baby Shower Webapp

Interaktivna webapp za baby shower event z zgodbo, nalogami in kodami za odklepanje.

## 🌸 O Aplikaciji

Aplikacija vodí udeležence skozi "Mamin dnevnik priprav" - pet posebnih strani dnevnika, kjer vsaka predstavlja del priprav mlade mamice na prihod dojenčka:

1. **Sanjanje in uspavanka** 🎵 - QR kviz z otroškimi pesmicami
2. **Skrb za prehrano** 🍼 - Baby food blind test
3. **Prvi pogled** 👶 - Puzzle ultrazvočnega posnetka
4. **Učenje o skrbi** 🍶 - Stekleničkina matematika
5. **Izbira imena** ✨ - Anagrami otroških imen

## 🚀 Deployment na GitHub Pages

### Korak 1: Ustvari GitHub repozitorij

1. Pojdi na [GitHub](https://github.com) in se prijavi
2. Klikni na "+" v zgornjem desnem kotu → "New repository"
3. Ime repozitorija: `babyshower-app` (ali karkoli želiš)
4. Nastavi na **Public**
5. Klikni "Create repository"

### Korak 2: Naloži datoteko

1. V svojem repozitoriju klikni "Add file" → "Upload files"
2. Preimenuj `babyshower-app.html` v `index.html` (pomembno!)
3. Naloži `index.html` datoteko
4. Klikni "Commit changes"

### Korak 3: Aktiviraj GitHub Pages

1. V repozitoriju pojdi na **Settings** (zavihek)
2. V levem meniju klikni na **Pages**
3. Pri "Source" izberi **main** branch
4. Klikni **Save**
5. Počakaj 1-2 minuti

### Korak 4: Odpri svojo aplikacijo

Tvoja aplikacija bo dostopna na:
```
https://[tvoje-github-ime].github.io/babyshower-app/
```

Primer: `https://marija123.github.io/babyshower-app/`

## 🔐 Prilagajanje Kod

**POMEMBNO:** Pred eventom moraš spremeniti kode v aplikaciji, da se ujemajo z rešitvami tvojih nalog!

### Kako spremeniti kode:

1. V GitHub repozitoriju odpri `index.html` datoteko
2. Klikni na ikono "edit" (svinčnik) ✏️
3. Najdi sekcijo z kodami (okoli vrstice 820):

```javascript
codes: {
    1: '0000',  // Naloga 1: Tihi otroški kviz (4 znaki - default)
    2: '0000',  // Naloga 2: Baby food test (4 znaki - default)
    3: '0000',  // Naloga 3: Puzzle ultrazvok (4 znaki - default)
    4: '0000',  // Naloga 4: Stekleničkina matematika (4 znaki - default)
    5: '0000'   // Naloga 5: Imena v zmešnjavi (4 znaki - default)
}
```

4. **Spremeni kode** glede na tvoje dejanské rešitve:
   - **VSE kode morajo biti 4-mestne** (npr. `'1234'`, `'ABCD'`, `'12AB'`)
   - Lahko kombiniraš številke in črke
   - Če je tvoja koda krajša, dodaj 0 ali črke na začetek:
     - 3-mestna: `369` → `'0369'` ali `'A369'`
     - 2-mestna: `42` → `'0042'` ali `'AB42'`
   - Primeri kod: `'7425'`, `'ABCD'`, `'12AB'`, `'0180'`

5. Klikni "Commit changes"
6. Počakaj 1-2 minuti, da se stran posodobi

### Primer prilagajanja:

Če so tvoje rešitve:
- Naloga 1: 9283
- Naloga 2: 147 → dodaj 0 → 0147
- Naloga 3: 6891
- Naloga 4: 0240
- Naloga 5: ANA → dodaj črko → ANAB (ali naredim 4-mestno ime)

Spremeniš na:
```javascript
codes: {
    1: '9283',
    2: '0147',
    3: '6891',
    4: '0240',
    5: 'ANAB'
}
```

### Kako spremeniti vrstni red nalog za ekipe:

Po defaultu:
- **Ekipa 1** dela naloge v vrstnem redu: 1 → 2 → 3 → 4 → 5
- **Ekipa 2** dela naloge v vrstnem redu: 3 → 4 → 5 → 1 → 2

Če želiš spremeniti vrstni red, najdi (okoli vrstice 830):

```javascript
teamPaths: {
    1: [1, 2, 3, 4, 5], // Ekipa 1: naloge po vrsti
    2: [3, 4, 5, 1, 2]  // Ekipa 2: začne pri 3, konča z 1 in 2
}
```

Primer spremembe:
```javascript
teamPaths: {
    1: [1, 3, 5, 2, 4], // Ekipa 1: lihe najprej, nato sode
    2: [2, 4, 1, 3, 5]  // Ekipa 2: sode najprej, nato lihe
}
```

## 📱 Mobilna Prilagoditev

Aplikacija je **že popolnoma prilagojena za mobilne naprave**! Deluje odlično na:
- Telefonih 📱
- Tabličnih računalnikih 📱
- Namiznih računalnikih 💻

Udeleženci lahko odprejo aplikacijo na svojih telefonih in jo uporabljajo med eventom.

## 🎨 Prilagajanje Besedila

Če želiš spremeniti zgodbo, navodila ali namige, lahko urejaš HTML datoteko:

1. Odpri `index.html` v GitHub-u
2. Klikni "Edit" ✏️
3. Poišči tekst, ki ga želiš spremeniti
4. Spremeni in shrani ("Commit changes")

Primer: če želiš spremeniti uvodno zgodbo, poišči:
```html
<div class="story-text">
    <p style="margin-bottom: 15px;">Danes boš prebrala posebne strani...</p>
```

## 🎁 Kako Uporabiti na Eventu

1. **Pred eventom:**
   - Prilagodi vse kode v aplikaciji (vse 4-mestne!)
   - Pripravi fizične naloge (QR kode, kašice, puzzle, stekleničke, kartice z imeni)
   - Pripravi 2 seta nalog (ali 1 set, ki ga ekipe uporabljajo skupaj)
   - Testiraj aplikacijo
   - Pripravi škatlo z ključavnico in avtomobilčki notri

2. **Na eventu:**
   - Razdelite udeležence v 2 ekipi
   - Vsaki ekipi daj povezavo do aplikacije
   - **Ekipa 1 izbere "Ekipa 1 🌸"** → dela naloge 1, 2, 3, 4, 5 (po vrsti)
   - **Ekipa 2 izbere "Ekipa 2 🌼"** → dela naloge 3, 4, 5, 1, 2 (druga pot)
   - Tako obe ekipi delata različne naloge hkrati, a obe na koncu obdelata vse
   - Lahko jo odprejo s QR kodo (uporabi generator QR kod online)
   - Rešujejo naloge v živo in vnašajo kode v aplikacijo (vedno 4 znake!)
   - Aplikacija jih vodi skozi zgodbo
   - Na koncu dobijo končno kodo za škatlo z nagrado! 🎉

3. **Zakaj 2 ekipi?**
   - Manj gneče pri nalogah - vsaka ekipa začne drugje
   - Bolj dinamično in zabavno
   - Tekmovalen element
   - Na koncu obe ekipi obdelata vse naloge

## 💡 Nasveti

- **Testiraj vse kode** pred eventom!
- **Shrani rezervno kopijo** kod nekje drugje
- Lahko naredíš **QR kodo** za aplikacijo, da jo udeleženci lažje odprejo
- Če je skupina velika, lahko **razdeliš v ekipe**
- Pripravi **rezervne žličke** za baby food test
- Označi **alergene** pri kašicah!

## 🔧 Tehnične Podrobnosti

- **Framework:** Vanilla JavaScript (brez odvisnosti)
- **Stil:** Custom CSS z Tailwind principi
- **Fonti:** Google Fonts (Caveat, Nunito)
- **Responsivnost:** Mobile-first dizajn
- **Brezplačno:** Brez stroškov gostovanja

## 📞 Podpora

Če imaš težave:
1. Preveri, ali si pravilno preimenovala datoteko v `index.html`
2. Preveri, ali je repozitorij nastavljen na "Public"
3. Počakaj 2-3 minute po vsaki spremembi
4. Osveži stran (Ctrl+F5 ali Cmd+Shift+R)

## 🌟 Uživajte!

Želim ti čudovit baby shower event! 💕👶🎉

---

**Narejeno z ljubeznijo za posebne trenutke** 💝