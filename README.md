# Uploadservice Redesign

HTML/CSS templates voor het redesign van de Uploadservice


# Ontwerp rationale

De huidige [Uploadservice](http://uploadserver.staging.lizard.net/) heeft een Excel-achtig voorkomen dat stamt uit de tijd van Lizard 5. De templates en stylesheets van Lizard 5 waren dan ook bedoeld voor een specifieke use-case: een map viewer. Vandaar dat de volledige breedte gebruikt werd en er nog sporen zichtbaar zijn van een kaartlagenzijbalk. 
Het totaal resulteerde in een technisch uitziend product dat voor de gemiddelde gebruiker nogal intimiderend is om te gebruiken. 

We hebben de huidige UI (juni 2015) onder de loep genomen en geherstructureerd & opgepoetst volgens basis ontwerprichtlijnen.

Deze richtlijnen worden toegelicht in de volgende secties:

## Eenduidige navigatie en positiebepaling

Voor de hoofdnavigatie wordt de breadcrumb gebruikt. In dit ontwerpvoorstel is de klant/organisatie 'Purmerend' het hoogste niveau. Projecten vallen daaronder: Purmerend/projectnaam. Zo weet een gebruiker altijd als of voor wie hij of zij werkt, en het is ook altijd duidelijk in welk project gewerkt wordt.


## Witruimte

Hiermee bedoelen we de ruimte tussen interface elementen. Deze ruimte is in ons geval ook daadwerkelijk wit maar dit hoeft dus niet. In het oude design werd witruimte niet optimaal toegepast, waar de leesbaarheid, begrip en aandacht van de gebruiker onder leden.

Om dit te verbeteren hebben we de afstand tussen de elementen op veel plaatsen vergroot. Vaak moesten we hierdoor ook de positie en de grootte van de elementen aanpassen.

Het resultaat en het effect is goed zichtbaar in deze zij-aan-zij afbeelding: 

![Whitespace difference](http://i.imgur.com/LY6OzIw.jpg)


## Benamingen

Teksten op labels en buttons waren vaak te algmeen en te technisch. We hebben ze vertaald in termen die voor de minder technische gebruiker beter te begrijpen zijn.


## Mobielvriendelijk

Zoals gezegd is de oude Uploadservice gebaseerd op Lizard 5. Lizard 5 is niet specifiek gebouwd met mobiel gebruik in gedachten. Gebruikers van de Uploadservice gaan naar verwachting wel gebruikmaken van tablets. Daarom is 'responsiveness' hier wel van belang. In het redesign hebben we rekening gehouden met de formaten tablet tot desktop.


## UI consistentie

De interface moet zo voorspelbaar mogelijk zijn. Buttons die leiden tot destructieve acties zijn daarom rood, buttons die leiden tot constructieve acties zijn groen. Al dit soort zaken zijn vastgelegd in stylesheets, geïntegreerd met Twitter Bootstrap via SASS.

Effect: Als je bijvoorbeeld een `<button>` element gebruikt ziet die er meteen uit alsof hij erbij hoort.

Eventuele foutmeldingen zijn menselijker van toon en inhoud. Afbeeldingen-als-UI hebben altijd een label ter verduidelijking en worden minder vaak toegepast.


## Minimalistischer

'Een goede interface zie je niet' zei een bekende ontwerper ooit. Deze gedacht komt terug in de sub-navigatie van projecten. Als je naar een project navigeert, kom je op het Dashboard terecht. Dit is omdat je vaak eerst overzicht en voortgang wil zien. De subnavigatie is hier nog volledig: iconen en tekst-labels zichtbaar.

Als je nu navigeert naar Configuratie of een ander onderdeel van het project, dan zal de subnavigatie inklappen: alleen iconen zichtbaar. De interface wordt minder zichtbaar, want de gebruiker is al gewend. Op de elementen zitten wel labels met tekst (on hover) ter verduidelijking.

Bevestigingspopups worden alleen nog gebruikt wanneer het echt nodig is.


## Minder tekst

Op sommige plekken werd erg veel tekst en uitleg gegeven. Dit kan beter in de handleiding worden gezet of in de Help-sectie die via het menu rechtsboven te vinden is.


## Gebruiksvriendelijkere datum/tijd aanduiding

In plaats van een volledige datum/tijd weergeven die de gebruiker moet interpreteren, wordt op plaatsen waar het relevant is aangegeven hoe recent het item is: '3 dagen geleden'.


## Overig

Geen pagination maar een combinatie van 'facetted' zoeken en 'endless scroll'.




# Toegepaste software

 - [SASS](http://sass-lang.com/) & [Compass](http://compass-style.org/)
 - [Twitter Bootstrap geïntegreerd met SASS](http://getbootstrap.com/css/#sass)

# Screenshot

![Screenshot](http://i.imgur.com/soMrJB9.jpg)





