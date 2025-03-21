# Interactive functionality

## UI states voor POST interactie

Over het ontwerpen en bouwen verschillende states van de UI-Stack.

### Aanpak

Als je een interactie ontwerpt moet je voor de gebruiker feedback ontwerpen. Je weet dat je met feedback en feedforward ervoor kan zorgen dat gebruikers weten wat ze moeten doen. Dit doe je o.a. met de juiste labels, teksten en button states.  

Als je een POST interactie ontwerpt moet je in de interface nog andere states ontwerpen. Het kan het zijn dat er nog geen data is, dat er data geladen wordt, of dat er iets fout gaat. Hiervoor kan je de UI-Stack gebruiken... Eerst ga je leren wat states en de UI-Stack zijn, daarna ga je de states ontwerpen en bouwen. 


## UI-Stack

Voor het ontwerpen van states met dynamische data gebruiken we de UI stack.  Scott Hurrf schrijft hierover:

> Every screen you interact with in a digital product has multiple personalities.
> 
> [How to fix a bad user interface](https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/)


Voor elke scherm waar een gebruiker iets mee doet moet je verschillende states tonen. Er wordt bijvoorbeeld data geladen, of er kan iets mis gaan. Dan heeft de gebruiker feedback nodig die duidelijk maakt wat er gebeurt. Hiervoor heeft elk scherm 5 states nodig. 

![UI-stack](ui-stack.jpg) *verschillende states van dezelfde pagina.*

1. Loading State
2. Empty State
3. Partial State
4. Error State
5. Ideal state


### Opdracht

Onderzoek met je tafel wat de 5 states van de UI-stack er zijn:

👉 Schrijf de 5 UI-Stack states op het bord

👉 Zoek voor elke state een goed voorbeeld, heb je ook voorbelden waar het niet goed gaat?

👉 Schrijf kort op waar ze voor gebruikt worden

👉 Bespreek met je tafel welke UI-stack states je kan gebruiken voor jouw `post` interactie



## UI-Stack ontwerpen en bouwen

Om de UI-Stack toe te passen is het handig als je precies weet wat je wilt gaan doen. Daarom beginnen we met het uitbreiden van jouw wireflow met meerder states voordat we gaan bouwen! 

### Wireflow uitbreiden met de UI-Stack

Bespreek je wireflow met je buur en bedenk welke schermen de UI-Stack nodig hebben. Voeg de states toe en geef ze een duidelijke titel. 
dat zie er dan bijvoorbeeld zo uit: 




<!--
👉 Breid je wireflow uit met elke UI state
-->



### UI-Stack states bouwen in Liquid

Om de states die je zojuist onderzocht hebt te kunnen toepassen in Liquid zal je veel gebruik gaan maken van if/else statements. 


👉 Schrijf bij de wireflows ook alvast wat dummy code hoe je die state kunt bereiken

👉 Ga in de liquid documentatie op zoek welke tags en filters je zou kunnen gebruiken om UI states te maken en schrijf ze op het bord



👉 Ga aan de slag met ze maken, vanmiddag is er een practicum waar je mee kan gaan typen met Justus en Dion

💪 Maak de UI states in [partials](https://shopify.github.io/liquid/tags/template/#render)

### Bronnen

- [Wireframing User Flow with Wireflows](https://balsamiq.com/learn/articles/wireflows/)
- [UI-Stack - How to fix a bad user interface](https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/)
- [Shopify Liquid documentatie](https://shopify.github.io/liquid/)
- [Officiele Liquid documentatie](https://liquidjs.com/index.html)
