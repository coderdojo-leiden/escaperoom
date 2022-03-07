# Escaperoom
*Bouw een escaperoom in Scratch*

In deze opdracht gaan we zelf een escaperoom bouwen. We beginnen in een kamer met wat spuillen (zoals een tapijt, een schilderij, en een kluis). De deur in die kamer is 'op slot'. Het doel van het spel is om de deur open te maken door erop te klikken, zodat je naar buiten kunt.

Zo ziet het er uit als je de opdracht klaar hebt:

[escaperoom finished project](images/nl/finished-project.gif)

We beginnen met een leeg project waar alle benodigdheden al in sprites zitten. Op deze manier hoef je je alleen maar druk te maken om de code-blokken! Dit lege project kun je in de Scratch editor openen via ons [escaperoom start project](https://scratch.mit.edu/projects/629181159/editor).

## Start situatie

We beginnen om alle sprites een goede startpositie te geven als we ons spel starten. Mocht er tijdens het spel per ongeluk iets verschuiven, dan weten we dat de volgende keer alles weer goed staat zoals we hebben bedoeld.

### Verberg Huis en 'ontsnapt'-tekst

Het huisje moet pas getoond worden als de deur open is. Dus die moet verborgen worden als op de groene vlag wordt gedrukt. Hiervoor bestaat de gebeurtenis "wanneer op ![groene vlag](images/green-flag.png) wordt geklikt"

1. Selecteer de **ontsnapt!**-sprite
2. Zoek bij *Gebeurtenissen* het volgende blokje:  
   ![Gebeurtenissen | groene vlag](images/nl/events-greenflag.png)
3. Sleep deze naar het grote witte vlak in het midden
4. Zoek bij *Uiterlijken* het volgende blokje:  
   ![Uiterlijken | verdwijn](images/nl/looks-hide.png)
5. Zet deze vast aan het blokje erboven

Je kunt op twee manieren controleren of je code werkt:

* door éénmaal met je muis op jouw code-blok te klikken
* door rechtsboven op de groene vlag te klikken

Als het goed is, verdwijnt het huisje nu.

> Kun jij dit nu ook doen voor de **ontsnapt!2**-sprite?

### Toon de andere objecten, met het goede uiterlijk

We gaan nu zorgen dat alle andere objecten op de juiste plek, en met het juiste uiterlijk worden getoond, als het spel wordt gestart.

Sommige sprites hebben méér dan 1 uiterlijk, dit kun je zien door bovenaan op de tab 'Uiterlijken' te klikken:  
![Tab Uiterlijken](images/nl/tab-costumes.png)

1. Selecteer de **tapijt**-sprite
2. Net als hierboven, sleep de gebeurtenis "wanneer op de groene vlag wordt geklikt" naar het midden
3. Zoek nu bij *Uiterlijken* het volgende blokje, en sleep deze naar je code-veld:  
   ![Uiterlijken | verander uiterlijk](images/nl/looks-switchcostume.png)
4. Kies nu het juiste uiterlijk-nummer (is dit `1` of `2`? Kijk even welke uiterlijken er beschikbaar zijn!)
5. Zoek bij *Uiterlijken* het volgende blokje, en sleep deze naar je code-veld:  
   ![Uiterlijken | verschijn](images/nl/looks-show.png)

Werkt je code? Testen!

> Kun jij dit nu ook doen voor de **schilderij**-sprite, de **kluis**-sprite, en de **deur**-sprite?

### Startpositie

Ook willen we graag dat iedere sprite op de juiste plaats op het scherm wordt getoond, zodat het er iedere keer hetzelfde uitziet. Dit laten we aan Scratch weten waar het plaatje moet staan ten opzicht van het midden van het scherm. Van links naar rechts wordt aangegeven met een `x`, en van beneden naar boven met een `y`. Laten we hiervoor beginnen met het tapijt.

1. Selecteer de **tapijt**-sprite
2. Zoek nu bij *Beweging* het volgende blokje, en sleep deze naar je code-veld vlak **boven** het "verdwijn"-blokje:  
   ![Beweging | ga naar x y](images/nl/motion-goto_x_y.png)  
   Op deze manier zetten we de plaats goed voordat deze wordt getoond.
3. Zorg dat het getal achter de `x` en de `y` allebei een `0` is

> Kun jij dit nu ook doen voor de **schilderij**-sprite, de **kluis**-sprite, de **deur**-sprite, en het huisje (dus de **ontsnapt!**-sprite)?

## Rondkijken en zoeken in de kamer

Bij een escaperoom moet je op zoek gaan naar aanwijzingen om te ontsnappen. In ons kleine kamertje willen we de volgende dingen inbouwen:

* Als je onder het tapijt kijkt, vind je geen aanwijzing.
* Als je achter het schilderij kijkt, zie je dat er een code op de muur staat geschreven
* Als je de kluis wilt openen, wordt er om een code gevraagd. Bij het invullen van de goede code gaat de kluis open
* In de kluis ligt een sleutel, en die sleutel moet je gebruiken om de deur van het slot te halen
* Als de deur van het slot is, kun je hem open maken en naar buiten

Al deze eigenschappen gaan we nu maken!

### Aanwijzingen: wisselen van uiterlijk

Als eerste willen we zorgen dat je het tapijt op kan tillen, en het schilderij opzij kan schuiven, als je er op klikt. Nog een keer klikken moet alles weer terugzetten. Dit doen we door gebruik te maken van de verschillende uiterlijken bij iedere sprite.

1. Selecteer de **tapijt**-sprite
2. Zoek nu bij *Gebeurtenissen* het volgende blokje, en sleep deze naar een leeg plekje in je code-veld:  
   ![Gebeurtenissen | geklikt op sprite](images/nl/events-spriteclicked.png)
3. Zoek nu bij *Uiterlijken* het volgende blokje, en sleep deze naar je code-veld, en zet hem vast aan de goede gebeurtenis:  
   ![Uiterlijken | volgend uiterlijk](images/nl/looks-nextcostume.png)

> Kun jij dit nu ook doen voor de **schilderij**-sprite?

### De code weergeven: een uiterlijk bewerken

Je zag misschien dat er nog geen code op de mur geschreven stond, toen we op het schilderij klikten. We gaan nu een **zelf bedachte code** op de muur achter het schilderij zetten, door het uiterlijk van het opzij geschoven schilderij te bewerken.

1. Selecteer de **schilderij**-sprite
2. Klik bovenaan op de tab 'Uiterlijken'
3. Selecteer nu het tweede uiterlijk door er op te klikken.  
   Als het goed is zie je nu het opzij geschoven schiulderij in het midden van het scherm
4. Je kunt het plaatje iets groter of kleiner op je scherm krijgen door de `+` en `-` knopjes te gebruiken onderaan het scherm:  
   ![Uiterlijk - zoom](images/costume-zoom.png)
5. Klik nu op het Tekst-tool: ![Uiterlijk-tekst](images/costume-tool-text.png)
6. Kies zelf een passende kleur, en een leuk lettertype.
   Dit vind je bovenaan het bewerk-paneel:  
   ![Uiterlijken - tekst formaat](images/nl/costume-text-format.png)
7. Klik nu ergens naast het schilderij op een lege plek, en typ het eerste getal van je eigen verzonnen code. Je ziet deze meteen verschijnen. Misschien moet je de plaats en de grootte nog even aanpassen, zodat het helemaal naar je zin is.
8. Doe dit ook voor de andere getallen uit je code, en zet ze op een iets andere plek.
9. Als je klaar bent, klik dan eens afwisselend op uiterlijk 1 en uiterlijk 2. Ben je tevreden met het resultaat? Anders kun je misschien nog wat bewerken tot je tevreden bent.

### De kluis openen

Als je de kluis wilt openen, moeten we om een code vragen. En als die code goed is ingevuld, gaat de kluis open. Wat moeten we daarvoor doen?

#### Waarnemen

Als je in Scratch iets wilt vragen aan de gebruiker, of kijken of er misschien een toets is ingedrukt, of dat de muis misschien beweegt, heet dat "Waarnemen". Dit gaan we hier gebruiken.

1. Selecteer de **kluis**-sprite
2. Start een nieuw stukje code, en begin weer met een gebeurtenis wanneer op de sprite wordt geklikt.
3. Zoek nu bij *Waarnemen* het volgende blokje, sleep deze naar je code-veld, en zet hem vast aan de goede gebeurtenis:  
   ![Waarnemen - vraag en wacht](images/nl/sensing-ask-wait.png)
4. Pas de vraag aan naar `Wat is de code?`

Nu moeten we alleen de kluis openen als de goede code wordt ingevoerd. Of, anders gezegd:

    ALS het antwoord hetzelfde is als de code op de muur
    DAN doe ik de kluis open
    
Om dit te kunnen doen, maken we in Scratch gebruik van de blokjes onder "Besturen". Dit kan zijn dat we ergens op willen wachten, of een als-dan vraag willen gebruiken, of zelf iets meerdere keren (of voor altijd) herhalen.

1. 

#### Signalen





### 
