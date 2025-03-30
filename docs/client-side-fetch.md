# Interactive functionality

## Client-Side Fetch met Server-side partials 
Over het client-side fetchen van data volgens het principe van Progressive Enhancement

### Aanpak

Deze sprint ontwerp en bouw je een interactie met een POST request. Om ervoor te zorgen dat je website het altijd doet, leer je dit te bouwen met de coding strategie Progressive Enhancement.

Als je goed weet wat je gaat bouwen (laag 1) en je hebt de POST server-side gebouwd met een HTML formulier en eenvoudige CSS (laag 2) dan kan je de User Experience verbeteren met client-side JS (laag 3 van Progressive Enhancement). Nu wordt het leuk !

Vandaag ga je eerst bedenken en schetsen hoe je de interactie kan verbeteren met states van de UI stack.
Daarna ga je leren hoe je met client-side JS data kan fetchen om de gebruiker goede feedback te geven.

<!--
Deze workshop de POST interactie helemaal laten schetsen, inclusief client-side enhancement. laag 3 van PE. 

UI stack en states toevoegen: loading state, succes state

Opdracht: Schets een UML diagram met de routing en pseudo-code voor de data-flow en control-flow van de Node-code

Teken de interactie voor de user story in een wireflow. Zorg dat je de verschillende states van het formulier uitwerkt
(het versturen van data, een succes state en mogelijke errors, etc…)
Noteer per state de routing
Voeg aan de wireflow een control-flow toe:
Noteer welke data wordt ge-POST, welke data wordt opgehaald met een fetch en welke data wordt doorgegeven aan een volgende functie of methode

Control Flow
Met een Control Flow beschrijf je de logica / structuur van je code. De Control Flow (of Flow of Control) toont de volgorde van methodes en functies die worden uitgevoerd in de code. Zo krijg je een duidelijk overzicht van hoe de code werkt en in welke volgorde.
-->

## Enhancement

Volgens de *hierarchy of User Needs* moet je ervoor zorgen dat jouw interactie eerst *functional* en *reliabel* is, voordat je het *usabel* en *pleasurable* kan maken.

![Hierarchy of User Needs](aarron-walter-user-needs.png) 

Dit betekent dat je jouw interactie eerst met een HTML formulier, POST en Server-side betrouwbaar moet bouwen zodat je website het altijd doet.

Daarna kan je de interface verbeteren, oftewel 'enhancen' met client-side scripting. Stel dat een browser bepaalde CSS of Javascript die je gebruikt niet ondersteund, dan zal een browser 'terug vallen' naar een werkende versie.

### Loading state en Succes state
Met behulp van de UI-Stack kan je verschillende states van een pagina ontwerpen als je met dynamische data werkt. De empty state heb je al, die kan je tonen als er bv nog geen berichten zijn getoond. Een loading state en succes state kan je tonen als je posten van data in de browser gaat regelen. 

Op het moment dat een gebruiker op een knop klikt, er wordt data gepost en de response terugestuurd, kan je een loading state tonen

![Loading state](loading-state.gif) 
*Door het tonen van een loading state weet de gebruiker dat er iets gebeurt*

Als het posten van data gelukt is, en de browser heeft response data binnen, kan je feedback tonen dat het gelukt is met een succes state.

![Loading state](loading-state.gif) 
*Door het tonen van een succes state weet een gebruiker dat het versturen en laden data is gelukt*

#### 👉 Loading states en Succes states onderzoeken
Zoek met je tafel verschillende voorbeelden van loading states en succes states. Gebruik [codepen.io](https://codepen.io/) ter inspiratie. Je kan ook zoeken naar micro interactions ...  

#### 👉 Wireflow schetsen met states
Schets de wireflow van jouw interactie. Toon eerst de *ideal states*, de flow dat alles goed gaat.  

Voeg daarna verschillende states toe aan je wireflow. Gebruik hiervoor de state van de UI-Stack: Empty state, Loading state en Succes state

![Wireflow met states](wireflow-met-states.jpg) 
*HIER EEN GOED VOORBEELD TONEN In een Wireflow kan je de verschillende states tonen*



## Server-side vs. Client-side

Hier een uitleg/herhaling over het verschil tussen server-side en client-side.

### Server-side POST Break down

Hier een opdracht waarin studenten de wireflow en server-side POST techniek, inclusief formulier en Directus gaan tekenen zoals ze dat al gemaakt.
De wireflow uitbreiden met een control-flow

![Wireflow met control flow](wireflow-met-states.jpg) 
*HIER EEN GOED VOORBEELD TONEN In de Control Flow toon je de logica en structuur van je code*

### Client-side Fetch

Techniek uitleggen, wat is fetch? 

👉 Oefenopdracht om met client-side javascript data te fetchen op directus. 

👉 Oefenopdracht om met (liquid) partials te werken, dus dezelfde route te gebuikern als de server-side code.

### States tonen na een Client-side Fetch

👉 Hoe werkt dan de techniek voor het tonen van een loading state? En de succes state? na het laden van data?


💪 wat kan je nu nog meer doen op de client? View transitions!

### Client-side Fetch Break down 

👉 Hier een opdracht waarin studenten de wireflow gaan uitbreiden met pseudo-code van de client-side POST met partials (en directus)

