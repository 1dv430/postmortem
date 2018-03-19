#### Titel, Författare och datum
Kult - Upptäck din omgivning
Olle Lauri Boström   
7/6 - 17

#### Abstrakt 
Denna rapport avhandlar utvecklingen av en mobilapplikation för iOS/Android under kursen Individuellt mjukvaruutvecklingsprojekt på Linnéuniversitetet. Mobilapplikationen heter Kult och erbjuder ett lättillgängligt sätt att upptäcka sin omgivnings historia och kultur. I appen kan intresserade lära sig mer om historiska byggnader och offentlig konst i sin närhet. Projektet är helt JavaScriptbaserat, och mobilappen är baserad på ramverket React Native. I rapporten konstaterar jag att React Native är ett trevligt ramverk att jobba med. Som webbutvecklare, utan någon erfarenhet av ett "native-språk" (Java/Swift) så är det ett lättillgängligt sätt att komma igång med utveckling av mobilapplikationer. Speciellt om man har lite erfarenhet av React som ramverk sedan tidigare.

#### Inledning och bakgrund

##### Mål
Projektets mål var att utveckla en mobilapp där användarna på ett enkelt sätt skulle kunna upptäcka intressanta platser i sin omgivning. Utifrån användarens position skulle en lista/karta med platser presenteras, bestående av allt från historiska byggnader till offentlig konst. Målet var att förädla öppen data från ett par APIn, och på så sätt göra vår gemensamma historia och kultur lättillgänglig och rolig att upptäcka. För att sticka ut från liknande appar och göra upplevelsen i appen roligare var tanken att erbjuda ett modernt och användbart användargränssnitt.

##### Teknik
Projektet är helt JavaScript-baserat, och React fungerar som ramverk både för mobilappen och den webbplats som har skapats. React är ursprungligen ett front-end ramverk för webbapplikationer utvecklat av Facebook. React Native tar React-platformen till mobila enheter och gör det möjligt att med hjälp av JavaScript skapa mobilapplikationer som kan köras på både iOS och Android.

Projektets bakomliggande API drivs av en express-applikation som både servar APIt och den React applikation/webbplats som presenterar mobilappen. Denna expressapplikation är publicerad på molntjänsten Heroku. 

Mobilappen är som ovan nämnt utvecklad med hjälp av React Native. Jag har använt mig av npm-paketet Create React Native App (CRNA) för att snabbt komma igång med en fungerande utvecklingsmiljö. Appen är inte publicerad på någon ”app-butik” eftersom att det kostar en del, utan istället publicerad via expo (instruktioner för hur man kan ladda hem expo och köra appen finns på WIKINs startsida).

All kod är skriven enligt ES6/ES7 syntax och jag har försökt att i största möjliga mån följa gällande konventioner i React-communityt genom att exempelvis använt mig av saker som ”Stateless functional components”, ”Proptypes” och ”ES7 property initializers”. Kodkvalitets-verktyget ESLint har använts med Airbnbs JavaScript-stilguide för att hålla ett konsekvent utseende på koden. Jest, Chai och Enyzme används som ramverk för enhetstester.

Här hittar du ett par källor där du kan läsa mer om några av de tekniker och uttryck som nämns ovan:
- [React Native](https://facebook.github.io/react-native/)
- [CRNA](https://github.com/react-community/create-react-native-app)
- [React on ES6+](https://babeljs.io/blog/2015/06/07/react-on-es6-plus)
- [Stateless functional components](https://hackernoon.com/react-stateless-functional-components-nine-wins-you-might-have-overlooked-997b0d933dbc)
- [ESLint](http://eslint.org/)
- [Jest](https://facebook.github.io/jest/)
- [Air bnb JavaScript styleguide](https://github.com/airbnb/javascript)
- [Heroku](https://heroku.com)
- [Expo](https://expo.io)

##### Arbetssätt
I början av projektet skapades ett visionsdokument där bilden av hur slutprodukten skulle se ut definierades. Dessutom upprättades en ”product”-backlog i form av en lista med krav bestående av user stories och tasks. Projektet har sedan genomförts i iterationer (1 vecka). Varje vecka har planerats i detalj och arbetsuppgifter har definierats utifrån de krav som funnits i projektets ”product backlog”. Varje iteration har avslutats med ett handledningsmöte där resultatet av iterationen har presenterats samt i form av en tidrapport och skriftlig utvärdering. 

#### Positiva erfarenheter

Redan tidigt i projektet hade jag en tydlig bild av hur min applikation skulle fungera, vilka tekniker som skulle kunna bli användbara och på ett ungefär hur olika moduler skulle kunna hänga ihop. Detta visualiserades i ett visions-dokument och med hjälp av UML-diagram. Jag fick dessutom snabbt igång en fungerande utvecklingsmiljö genom att använda npm-paketet CRNA (Create React Native App). Att jag tidigt i projektet skapade en tydlig bild av hur jag ville att slutresultatet skulle se ut, och satsade på att skapa UML-diagram och fundera kring hur de olika delarna i mitt projekt (Mobilapp, API och Webb) skulle hänga ihop tror jag varit en viktig del i att lyckas få till ett gott slutresultat. Detta är en positiv erfarenhet som jag definitivt kommer att ta med mig in i kommande projekt. Det är inte bara viktigt att planera och modellera sin applikation, utan det kan dessutom vara riktigt roligt. I början av projektet köpte jag mig faktiskt en liten whiteboard som blivit välanvänd under projektets lopp! 

Det iterativa arbetssättet har fungerat mycket bra och lett till att det blivit tydligt vilka uppgifter som stått på agendan för veckan. Just att lära sig planera sin tid, och sätta pränt på arbetsuppgifter som bör slutföras under en vecka tror jag är en nyttig erfarenhet. Att resultatet av varje iteration sedan har presenterats på handledarmötena på måndagarna har för lett till att jag jobbat lite extra hårt för att leverera ungefär som planerat.

Efter avslutat projekt känner jag mig faktiskt på många sätt riktigt nöjd med min slutprodukt. Den största positiva erfarenheten som jag tar med mig är React och React Native som ramverk. Jag har testat på React lite smått under en tidigare kurs, men känner att jag under detta projekt har kunnat bygga vidare på mina kunskaper och lärt mig mycket mer om gällande konventioner inom React-communityt. Även om ramverket fortfarande är ”ungt” och på vissa områden har sina begränsningar så måste jag säga att det är ett smidigt sätt för webbutvecklare dra nytta av sina kunskaper om JavaScript för att kunna utveckla mobilapplikationer. 

Jag har tidigare skapat en mobilapplikation i Cordova (också med hjälp av JavaScript). Då var jag absolut inte nöjd med slutresultatet, som egentligen mest kändes som en webbplats i app-format utan någon slags ”native-känsla” över huvud taget. React Native framstår som ett mycket bättre alternativ, och en värdig motståndare till en app utvecklad i Java/Swift. 


#### Negativa erfarenheter
Under projektets lopp har jag under vissa iterationer kanske fokuserat lite för mycket på små detaljer i applikationen, exempelvis att fixa någon liten bugg. Det känns inte som ett speciellt effektivt förhållningssätt att lägga ner flera timmar på att lösa någon liten bugg i en applikation, utan i vissa fall hade det kanske varit smartare att helt enkelt dokumentera buggen och fortsätta med andra planerade uppgifter. 

Delar av källkoden, framförallt för mobilalpen har skrivits om flera gånger. Exempelvis så har navigationen omarbetats flera gånger och de flesta komponenter har skrivits om från klasskomponenter till ”Stateless functional components”. Detta är i sig inget negativt eftersom att det i slutändan resulterat i en modern kod som följer gällande ”best practices” samt att jag har lärt mig massor. Däremot kan jag reflektera över detta så här i efterhand och tänka att arbetet i projektet stundvis varit ”oeffektivt”, vilket ute i arbetslivet troligtvis varit problematiskt. Hade det funnits en riktig kund med i bilden hade det kanske inte fungerat att lägga ner massor med tid på att skriva om kod som redan fungerar.

Tanken var att projektet skulle implementera en testdrivan utvecklingsmetodik. Detta fungerade bra för utvecklingen av APIt, mest troligt eftersom att jag sedan tidigare har rätt så bra koll på hur ett express-api är uppbyggt. Under utvecklingen av webb och mobilapplikationen har denna metodik inte fungerat/implementerats eftersom att det blivit svårt att skriva tester innan den faktiska koden på grund av att jag ofta varit osäker på exakt hur en viss komponent skulle implementeras. Istället har ett mer explorativt förhållningssätt använts, där jag helt enkelt testat mig fram, och sedan kompletterat med enhetstester i efterhand. 


#### Sammanfattning

Först och främst vill jag säga att denna kurs har varit otroligt lärorik och rolig. Kursen blir såklart mycket till vad en själv gör den till men det har känts skönt att ha fått möjlighet att stanna upp ett tag och faktiskt fundera på vad vi har lärt oss hittills under utbildningen. Att använda React Native för att skapa mobilapplikationer har varit otroligt roligt och jag har fått massor av idéer på andra applikationer som jag vill utveckla framöver.

Även om jag är nöjd med slutresultatet om man ser till kvalitén på den kod jag har skrivit så skulle applikationen nog inte bli en super-succé om det släpptes i app-butikerna. Däremot ser jag absolut att jag skulle kunna ha med appen på ett CV och därför kommer jag troligtvis att fortsätta jobba vidare med den och eventuellt släppa den på Appstore/Google play.

Efter avslutad utbildning skulle jag gärna jobba med JavaScriptutveckling, kanske som fullstack-utvecklare med kunskaper om både front- och back-end. I en sådan arbetsroll verkar kunskaper om React kunna vara värdefulla, kanske i kombination med något annat front-end ramverk som Angular eller Vue. Nästa steg i mitt React-lärande känns som det skulle kunna vara att titta på hur Redux fungerar.

Trevlig sommar!
