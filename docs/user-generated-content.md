# Interactive functionality

## User Generated Content

Deze workshop gaat over het POSTen en bewaren van data op de server, en hoe je dit weer kunt tonen op een pagina.


### Aanpak

Vandaag gaan we—net als in Sprint 7 bij de squad page—gegevens _opslaan_ in Directus. Maar deze keer voor het project van jullie opdrachtgever.

Net als bij de squad page moeten we daarvoor eerst bedenken welke interactieve functionaliteit we willen toevoegen, en wat dus de _User Generated Content_ wordt. Als de database van jullie project hiervoor aangepast moet worden, kunnen we dat meteen doen.

Hierna gaan we een Wireflow schetsen met nette URLs, routes aanmaken, een HTML formulier maken en de data opslaan in Directus. Je kunt daarna verder met het uitwerken van je ontwerp in code.

Komende vrijdag ga je je interactie testen tijdens de code/design review.

### Progressive Enhancement

Progressive Enhancement is een coding strategie, waarmee je er voor kunt zorgen dat je website het _altijd_ doet, voor _iedereen_. Het zorgt er ook voor dat je minder hoeft te testen. Tijdens deze sprint gaan we je in verschillende workshops deze strategie aanleren, zodat je dit uiteindelijk kunt dromen:

1) Bouw de functionaliteit robuust, met de simpelste techniek (HTML en Server-Side Rendering)​
2) Voeg Mobile First CSS voor de huisstijl toe​
3) _Enhance_ de functionaliteit geleidelijk voor een betere User Experience​ (De leukste stap. Met moderne CSS en client-side JS.)

Later deze sprint (en in Sprint 10 en 11 nog meer) gaan we je een aantal strategieën leren om dit enhancen geleidelijk goed te doen. Voor nu richten we ons op de eerste twee stappen van _Progressive Enhancement_, zodat we die goed onder de knie krijgen. Het is helemaal ok als je vandaag nog niet jouw uiteindelijke ontwerp hebt kunnen maken.


## Interactieve functionaliteit bedenken en schetsen

Tot nu toe heb je minimaal een overzichtspagina en een detailpagina gemaakt voor de opdrachtgever. Je hebt hiervoor `GET` requests gebruikt. Voor je eigen routes én voor de fetches naar Directus. Hier komen deze sprint `POST` requests bij. Maar hiervoor moeten we eerst bepalen _wat_ we willen gaan maken.

Wil je een opfrisser over het verschil tussen `GET` en `POST`, lees dan eerst eens [de bron uit Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/user-generated-content.md#get-vs-post).

Overleg met studenten die dezelfde opdrachtgever hebben welke functionaliteit je zou kunnen maken, waarbij je gegevens in jullie Directus database aan moet passen of toe moet voegen. Wat wordt dus jouw _User Generated Content_ deze sprint? Misschien heeft het ontwerp van je opdrachtgever al een duidelijk idee (een wish list, likes, comments, een vragenlijst die je in kunt vullen, etc). Misschien is er tijdens de laatste Sprint Review een idee ontstaan, dat je wilt gaan maken. Of misschien wil je hiervoor zelf wel iets compleet nieuws verzinnen en laten zien tijdens de komende Sprint Review. Alles mag.

Maak een snelle schets van jouw idee, zodat je deze kunt overbrengen aan een ander aan je tafel. Deze leertaak is individueel, maar probeer samen in te schatten of een bepaald idee haalbaar is, en hoe. Analyseer samen jullie Directus database, en noteer voor jezelf mogelijke problemen en knelpunten die je verwacht voor jouw idee. Als je een aanpassing in de database nodig hebt, kunnen we dat voor jullie doen, net als bij de WHOIS API. Het is hiervoor handig als je zelf al bedenkt wat je nog nodig hebt. Als jouw idee misschien te ingewikkeld is, hou dan een ander idee achter de hand. Overleg uiteindelijk met een docent over de haalbaarheid.

Schrijf voor jouw functionaliteit een User Story, en maak hiervoor een nieuw issue aan. Gebruik hiervoor eventueel [de workshop uit Sprint 5](https://github.com/fdnd-task/fix-the-flow-interactive-website/blob/main/docs/user-interface-design.md#user-story). Leg in je issue kort uit wat je nodig gaat hebben, en voeg je eerste schets(en) toe. Voeg ook een hifi ontwerp in Figma toe aan het issue.

Heb je voor jouw functionaliteit een aanpassing in de database nodig? Plaats dan een link naar dit issue op Teams, of tag in je issue een docent die dit op kan pakken. Het kan even duren voordat dit gedaan is, maar je kunt alvast verder met de volgende stappen.


## Bouw de functionaliteit robuust, met de simpelste techniek (HTML en Server-Side Rendering)​

De simpelste techniek voor User Generated Content is een `<form>` in HTML, met waarschijnlijk een submit button. Dit werkt in elke browser, op elk apparaat, overal, voor iedereen. En dat is je doel als frontender.

Deze _simpelste techniek_ voor eindgebruikers—een `<form>`, HTTP methods en URLs—, gecombineerd met onze Directus JSON API en Express, brengt best wat complexiteit met zich mee. Daarom gaan we deze interactie eerst weer uittekenen.

### Wireflow breakdown met URLs

Schets een Wireflow van jouw interactie. Gebruik hiervoor [de workshops uit Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/filteren-en-sorteren.md#wireflow-schetsen) en [Sprint 8](https://github.com/fdnd-task/server-side-rendering-server-side-website/blob/main/docs/templating-met-json.md#wireframe-met-statische-en-dynamische-data-en-componenten), en pas deze toe op het formulier dat je nu ontwerpt. Bedenk nette URLs voor je pagina's en routes, en schrijf deze erbij.

Annoteer je Wireflow met hints voor je dynamische data, en bedenk ook hoe je aan kunt geven dat je een `POST` afhandelt.

💪 Na het afhandelen van een `POST`, wil je bezoekers doorsturen naar de pagina waarop ze kunnen zien wat er veranderd is (_redirecten_, met een `303` _status code_); kun je dat ook aangeven in je Wireflow?

Voeg je Wireflow toe aan je User Story issue en vraag hierop feedback.

We gaan straks verder met het aanmaken van routes, het maken van het formulier, en het opslaan van gegevens in Directus.

### Routes

Gebruik de hints uit je Wireflow schets, de voorbeeldcode die je van ons hebt gekregen (in comments in `server.js`) en de bronnen hieronder om jouw `POST` route(s) aan te maken in `server.js`. Je kunt hiervoor nieuwe issues aanmaken.

Neem bestanden of stukken code die je mee wilt nemen uit je vorige repository mee. Misschien wil je wel een deel opnieuw gaan bouwen.

#### Bronnen

- [GET vs POST @ Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/user-generated-content.md#get-vs-post)
- [`app.post()` @ Express](https://expressjs.com/en/5x/api.html#app.post.method)
- [Routes en query parameters @ Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/filteren-en-sorteren.md#routes-en-query-parameters)
- [Routing @ Sprint 8](https://github.com/fdnd-task/server-side-rendering-server-side-website/blob/main/docs/routing-request-response.md#routing)


### Formulier maken

Bouw je formulier in een Liquid view.

Als je een opfrisser wilt van hoe je formulieren afhandelt, zie dan de bronnen uit Sprint 7.

#### Bronnen

- [Oefenen met een POST @ Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/user-generated-content.md#oefenen-met-een-post)
- [Maak één squad page @ Sprint 7](https://github.com/fdnd-task/connect-your-tribe-squad-page/blob/main/docs/user-generated-content.md#maak-%C3%A9%C3%A9n-squad-page)


### Opslaan in Directus

In `server.js` staat wat code uitgecomment. Gebruik deze om stap voor stap data op te slaan in Directus. De exacte code verschilt per project en per onderwerp, dus hiervoor zul je zelf aan de slag moeten. Hier kunnen we je goed bij helpen.

Jullie hebben dit eerder gedaan in de team-squad-page opdracht in Sprint 7, dus pak je code daarvan erbij.

#### Bronnen


- [Create an item @ Directus](https://docs.directus.io/reference/items.html#create-an-item)
- [Update an item @ Directus](https://docs.directus.io/reference/items.html#update-an-item)
