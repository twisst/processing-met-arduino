Waterval
++++++++

.. image:: /imgs/stap8.jpg

In deze instructie gaan we een simpel Arduino circuit maken en gebruiken om een balletje in Processing te besturen.

Benodigdheden
=============

.. image:: /imgs/banner.jpg

Wat heb je nodig?

 * 1 x Arduino bordje (de instructie gaat uit van een Uno)
 * 1 x insteek bordje
 * 1 x lichtgevoelige weerstand
 * 1 x 10kOhm weerstand (kleurcode bruin-zwart-oranje)
 * 1 x potmeter
 * handje vol insteek draadjes

Stappen
=======

1: de potmeter verbinden met het insteekbord
--------------------------------------------

.. image:: /imgs/stap1.jpg

Je hebt hier 3 insteek draadjes voor nodig. Bevestig de positieve en negatieve draadjes (rood en bruin in het plaatje)
met de plus- en min-banen.

Het derde draadje, in het midden op de potmeter, stuurt informatie over de stand van de potmeter naar de Arduino en
moet aan poort A1 (analog A1) worden aangesloten.

2: de lichtgevoelige weerstand aansluiten
-----------------------------------------

.. image:: /imgs/stap2.jpg

We gaan nu de lichtgevoelige weerstand aansluiten.

 1. verbind de plus-baan met de 10kOhm weerstand
 2. verbind de het draadje van de weerstand met die van de lichtgevoelige weerstand en met poort A0 (analog A0) op het Arduino bordje
 3. verbind het draadje aan de andere kant van de lichtgevoelige weerstand met de min-baan

3: de voeding aansluiten
------------------------

.. image:: /imgs/stap3.jpg

Het zwarte draadje moet aan een van de aard aansluitingen (gnd) van de Arduino verbonden worden en de min-baan.
Het rode draadje moet aan de 5V aansluiting van de Arduino en de plus-baan verbonden worden.