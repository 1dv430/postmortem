# Tidsrapportering för Sommarkollo

**Innehållsförteckning**
 * [Abstrakt](#abstrakt)
 * [Inledning/Bakgrund](#inledningbakgrund)
 * [Demonstrationsvideo](#demonstrationsvideo)
 * [Vad har ändrats under projektets gång](#vad-har-%C3%A4ndrats-under-projektets-g%C3%A5ng)
 * [Vad gick bra](#vad-gick-bra)
 * [Vad gick dåligt](#vad-gick-d%C3%A5ligt)
 * [Vad blev inte som jag tänkt mig?](#vad-blev-inte-som-jag-t%C3%A4nkt-mig)
 * [Vad skulle jag göra annorlunda](#vad-skulle-jag-g%C3%B6ra-annorlunda)
 * [Vidareutveckling](#vidareutveckling)
 * [Sammanfattning](#sammanfattning)


### Abstrakt
Projektet är en appliktion skapad med HTML/CSS och JavaScript som exporteras med Phonegap till Android. Bakom appikationen finns en serversida med PHP och MySQL för att sköta beräkningar och lagring. 

Appens syfte är att anställda på sommarkollot skall kunna rapportera in sina arbetade timmar och att beräkning av OB-timmar skall ske på automatik. 

Administratören för systemet får rapporterna på sin mail, men kan även läsa dessa rapporter i PDF-format i ett webbgränssnitt, där administratören även kan administrera personalen.

De problem som har uppstått har varit svårigheter att planera tiden, skriva enhetstester och utvecklingsmiljön med Phonegap. Däremot har det uppstått flera positiva erfarenheter såsom att sätta upp en egen PHP-server, lyckan när applikationen fungerar och att de största riskerna försvann tidigt i projektet.


### Inledning/Bakgrund
Under de senaste 6 åren har jag arbetat som kolloledare på ett sommarkollo i Västerås under sommrarna. Vi är ungefär 11 kolloledare som jobbar under 3 perioder om 12 dagar och arbetet är ofta väldigt intensivt och innebär mycket nattjobb. Eftersom att vi arbetar "obekväma arbetstider" (OB) måste vi även lämna in en rapport i slutet på varje period med de timmar som kvalificerar extra lönekompensation. 

Denna rapport har tidigare skrivits för hand på papper och därmed har alla även gjort beräkningar själva på när man ska få "OB-timmar" osv. Många har tyckt att detta är delvis förvirrande, men även svårt att göra, då det fylls i sista kvällen på perioden när alla är stressade och har annat att göra på kollot. 

För att underlätta detta arbete och få de anställda att lägga tid på saker som gör att de känner sig mindre stressade valde jag därför att ta denna rapport och göra den elektronisk.

Anledningen till att det blev just en app som installeras i telefonen och inte en mobilanpassad websida är för att internetmottagningen på sommarkollot är väldigt dålig. Det går att gå in på hemsidor, men det tar tid. Därför är lösningen en applikation som låter användaren fylla i sin rapport i "lugn och ro", för att sedan skicka rapporten som med så lite data som möjligt (JSON-objekt) till servern som gör all uträkning och genererar en PDF. Denna PDF mailas sedan ut till den anställde och verksamhetsansvarige.

Utöver detta har även den verksamhetsansvarige en webbsida som kan visa alla inskickade rapporter och olika typer av sammanställningar (t.ex. alla rapporter som är inskickade på en period, eller alla rapporter för en anställd). 

Projektet har genomfört iterativt med 1 veckas iterationer. Avstämningsmöten har hållts med en projektgrupp (som dock inte är med som utvecklar i projektet, utan ses mer som ett stöd i applikationens utseende och projektets gång) efter varje vecka där man har berättat en sammanfattning av föregende iteration samt vad man planerar att göra i kommande iteration.

Projektets tidstgång har varit 240 timmar som satts utefter de kurser projektet ligger under och den tid de kurserna tillåter att jag har jobbat med projektet.

### Demonstrationsvideo
[Länk till YouTube](https://youtu.be/dSntWILh0bw "Demonstrationsvideo")

### Vad har ändrats under projektets gång?

#### Personalhanteringen 
Detta flyttades till den administrativa sidan som från början var tänkt att ligga i appen. Förändringen kom fram med feedback från projektgruppsmedlemmarna, vilket i slutändan var positivt. Det som var tråkigt med det var att det blev mindre funktionalitet att testa på i Phonegap-miljön. Posititvt med flytten var att det finns mycket mindre fel användaren kan göra och det går snabbt ovh enkelt att komma igång med sin rapport. Det utökar även möjligheterna för framtida utveckling.

#### Input-fält
Tidsvalen böts ut till Select-rutor från att ha varit input[type=number]. Detta gjorde felhanteringen lättare och det gör det enklare för användaren att första vad man ska välja. Nu slipper man ens fundera på vilket format tiden ska vara i, även om det gick bra med både "08" och "08:00" innan, så gör det saken lättare för användaren, vilket är det viktiga.

#### Sammanfattningssida
Innan man ska skriva på rapporten får man nu en enkel översikt på vad man har fyllt i, så att man kan upptäcka egna fel innan man signerar.

#### Driftsmiljön
Detta flyttades från One.com där projektet från början låg i en underkatalog till min pivata hemsida. Kunden önskade dock ett eget domännamn, och lösningen blev då att sätta upp en Apacheserver på en Rasperry Pi som låg i en flyttkartong. På det sättet blev det fortsatt gratis hosting för sidan vilket altid är positivt och det var en lärorik erfarenhet att sätta upp en egen server med databas och FTP-anslutning.

#### Autentisering
Då sidan ligger publikt och inte dolt i en underkatalog var det viktigt att få dit en simpel autentisering på sidan för att förhindra robotar från att ta sig in. Detta fungerade bra och har under projektets gång haft ett väldigt simpelt lösenord hårdkodat, vilket kommer ändras så fort projektet lanseras.

### Vad gick bra?
#### Risker avklarades tidigt
De största risker som fanns med projektet var helt enkelt att jag inte skulle kunna producera en app. Eftersom att jag såg den biten som oerhört spännande satte jag mig med det tidigt för att få ut en Hello World-applikation och ett proof-of-concept. Detta ledde till att det kändes som att jag hade ett försprång under projektet vilket gav mig mer motivation. 

Att göra det svåraste först är någonting jag gör "av gammal vana" och kommer garanterat att fortsätta med i fortsättningen. Det har mestadels att göra med att jag gillar de utmaningar som de större riskerna för med sig.

#### Efterforskningar
Jag lade ner en hel del tid på att ordentligt undersöka de bibliotek jag använder i backend-delen. Då jag redan kan utveckla i PHP såg jag det som en chans att sätta sig in i några av de större bibliotekens dokumentationer för att välja ut det som passar projektet bäst. Ett bra exempel på detta är mitt val av FPDF istället för MPDF (2st PHP-bibliotek för PDF-generering) där jag under min efterforskning kom fram till att MPDF är långsammare då det parsar HTML och CSS, medan FPDF(som jag till slut valde) är mer primitivt, men äver därtill snabbare. I implementeringen vet jag inte om det kommer att märkas någon större skillnad, men då ett av kraven är att appen skall använda så lite datatrafik som möjligt ser jag detta som ett mål att korta ner anslutningstiden till servern när mailutskicket sker.

### Vad gick dåligt?

#### Tidsplanering 
Att ha ett deltidsjobb och studera heltid fungerade väldigt bra i förra läsperioden. Anledningen till att detta inte har fungerar bra under projektet har varit att min chef har haft sämre framförhållning på när det behövs extra personal. Jag skyller inte på någon annan här, utan det är mitt fel att jag inte stått på mig och sagt att jag inte kan jobba för att jag har studier, utan har sagt ja till jobb när det erbjudits.

#### Debug-möjligheter
Under större delen av projektet fick jag sitta och lägga in en alert i javascript-koden, kompilera, skicka till emulator och hoppas att jag fick ut den information jag behövde. Oftast var det dock bara "Object [Object]" som dök upp. Efter många timmar på google lyckades jag hitta ett plugin som omnämnde urlen "chrome://inspect" för Chrome. 

Chrome har ett inbyggt stöd för att hitta WebViews i Android-emulatorer (för en del enheter, dock inte alla) och lyckligtvis fungerade detta på min emulator. Därefter hade jag en vanlig konsoll och kunde inspektera all trafik/console.

#### Testning
Att testa fungerande kod i efterhand är en väldigt tråkig syssla. Enhetstesterna har lidigt genom hela projektet. I framtiden skall jag försöka vara bättre på att skapa tester under tiden jag implementerar funktionalitet. Jag skall även under sommaren försöka att genomföra ett mindre projekt enligt Test Driven Development-metoden.

### Vad blev inte som jag tänkt mig?
#### Mailutskick
Jag har alltid trott att PHP har en egen SMTP-server inbyggt för att skicka ut mail. Jag vet inte om jag har missat någonting i min server-setup eller inte, men i slutändan använder jag mitt egna mailkonto på google för att skicka ut rapporten på mail genom deras öppna SMTP-kanal. Detta har tyvärr gett längre anslutningstid än vad jag velat. Och jag kommer ev. att titta på att skapa ett Chron-jobb som skickar ut nya rapporter varje timme istället för att det skall ske när appen står och väntar med sin anslutning på ett "OK" från servern.

#### Undvika att spara signaturer på disk
Nackdelen med att FPDF-biblioteket är lite simplare gör också att det är lite klurigare att importera en base64-encodad bild från databasen, utan jag blev tvungen att spara ner den på disk först. Detta ger ett extra steg i att ta bort rapport-information och då det är så få användare är inte utrymmet det tar i databasen ett problem. Jag kommer dock inte att göra några ändringar med detta, utan det fungerar utan några problem i dagsläget.

### Vad skulle jag göra annorlunda
1. Testa tidigare
2. Vara mer strukturerad i hur mycket tid jag kan lägga på varje iteration
3. Dokumentera bättre. Testdokumentationen och kravspecifikationen tog för lång tid innan det kom upp på wikin. Det hade underlättat att "hålla rätt kurs" i projektet om de hade varit mer utförliga.
4. Jag skulle undvika jQuery Mobile. Det gav en ok styling av appen från början och kändes då som ett bra val. Men att jobba med dynamisk data är jobbigt då man i så fall måste kalla på konstruktorn för jQuery Mobile för att den ska rendera elementen korrekt. Detta var en mardröm när jag vill ändra de elementen i CSSen, men det gick tillslut. Jag hade hellre gjort om det och skapat all CSS själv.

### Vidareutveckling
Det finns ett par riktningar det här systemet kan ta i sin vidareutveckling. Under sommaren kommer jag och en till utveckla ett CMS till verksamheten och appens administrativa sida skall integreras med CMSet. 

Någonting jag har planer på är att så småningom även flytta verksamhetens schemaläggning till CMSet och där kommer det då att öppna upp möjligheter för appen, t.ex. att man får ett färdigifyllt formulär med sina schemalagda tider. Har man inga avvikande tider blir det bara att skicka in.

Jag funderar även på att lägga in möjlighet till rapportering via en webbsida (utöver appen), då jag vet att det finns de som inte har Android-telefon, och som det är idag kommer vi att låna ut våra telefoner till iPhone-användarna.

### Sammanfattning
Slutprodukten stämmer bra in på visionen och jag känner mig väldigt nöjd med resultatet. Det är extra kul när man vet att applikationen kommer att användas skarpt, och även om jag har buggtestat den så har jag ingen möjlighet att åtgärda problem när vi väl ska använda den då jag både saknar min utvecklingsmiljö och bra internetuppkoppling. Jag känner mig dock väldigt säker på produkten och hoppas att alla blir nöjda med den!
