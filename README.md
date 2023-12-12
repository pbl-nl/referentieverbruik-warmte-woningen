# Referentieverbruik warmte woningen python

Referentieverbruik warmte woningen python kan worden gebruikt om de gemeentebestanden uit het project [Referentieverbuik warmte woningen](https://www.pbl.nl/publicaties/referentieverbruik-warmte-woningen#:~:text=Het%20referentieverbruik%20is%20bedoeld%20voor,voor%20particuliere%20eigenaren%20en%20bewoners.) te genereren zonder daarvoor de excel template te gebruiken. Voor meer informatie over de achtergrond en het gebruik van het referentieverbruik warmte woningen, zie het achtergrondrapport, en handleiding en bijsluiter bij het project. 

## Installatie

Het model is via Github binnen te halen. De benodigde mappenstructuur wordt automatisch meegegeven.

Het model gebruikt de packages [numpy](https://numpy.org/) en [pandas](https://pandas.pydata.org/) in de berekeningen. Deze packages zijn daarom vereist in de environment waar het model gedraaid wordt.

## Gebruik

Voeg in de map 'gemeente_inputdata' de databestanden voor de gemeenten toe. Deze zijn te vinden in het [PBL dataportaal referentieverbuik warmte woningen](https://dataportaal.pbl.nl/downloads/VIVET/Referentieverbruik_warmte/). In deze bestanden kunnen aanpassingen worden gedaan als er meer gedetaileerde informatie rondom de energetische kwaliteit van de betreffende woningen beschikbaar is. 

Het model biedt een aantal opties aan voor aanpassing van het gebruik. Deze variabelen zijn in het script rekenregels.py aan te passen.

- Met de variabele 'GM_codes' is aan te passen welke gemeente(n) meegenomen worden.
    - Een enkele gemeente kan worden doorgerekend door de gemeentecode van die gemeente als string binnen de lijst (de blokhaken) in te voeren.
    - Meerdere gemeentes kunnen worden doorgerekend door de bijbehorende gemeentecodes als lijst van strings in te voeren, dat wil zeggen binnen de blokhaken, gescheiden door komma's, met enkele aanhalingstekens om iedere gemeentecode.
    - Door enkel 'alle_inputdata' in de lijst in te vullen, worden alle databestanden in de map 'gemeente_inputdata' gebruikt voor de doorrekening. 
- Met de variabele 'behoud_nullen_excel_parameter' is aan te passen of de 'leading zeroes', de getallen nul  vooraan de gemeentecode en wijkcode behouden blijven wanneer de output geopend wordt in excel. Deze parameter staat standaard op 'False', omdat deze de output lastiger te gerbuiken maakt voor verdere bewerkingen.
- Met de variabele 'wegschrijven_per_gemeente_parameter' Is aan te passen of voor elke gemeente een apart outputbestand gemaakt wordt, of dat alle resultaten in ��n enkel outputbestand wordne weggeschreven. Houdt er rekening mee dat het wegscrijven van veel resultaten in ��n bestand lang kan duren. Dit is een verbeterpunt in het model. 
    
Het bestand outputvariabelen.py wordt gebruikt om de structuur van de output dataframe, en daarmee de output .csv, in te stellen. Tevens zijn daar ter referentie de eenheden van de verschillende variabelen te vinden.

De .csv's in de map datatabellen zijn kentallen overgenomen uit de gemeentebestanden. Deze waarden worden gebruikt in de rekenregels om de uitkomsten van de gemeentebestande  te reproduceren.

## Licentie

[GPL3.0](https://choosealicense.com/licenses/gpl-3.0/)

## Contact

Schroom niet contact op te nemen voor vragen en suggesties.

Wessel Poorthuis

wessel.poorthuis@pbl.nl

Planbureau voor de Leefomgeving
