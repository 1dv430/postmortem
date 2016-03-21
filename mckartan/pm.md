
### 2015-05-27

---
### Abstrakt

Rapporten handlar om kursen 1DV430 - Individuellt mjukvaruutvecklingsprojekt, som jag läst på webbprogrammerar-programmet, [Linnéuniversitetet][lnu] i Kalmar och mc-kartan.se den webbapplikation som jag utvecklat under kursens tio veckor.

Rapporten tar även upp de intryck och erfarenheter jag skaffat mig genom att gå in i ett projekt med en mängd nya metoder och tekniker samt hur ett [testdrivet][tdd] och [agilt][agile] arbetssätt gjort att mitt  förtroende för applikation ökat och underlättat möjligheten till att backa mindre lyckade beslut genom [omstrukturering][refactor].


### Inledning och bakgrund

#### Bakgrund

Syftet med mc-kartan.se är att med moderna webbtekniker skapa en karta som enkelt presenterar användarnas favoritvägsträckor. Allt för att förenkla planerandet av resor, öka möjligheten att hitta de finaste mc-vägarna i en region. Samtidigt ville jag lära mig mer om [Ruby on Rails], [testdriven utveckling][tdd], [beteendedriven utveckling][bdd] och en mängd andra saker. Denna önskan innebar dock att jag fick skala av min applikations funktionalitet för att kunna hinna med.

#### Arbetssätt

Arbetet har skett med hjälp av, för [Linnéuniversitetet][lnu], skräddarsydda varianter av [Unified Process] och [Scrum] där vi i början av var vecka dels levererade föregående veckas arbete, planerade nästkommande veckas arbete och dels fick handledning.

#### Teknik

Jag har i litteratur och tidigare i utbildningen stött på en mängd tekniker och begrepp som jag tidigt insåg att jag ville testa på i projektet. De tekniker jag ville kolla närmare på var:

* [Ruby on Rails]
* [Haml]
* [Testdriven utveckling][tdd]
* [Beteendedriven utveckling][bdd]
* [Continous integration][ci]


### Positiva erfarenheter

Erfarenheterna med arbetssättet och den variant av [Scrum] som vi använt oss av känns väldigt positiva och har gjort det betydligt enklare att utföra uppgifterna då jag tvingats till att bryta ner de problem jag vill lösa och på så sätt fått lätthanterliga och tydliga mål. Något som hindrat mig från att uppleva arbetsuppgifterna som enorma och oöverkomliga. Tror att arbetsättet är en stor anledning till varför jag kan sitta här nu och känna mig nöjd över de tio veckor som gått.

Bilden kring applikationen har hela tiden varit tydlig. Mycket tack vare den dokumentation som skapats kring projektet. Dokumentation som känns relevant och som en tillgång. Speciellt efter att kollat närmare på [Cucumber] och [Rspec] som på ett enklare sätt knyter samman dokumentationen med själva testen och minskar den information som lever på flera ställen.

Att mycket av min kod har haft test har gjort arbetet med [omstrukturering][refactor] väldigt mycket enklare och det förtroende som detta har inneburit har möjliggjort att koden har blivit lättare att följa och ta till sig. 

Upplever att jag breddat mina kunskaper väsentligt på många olika punkter. Främst har jag befäst min vilja att jobba testdrivet. Något som ökat mitt självförtroende och förhoppningsvis även kvaliteten på min programmering. Genom att fortsätta att arbeta med dessa, ovan nämnda, verktyg tror jag även framtida projekt kommer att bli positiva erfarenheter.


### Negativa erfarenheter

Tyvärr har jag, när timmarna börjat rulla på, övergett mitt testdrivna arbetssätt och helt enkelt utvecklat först för att sedan gå tillbaka och skriva testen på efterhand. I detta fall är min otålighet och bristen på kunskap det stora problemet. Något jag kan undvika i framtiden genom att acceptera att jag inte kommer att producera något direkt användbart de första iterationerna av ett projekt. Men framför allt genom att öka min kunskap om de verktyg, metoder och ramverk jag använder mig av.

Har även testat på lite för mycket olika tekniker, främst på testningssidan. Men de erfarenheter jag skaffat mig under detta projekt gör att jag står bättre rustad för nästa [Ruby on Rails] projekt då jag har en mängd verktyg jag provat på och nu börjar känna mig mer bekväm med. Även insikten att det inte går att göra och testa allt samtidigt gör att jag kommer ha det lättare att göra en mer informerad avvägning kring vilka tekniker som medför faktiskt värde och vilka vars "return of interest" är lågt.

Dokumentationen kring testen har ofta hamnat i baksätet och jag har inte riktigt upplevt att det funnits någon direkt kopplingen mellan den dokumentation som jag tagit fram och de faktiska test som körs. Jobbet att hålla dokumentationen uppdaterad har varit ett konstant problem och vid större projekt måste det vara en stor utmaning. Tror det för mig är viktigt att tidigt försöka utnyttja t.ex [Cucumber] och [Rspec] liknande arbetssätt där dokumentation och test flätas samman och där samma information lever endast på ett eller ett fåtal ställen.

Att skriva test efter att ha implementerat funktionaliteten gjorde mina test sämre och jag programmerade funktionalitet som jag egentligen inte behövde vilket i sin tur ledde till en större kodbas som egentligen inte tillförde något. Upplever det som att jag genom att hålla projektet [testdrivet][tdd] skulle få en mycket bättre kontroll och kod som gör rätt sak om jag faktiskt testar och tänker igenom vad det är jag vill åstadkomma innan jag börjar programmerar utforskande.

Har saknat test på min klientsidan något som genom hela projektet oroat och även ställt till det för mig då ändringar i serversidan medfört att kopplingar i min klientsida blivit fel. Tror det är viktigt att tidigt ta sig tid och implementera testning för även klientsidan.

Känner att projektets avslut kom lite tvärt och jag bör nog skaffa mig en bättre överblick över framtida projekt och dess helhetsplanering.


#### Sammanfattning

Projektet har flutit på bra och jag ligger väldigt nära min ursprungliga vision. 

Känner att applikationen blev något tunn och att jag gärna utvecklat denna betydligt mer. Men under projektet testade jag även på en stor mängd nya tekniker och arbetssätt. Detta har gett mig många nyttiga erfarenheter och jag känner mig betydligt bättre rustad att utveckla en applikation idag än vad jag gjorde innan projektet. Potentialen längre ner på den stig som jag har börjat att vandra med TDD/BDD känns väldigt lovande.

Har under projektets gång identifierat en mängd metoder och tekniker som gör att mitt förtroende för och den överlag upplevda kvaliteten kring applikationen ökar. Något som jag tar med mig till mina framtida projekt.

Tycker mc-kartan.se har en ganska bra grund och med möjlighet för användare att skapa konton och lägga upp sina egna favoritsträckor tror jag att mc-kartan.se skulle kunna fylla ett verkligt behov som finns bland motorcyklister.


[agile]: http://sv.wikipedia.org/wiki/Agil_systemutveckling
[bdd]: http://en.wikipedia.org/wiki/Behavior-driven_development
[ci]: http://en.wikipedia.org/wiki/Continuous_integration
[Cucumber]: http://www.cucumber.io
[haml]: http://www.haml.com
[lnu]: http://www.lnu.se
[tdd]: http://sv.wikipedia.org/wiki/Testdriven_utveckling
[refactor]: http://en.wikipedia.org/wiki/Code_refactoring
[Rspec]: http://www.rspec.info
[Ruby on Rails]: http://www.rubyonrails.com 
[Scrum]: http://sv.wikipedia.org/wiki/Scrum
[Unified Process]: http://en.wikipedia.org/wiki/Unified_Process