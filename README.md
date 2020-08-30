# Grupprojekt: Webshop
## TDD i Vue app
1. [Introduktion](#1-introduktion)
1. [Uppdragsbeskrivning](#2-uppdragsbeskrivning)
1. [Inlämning](#3-inlämning)
1. [Bedömning](#4-bedömning)
1. [Appendix: Arbeta med git i terminalen](#5-appendix-arbeta-med-git-i-terminalen)

---
### 1. Introduktion

Ni ska bygga en Vue-app med hjälp av testdriven utveckling, TDD. Appen ska vara en webbshop där man säljer produkter som ni väljer själva.

---
### 2. Uppdragsbeskrivning

Ni ska demonstrera att ni behärskar tekniker för att testa en lite större Vue app. Villkoren för projektet är:

+ 3-5 personer
+ arbeta agilt
+ kravspec, user stories och testfall
+ Trello
+ GitHub
+ TDD
+ Vue

Inom gruppen ska ni göra en avgränsning av uppgiften. Bestäm er för vilka sidor eller vyer (views) som ska finnas och implementera dem. Ni måste också välja vilka komponenter ni prioriterar att testa.

*Exempel: de flesta webbshoppar låter användaren se flera produkter, söka/filtrera produkter, se detaljer om en produkt, lägga till i kundvagn, se/ändra innehållet i kundvagnen, se hur mycket allt kostar.*

---
#### 2.1 Agil utveckling, kravspec och scrum
##### Steg 1
Det första ni ska göra i gruppen är att skriva en enkel *kravspecifikation*. (Den ska lämnas in i projektets slut.) Det ska vara en textfil eller ett delat dokument i molnet. Kravspec ska innehålla:
+ "dessa krav ska vårt projekt uppfylla"
    + både från utvecklarnas och användarnas perspektiv!
+ gärna skisser (tips: [Figma](https://figma.com/))
+ gärna formulerat som *user stories*

##### Steg 2
Skapa ett projekt på Trello. Gör listor med namnen: **product backlog, in progress, ready for test, done**. Alla *krav* ska läggas till som kort i product backlog. Men gör om så många *krav* som möjligt till *user stories* först.

##### Steg 3
Jobba med ett Trello-kort i taget, genom att tilldela det till din användare och flytta till listan *in progress*. När du är klar med ett kort flyttar du det till *ready for test*.

I början av varje dag som ni arbetar med projektet, ska ni ha ett *standup/daily scrum* möte.

*Obs! Ta inte bort din användare från något kort du jobbat med. Läraren måste kunna se vad du har gjort.*

##### Steg 4
När du arbetar med ett kort ska du använda TDD. Börja med att skriva ett *rött* testfall. Skriv sedan minsta möjliga kod som uppfyller testet - *grönt* testfall. Sist refaktorerar du tills du är nöjd med koden.

##### Steg 5
Kontrollera att kort i *ready for test* uppfyller kravet från kravspec. Oftast låter man en annan gruppmedlem göra det här steget, annars är det högre risk att buggar slinker igenom. Om du bedömer att kravet är uppfyllt flyttar du kortet till *done*.

När alla kort är flyttade till *done* är ni klara!

##### Steg 6
Före eller efter presentationen av projektet ska ni ha ett *retrospective*, där ni diskuterar hur arbetet med projektet gick. 15-30 minuter. Gruppens anteckningar från mötet ska skrivas ner i projektrapporten. Ni ska svara på följande frågor:
1. Vad har ni lärt er av projektet?
3. Hur fördelade ni arbetet? (vem gjorde vad)
1. Fundera över vilka ändringar ni skulle göra om ni skulle fortsätta med projektet i samma grupp:
    + Vad skulle vi börja göra?
    + Vad skulle vi sluta göra?
    + Vad skulle vi fortsätta göra?
2. Vilka krav var svårast respektive lättast att skriva test för?
2. Fanns det något ni hade tänkt göra, som ni inte hann med? Vad berodde det på?

[Till toppen av sidan](#grupprojekt-webshop)

---
#### 2.2 Uppstart och versionshantering
Skapa ett projekt i en terminal. Kom ihåg att välja till testning.
```bash
npx vue create ert-projekt-namn
```

När ni utvecklar ska ni köra testfall i terminalen. (Tips: lägg på "watch" så körs testen igen varje gång du sparar en fil.)
```bash
npm run test:unit -- --watch
```

Ni ska ha en branch som heter `dev`. Varje person i projektet ska ha sin egen *branch* i git. Du ska regelbundet göra *merge* till `dev`. Minst två gånger under projektet ska gruppen dessutom göra *merge* från `dev` till `master`.

*Obs! Det är viktigt att alla gruppmedlemmar gör commit och merge, så att det syns på GitHub vad ni har gjort. Aktivitet på GitHub är en del av bedömningen.*

Se [appendix](#4-appendix-arbeta-med-git-i-terminalen) för exempel på hur man arbetar med git.

---
#### 2.3 Projektrapport
Förutom koden ska det finnas en textfil REPORT.txt i roten på ert git-repository. Den ska innehålla följande:
1. Vilka har arbetat i gruppen? (fullständigt namn och klass)
1. URL till ert repo på GitHub (se till att repot är *publikt* så att läraren kan se det)
3. URL till Trello (se till att läraren kan se er Trello board)
4. Kravspec (textfil eller länk)
5. Anteckningar från retrospective

Om ni behöver en e-postadress för att dela GitHub och Trello kan ni använda `david.andersson@zocom.se`.

---
#### 2.4 Presentation
Gruppen ska förbereda en kort presentation av ert projekt, som ni ska hålla för klassen med hjälp av Zoom. Planera presentationen till 15-20 minuter och räkna med att det kan komma frågor på slutet. Skriv gärna ner stödanteckningar på en post-it bredvid skärmen.
1. Demonstrera appen från en användares perspektiv (utgå från att åhörarna inte vet något om ert projekt)
1. Berätta om hur det fungerade att testa. Uppskatta hur mycket mer tid det tog att skriva tester än att börja koda direkt. Hade ni någon nytta av testerna senare i projektet?
1. Berätta om er största utmaning under projektet, och hur ni löste den
1. Berätta om begränsningar som ni gjorde för att hinna klart i tid
1. (optional) Visa skärmdumpar från tidiga versioner av appen
1. Var beredda på att det kan komma frågor från åhörarna
1. Ta emot applåderna!

[Till toppen av sidan](#grupprojekt-webshop)

---
### 3. Inlämning
Zippa koden för projekt *(men inte node_modules!!)* och ladda upp på LearnPoint. Glöm inte projektrapporten.


[Till toppen av sidan](#grupprojekt-webshop)

---
### 4. Bedömning
**För godkänt** på projektet ska du
+ delta aktivt i gruppens arbete
+ arbeta enligt instruktionerna på den här sidan; agilt, med git, TDD och Vue
+ arbeta med git (göra commits och merge)
+ arbeta med Trello (ta och jobba med kort)

**För väl godkänt** på projektet ska du dessutom
+ visa på god förmåga att ta initiativ, samverka och leda i grupp
+ kunna resonera och reflektera kring kursinnehållet

Det finns möjlighet att demonstrera det senare VG-kriteriet genom gruppens presentation, men det kommer även att testas i det individuella projektet.

---
### 5. Appendix: arbeta med git i terminalen
```bash
# Exempel på hur man arbetar med git
# Byt branch, så att du inte förstör master
git checkout name-of-your-branch

# När du gjort klart några testfall:
git status
git add --all   # lägga till alla ändringar i staging area
git commit -m "Informativt meddelande"  # spara ändringarna som en version i repot
git push  # skicka upp dina ändringar till GitHub, så dina gruppmedlemmar kan se koden

# När det är dags att använda koden i resten av projektet:
git checkout dev  # byt branch
git merge name-of-your-branch  # dra över dina ändringar till dev branch

# Skapa en version av appen som ni kan presentera för läraren
git checkout master
git merge dev

# Hämta kod direkt från klasskamrat:
git checkout klaras-branch  # din klasskamrats branch
git fetch  # hämta eventuella uppdateringar från GitHub
git status  # kontrollera om något nytt har hänt
git pull  # hämta det senaste från GitHub
git checkout nisses-branch  # din branch
git merge klaras-branch  # dra över Klaras ändringar till din branch
```

[Till toppen av sidan](#grupprojekt-webshop)
