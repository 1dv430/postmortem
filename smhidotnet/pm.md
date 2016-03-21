#SMHIdotNET
## Slutrapport   
   
###Abstrakt
SMHIdotNET är en API wrapper av SMHI’s väderdata, för användning i Microsoft .NET-miljö.  SMHI levererar prognoser och observationer genom arkitekturen REST. Genom att samla funktionalitet i en API wrapper, kan väderdata hämtas med enkla metodanrop. Användaren av API’et behöver inte känna till tekniken bakom, och det reducerar mängden kod. Detta förenklar och effektiviserar programmeringen. API’et är skrivet i C# och utvecklingen har skett genom Test Driven Development (TDD).    
Projektet innefattar även en enklare webbplats som har utvecklats för att demonstrera användningen av API’et. Webbplatsen är utvecklad i Asp.net Webforms (C#) och JavaScript.    
I rapporten kommer jag beskriva syfte/mål med projektet, hur arbetssättet har bedrivits, tekniker som har använts, samt mina positiva respektive negativa erfarenheter.   
   
###Inledning och bakgrund   
####Syfte/mål   
Syftet med projektet var att skapa ett klassbibliotek i Microsoft .NET som hämtar väderdata från SMHI. Målet har varit att produkten ska vara enkel att använda, samt vara dokumenterad så att produkten blir användbar. Det akademiska syftet var att lära mig mer avancerad utveckling i C#, samt bli introducerad till tekniker som REST, TDD, json etc.   
   
####Arbetssätt   
Projektet har bedrivits som distansstudier på halvfart under 10 veckor. Arbetsmetoden som har använts var en Unified Process-liknande ([Wikipedia, Unified Process](http://en.wikipedia.org/wiki/Unified_Process)) och för projektledning/styrning har SCRUM använts ([Wikipedia, Scrum](http://en.wikipedia.org/wiki/Scrum_(software_development))). Det har inneburit veckolånga iterationer, med ett gruppmöte per vecka. Mötesformen har varit videokonferens över Skype. Gruppen bestod av 5 studenter och en lärare.  Inför varje iteration presenterades föregående veckas arbete, samt planeringen inför nästkommande iteration. Allt material i projektet har versionshanterats på Github.com. Projektet avslutades med en projektredovisning.  
   
####Genomförande/teknik   
Programmeringsspråket som har använts var C#. SMHI använder REST ([Wikipedia, Representational state transfer](http://en.wikipedia.org/wiki/Representational_state_transfer)) och data levereras i json-format. Utvecklingen av produkten har skett genom Test Driven Development (TDD) ([Wikipedia, Test-driven development](http://en.wikipedia.org/wiki/Test-driven_development)). Istället för användning mock-ramverk har all testning skett mot egenskrivna mocker. 
Demonstationswebbplatsen är utvecklad i Asp.net Webforms. I ett par av exemplen har JavaScript använts där ett ajax-anrop till servern hämtar väderdata asynkront.  
   
####Positiva erfarenheter   
Projektet har löpt på bra. Jag har under hela projektet levererat på utsatt deadline, och detta har hjälpt mig att hela tiden ligga i fas. Det har bidragit till minskad stress.   
Jag la ner extra mycket tid i början för att vara säker på att hinna klart. Jag började med att sätta mig in i de olika teknikerna. Eftersom TDD var ett nytt arbetssätt för mig behövde jag sätt mig in i det tankesättet. Jag tittade på flera instruktionsvideos, och läste många tutorials på nätet. Jag har kört tester kontinuerligt, och har varit trygg med att allt har fungerat, även när jag gjort förändringar i existerande kod. Jag tycker att TDD är ett bra arbetssätt, och kommer i utvalda projekt att fortsätta med detta.     
För att kunna utföra enhetstester där koden haft minimalt beroende, insåg jag tidigt att jag behövde lära mig interface, inversion of control, och dependency injection. Det har lett till att jag har blivit bättre på att generalisera metoder och klasser.   
Många mock-ramverk använder LINQ och jag har lagt ner tid på att lära mig grunderna i LINQ och Lambda. Även om jag bara har fått grundläggande kunskaper, kommer jag att ha stor nytta av detta i framtida programmering i C#.   
   
####Negativa erfarenheter   
De första veckorna kändes det som att projektet stod stilla, eftersom den största tiden gick åt till att lära sig nya tekniker. I efterhand ser jag att detta var bra, men i rådande stund var detta ett stressmoment. Jag försökte sätt mig in i hur mock-ramverk fungerar, men gav upp eftersom jag inte kunde hitta någon tutorial som gick igenom det som jag behövde veta (ex. hur man mockar en http-respons). Istället skrev jag egna mockar och detta är tagit mycket tid, som skulle kunna ha lagts på bättre saker.   
Jag har varit dålig på att tidsskatta. Jag har i många fall skattat för lågt, vilket har inneburit ganska många fler timmar än planerat.    
Jag tycker att kursen kunde ha haft fler (frivilliga) föreläsningar, kanske finns det ett par gemensamma områden som flera studenter kunde ha nytta av i sina projekt. Det har varit väldigt mycket ensamarbete och ibland behöver man en knuff i rätt riktning för att polletten ska trilla ner. I mitt eget projekt skulle jag önskat föreläsning i TDD, IoC, hur man använder mock-ramverk och Github.    

####Sammanfattning    
Jag har övervägande positiva erfarenheter av projektet. Det har varit mycket lärorikt, både vad det gäller projektformen, och programmeringen. Jag tycker själv att jag blivit mycket bättre programmerare i C# och kommer att ha med mig denna kunskap i nästkommande kurser. Jag har jobbat efter TDD, men är långt ifrån fullärd. Min önskan är att få fortsätta lära mig detta, så att TDD blir en naturlig del av mitt sätt att programmera.   
    
 

 

 
 


