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

+ 4-5 personer
+ avstämning med läraren varje lektionsdag
+ arbeta agilt, med scrum och TDD
+ Trello, GitHub, Vue

Inom gruppen ska ni göra en avgränsning av uppgiften. Bestäm er för vilka sidor eller vyer (views) som ska finnas och implementera dem. Ni måste också välja vilka komponenter ni prioriterar att testa.

*Exempel: de flesta webbshoppar låter användaren se flera produkter på samma gång, söka/filtrera produkter, se detaljer om en produkt, lägga till i kundvagn, se/ändra innehållet i kundvagnen, se hur mycket allt kostar.*

---
#### 2.1 Agil utveckling, kravspec och scrum
##### Steg 1 - i början
Skapa ett projekt på GitHub, i organisationen https://github.com/Jensen-frontend-fwk19g/

Skapa ett projekt på Trello. Gör listor med namnen: **product backlog, in progress, ready for test, done**. Lägg till alla *user stories* som kort i *product backlog*.

Börja på en projektrapport `REPORT.md` som ska ligga i repot:
+ era namn och Discord-alias
+ berätta kort vad webbshoppen handlar om och vilka features som ingår
+ user stories (minst 8 stycken, skrivna från användarnas perspektiv)
+ länk till Trello (se till att projektet är publikt)
+ länk till GitHub-repot

##### Steg 2.1 - varje dag
Jobba med ett Trello-kort i taget, genom att tilldela det till din användare och flytta till listan *in progress*. När du är klar med ett kort flyttar du det till *ready for test*.

I början av varje dag som ni arbetar med projektet, ska ni ha ett *standup/daily scrum* möte.

*Obs! Ta inte bort din användare från något kort du jobbat med. Läraren måste kunna se vad du har gjort.*

##### Steg 2.2
När du arbetar med ett kort **ska du använda TDD** - red, green, refactor. När kortet är färdigt ska du flytta det till *ready for test*.

##### Steg 2.3
En gruppmedlem som *inte* har implementerat en user story (test + kod) som ligger i **ready for test** ska kontrollera om lösningen uppfyller kravet. Om lösningen är godkänd flyttar man kortet till *done*. Annars får personen som jobbade med kortet göra om.

När alla kort är flyttade till *done* är ni klara!

##### Steg 2.4
Gruppen ska boka in avstämning med läraren varje lektionsdag.


[Till toppen av sidan](#grupprojekt-webshop)

---
#### 2.2 Uppstart och versionshantering
Skapa ett projekt i en terminal. Kom ihåg att välja till testning.
```bash
npx vue create ert-projekt-namn
```

När ni utvecklar ska ni köra testfall i terminalen. (Tips: lägg på "watch" så körs testen igen varje gång du sparar en fil. Antingen i package.json eller direkt i terminalen)
```bash
npm run test:unit -- --watch
```

Ni ska ha en branch som heter `dev`. Varje person i projektet ska ha sin egen *branch* i git. Du ska regelbundet göra *merge* till `dev`. Minst två gånger under projektet ska gruppen dessutom göra *merge* från `dev` till `master`.

*Obs! Det är viktigt att alla gruppmedlemmar gör commit och merge, så att det syns på GitHub vad ni har gjort.*

Se [appendix](#4-appendix-arbeta-med-git-i-terminalen) för exempel på hur man arbetar med git. Se även presentationer från början av kursen.



---
### 3. Inlämning
Zippa koden för projektet *(men inte node_modules!!)* och ladda upp på LearnPoint. Alla projektmedlemmar måste göra detta - det räcker inte med att en gör det.


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


---
### 5. Appendix: arbeta med git i terminalen
Detta är en kortare sammanfattning. Se även materialet från början av kursen.
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
