### Titel
Litteraturwebben

### Datum
2015-06-08

### Abstrakt
_Denna rapport berör utvecklingen av en applikation i kursen Individuellt mjukvaruprojekt på Linnéuniversitetet under våren 2015. Rapporten beskriver applikationen Litteraturwebben som riktar sig till litteraturintresserade och som kan användas av förlag för att presentera deras böcker samt ladda upp e-böcker som användare sedan kan ladda ner. Applikationen är skapad med hjälp av ramverket Ruby on Rails. I rapporten kommer jag fram till att detta ramverk är väldigt effektivt men brister något i flexibilitet. Genom utvecklingsprocessen har också värdet av en iterativ utvecklingsprocess med detaljerad planering och tidrapportering framträtt._

### Inledning och bakgrund
###### Mål
Målet för mitt projekt var att skapa en applikation för böcker och författare. Tanken var att personal på ett mindre eller mellanstort förlag själva skulle kunna lägga till information om sina böcker och författare samt ladda upp e-böcker och bildfiler. En användare skulle sedan kunna surfa in på applikationen och läsa om förlagets böcker och författare, plus att denne kunde skapa ett konto på sidan och då kunna ladda ner förlagets e-böcker. 

###### Teknik
För att skapa applikationen använde jag mig av ramverket [Ruby on Rails](RailsGuides, http://guides.rubyonrails.org/getting_started.html#what-is-rails-questionmark). Det bygger på programmeringsspråket Ruby. Filosofin bakom Rails är att programmeraren ska öka sin produktivitet genom att följa de strikta konventioner som ramverket erbjuder. För att publicera tjänsten använde jag mig av molntjänsten [Heroku](https://www.heroku.com/features)som också erbjuder en PostgreSQL databas. Jag har även använt mig av enkla jQuery-funktioner samt [Sass](http://sass-lang.com/) och [Bootstrap](http://getbootstrap.com/) för att underlätta arbetet med sidans utseende och gränssnitt. 

###### Arbetssätt
I projektets inledning skapade jag en vision samt en kravspecifikation. Därefter har jag följt en iterativ utvecklingsprocess med veckolånga iterationer där de inledande veckorna ägna-des åt att färdigställa den grundläggande arkitekturen och eliminera de största riskerna. Inför varje vecka har jag skrivit en detaljerad planering som avslutats med en tidrapport. 

### Positiva erfarenheter
Till mina positiva upplevelser av projektet hör ramverket Rails. Det gick väldigt snabbt att komma igång och det passade väldigt bra för den typen av applikation jag ville göra – en sida för innehåll med CRUD-funktionalitet samt användarinloggning. I början använde jag mig mycket av [Ruby on Rails Tutorial av Michael Hartl](https://www.railstutorial.org/book/frontmatter) som är en utmärkt guide för den som inte arbetat med Rails tidigare. Tack vare den hade jag en publicerad version av min applikation redan första veckan och kom också igång med testning från start.

En annan teknik som jag kommer att använda mig av i framtiden är Sass som hjälpte mig väldigt mycket när det kom till att stila applikationen. Det är exempelvis väldigt enkelt att arbeta med olika skärmstorlekar. Jag hade också en positiv upplevelse av Bootstrap även om jag ibland gjorde på mitt eget sätt för att exempelvis få saker och ting att anpassa sig till en mindre skärm.

Jag har alltid haft svårt och varit lite emot att ha en allt för strikt planeringen, plus att jag har varit lite dålig på att skriva upp mina tider. Men till sist insåg jag faktiskt fördelarna med att ha en detaljerad planering för varje vecka. Det skapade struktur och fick mig att veta vad som behövdes göra. Jag kommer nog att använda det arbetssättet även i framtida projekt även om det inte är ett krav. 

### Negativa erfarenheter
Till de negativa upplevelserna av projektet hörde att det tog några iterationer innan jag kom igång med planering och tidrapportering. Att jag enligt iterationsplan 2 bara jobbat 8 h under den första iterationen beror mest på att jag inte skrev upp alla tider. Det blev bättre sen då jag till och med skapade ett Exceldokument där jag skrev in alla tidpunkter då jag arbe-tade. 
	
Utvecklingen med Ruby on Rails har som sagt gått bra men inte varit helt problemfri. Från början fick jag det inte att fungera på min Windowsdator vilket tvingade mig att installera Ubuntu på en virtuell maskin. Jag tycker också att ramverket gör det svårt när man vill göra något som bryter mot dess konventioner, t.ex. har jag lagt ner väldigt många timmar på att få till så kallade nästlade formulär, t.ex. ett formulär för ny bok där man även kan lägga till en författare. 

I framtiden behöver jag också bli bättre på att inte blir för uppslukad av att lösa vissa problem. Ibland kunde jag sitta i flera timmar bara för att få till någon detalj som jag var fast besluten om att lösa. Man borde bestämma i förväg hur långt tid ett problem får ta innan man söker en annan lösning, ber om hjälp eller bara låter problemet vila medan man arbetar på någonting annat. 

### Sammanfattning
Min applikation är på inga sätt unik och kommer inte att bli någon stor succé bland massorna, även om det finns ett förlag där jag en gång i tiden gjorde praktik som skulle kunna vara intresserad av den. Men den största behållning jag har fått av projektet är att jag har lärt mig ett helt nytt ramverk samt blivit bättre på det jag redan kunde, exempelvis HTML och Css. Jag har också insett nyttan av en iterativ utvecklingsprocess och värdet av att planering och rapportering. 
