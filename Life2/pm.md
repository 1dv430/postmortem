## Life²
av Sofia Kristiansen, 2017-05-30.

### Abstrakt
Följande rapport berör utvecklingen av applikationen Life², ett projekt som pågått under 10 veckor och är en del av Linnéuniversitetets kurs 1DV430 Individuellt mjukvaruutvecklingsprojekt.

Rapporten beskriver kort Life² och vad det är för applikation. Projektets syfte och arbetssätt, samt vilka tekniker som använts i utvecklingen av applikationen. Författaren beskriver därefter sina positiva och negativa erfarenheter från projektet, där tidig testning framhålls som en positiv erfarenhet och avsaknade prototyper framhålls som en negativ erfarenhet. Rapporten avslutas med en sammanfattning av hur det varit att arbeta med projektet, samt utvecklingspotentialen hos applikationen.

### Inledning och bakgrund
Life² är en responsiv webbapplikation där användare kan:
* Skapa bucketlists och lifelist.
* Lägga till mål på sina listor.
* Sätta deadline för när målen ska vara uppfyllda.
* Checka av mål på sina listor.
* Följa sina framsteg i uppfyllandet av de uppsatta målen.
* Ladda upp och publicera bilder och text.
* Se tillbaka på uppfyllda mål i form av bild och text.
* Chatta med andra användare.
* Få inspiration till nästa mål att uppnå.

Kort sammanfattat: Self-composed lists of personal goals with self-imposed deadlines.

**Syfte/mål**  
Syftet med projektet var att leverera en individuellt utvecklad produkt som har testats och satts i produktion, samtidigt som man får erfarenhet av att arbeta med projekt och all dokumentation som hör till. Detta för att få kunskap i hur projekt bedrivs ute i arbetslivet och samtidigt få en chans att förkovra sig i de tekniker man valt att arbeta med.

Det övergripande målet med slutprodukten var ett digitalt verktyg för att skapa och samla bucketlists och lifelist på ett och samma ställe, där användare själv kunde sätta en deadline för när och hur just deras liv ska levas.

**Arbetssätt**  
Projektet har genomförts individuellt på distans på halvfart under 10 veckor. Under projektet har arbetsprocessen [Unified Process](https://en.wikipedia.org/wiki/Unified_Process) använts, vilket är en iterativ och inkrementell process där veckorna delas in i fyra olika faser: Inception, Elaboration, Construction och Transition. Beroende på vilken av faserna man befinner sig i ska olika delar av projektet arbetas/fokuseras på. Läs mer på Wikipedia: [Unified Process](https://en.wikipedia.org/wiki/Unified_Process). 

Som arbetsmetod för projektet har [SCRUM](https://en.wikipedia.org/wiki/Scrum_(software_development)) använts, en iterativ och inkrementell metod. Varje vecka har en ny sprint backlog skrivits, som innehåller en analys av föregående iteration, tidsrapport för föregående iteration och en tidsplanering för veckan. Veckan har sedan inletts med ett handledarmöte gruppvis, där varje deltagare i gruppen fått cirka fem minuter på sig att presentera föregående veckas arbete, vad som är planerat för veckan och ta upp de problem eller frågor de har. Dessa möten har genomförts över Google Hangouts.

Allt material som hör till projektet har versionshanterats på GitHub och går att hitta här: [Home](https://github.com/1dv430/sk222uf-project/wiki).

**Genomförande/teknik**  
Författaren har använt sig av följande tekniker i implementationen:  
* Atom, IDE.
* JavaScript, client-side scripting.
* HTML5, struktur.
* CSS, styling.
* npm, package manager. Nedladdning av bibliotek som används i programmeringen.
* Node.js, server-side scripting.
* Express.js, webbapplikations ramverk.
* Socket.io, för real-time uppdatering av applikationen.
* MongoDB och Mongoose, databas.
* Digital Ocean Droplets Ubuntu MongoDB 3.2.7 on 14.04, för att sätta applikationen i produktion. Gör applikationen tillgängling på www.
* Nginx, reverse proxy.
* PM2, process manager.
* Adobe Photoshop, grafik.

För testning har följande tekniker använts:  
* Mocha, testramverk.
* Chai, assertion library.
* Istanbul, code coverage.  
För mer info om hur testning genomförts: [Testspecifikation](Testspecifikation)

### Positiva erfarenheter
Jag är glad över att jag påbörjade testning av min applikation så tidigt som jag gjorde, då det visade sig ta mycket längre tid att skriva automatiserade tester och genomföra manuella tester på flera olika enheter än vad jag först hade tänkt. Utan testerna hade jag inte hittat alla de fel och buggar som min applikation faktiskt hade och kunnat åtgärda dem för att få ett system som känns mycket stabilare ju fler tester som har körts. Testning är definitivt något jag kommer påbörja tidigt i mina kommande projekt också, för att ha en stabil grund att fortsätta bygga på och för att ha tid att rätta till och fixa buggar för att få ett stabilt system.

Jag är också nöjd med min planering och prioritering i projektet. Den gjorde att jag tidigt blev klar med implementationen av de mest högprioriterade kraven och därför hann lägga ner mer tid på att implementera de lägre prioriterade kraven. Jag hann implementera alla krav som jag skrivit upp i min product backlog plus lite extra funktionalitet. Detta tror jag har att göra med att jag tidigt i projektet var klar över vad som var viktigast att ha med i applikationen, vilket gjorde det lätt att skriva planering för kommande iterationer utifrån vad som redan var färdigt och vad som stod näst på tur. Att göra en prioritering och inte avvika från den är något jag tar med mig till kommande projekt.

### Negativa erfarenheter
En av mina negativa erfarenheter var att jag inte lade ner tid på att ta fram prototyper innan jag började med implementationen. Som exempel har mycket av designen arbetats fram spontant med test hit och dit i CSS-koden för att se vad som blir snyggast, istället för att jag bara hade kunnat rita upp olika designalternativ och sedan implementerat det som jag i slutändan väljer. Det hade varit bra att istället för att hålla alla alternativ i huvudet ha dem konkret på papper och ha ett mål att arbeta mot.

En annan negativ erfarenhet är att jag inte började använda mig av [caniuse.com](http://www.caniuse.com) tidigare i utvecklingen av min applikation. Det hade exempelvis sparat mig mycket tid när jag sökte efter en lösning på att få chatten att fungera i webbläsarna Edge och IE och att få felmeddelanden att dyka upp i äldre versioner av iOS. CanIUse hade direkt sagt till mig att nej, du kan inte använda template-taggarna på det viset som du gör om du ska ha stöd för chatten i Edge och IE eller att Safari iOS 10.3 är den första iOS versionen som stödjer formulärs felmeddelanden.

Sen är jag inte helt nöjd med att inte ha kunnat åtgärda samtliga kända buggar. Anledningen till det är främst att jag inte vetat hur jag ska gå tillväga för att lösa vissa av dem och tyvärr fokuserat på de som verkar svårast att lösa, men som inte påverkar fler än en liten andel av de tänkta användarna. Det hade exempelvis varit bra med mer tid för att läsa på om hur man implementerar splashscreen och ikoner på iOS enheter när applikationen går över HTTPS, trots att jag redan lagt uppemot 4-5 timmar bara på att försöka lösa just det specifika problemet. Den tiden hade kunnat läggas på att fixa någon av de andra buggarna som påverkar fler av de tänkta användarna, men här brast jag i prioriteringen. En lista eller ett dokument över kända buggar med prioritering hade varit bra för att kunna åtgärda de mesta akuta buggarna.

### Sammanfattning
Slutprodukten blev som jag hade tänkt mig plus lite till. All tänkt funktionalitet finns där och jag är nöjd med hur applikationen ser ut både på desktop och mobil. Att det finns en del kända buggar som inte är åtgärdade påverkar inte slutresultatet i någon större mån, men är något jag hade hoppats kunna rätta till för att få det exakt så som jag hade tänkt mig.

Under projektets gång har jag fått större förståelse för det iterativa arbetssättet och hur det kan göra det lättare att dela upp ett stort projekt i mindre, mer hanterliga bitar. Att varje vecka också få prata av sig med en grupp och berätta hur arbetet går har varit positivt och även gjort det lättare att bibehålla disciplinen. Utan mötena hade det kanske blivit så att man hade latat sig de första veckorna, för att sedan stressa ihjäl sig de sista veckorna.

Att välja att arbeta med de tekniker som tidigare tagits upp under läsåret har gjort att jag kunnat fördjupa mina kunskaper och även få repetition i sådant som jag nästan hunnit glömma bort.

Min applikation har absolut utvecklingspotential. Ett exempel på ytterligare funktionalitet att implementera skulle kunna vara att användare kan besöka varandras bucketlists och lifelist för att få inspiration eller hitta någon att genomföra sina gemensamma mål med. Att ha flera chattrum beroende på vad det är man vill diskutera. Kunna lägga till en personlig presentation av sig själv på sin användarsida och en profilbild. Man kan helt enkelt, om man vill, utveckla Life² till att bli ett av de kommande sociala medierna.

Jag är nöjd med min insats i kursen och med min applikation.
