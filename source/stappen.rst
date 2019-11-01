Stappen
=======

Instructie template aanpassen
-----------------------------

Deze instructie is voornamelijk bedoeld om uit te leggen hoe nieuwe instructies te maken op basis van deze template.
Maar, zo nu en dan zullen er ook aanpassingen aan de template gemaakt moeten maken. De werkwijze is niet heel anders dan 
voor nieuwe instructies:

1. clone de `instructie_template <https://github.com/coderdojonijmegen/instructie_template.git>`_
2. maak aanpassingen aan de template
3. `bouw de html <#html-bouwen>`_
4. commit en push de aanpassingen en aangepaste HTML

Nieuwe instructie maken
-----------------------

De `instructie_template <https://github.com/coderdojonijmegen/instructie_template.git>`_ is op GitHub opgeslagen als template.
Dit betekend dat je de repository als basis voor een nieuwe repository kunt gebruiken. Dit is een handig startpunt voor
nieuwe instructies.

Om de nieuwe repository op basis van de template te maken, klik je op de groene *Use this template* knop:

.. image:: /imgs/github_use_template_repo.png

Clone vervolgens de nieuwe repository en 

HTML bouwen
-----------

Scratch blokken gebruiken
-------------------------

Je kunt in de instructies gebruik maken van Scratch blokken. Gebruik daarvoor de volgende code:

.. code::

   .. raw:: html

      <div class = "scratch">
          when flag clicked
          clear
      </div>

En dat resulteert dan in:

.. raw:: html

   <div class = "scratch">
       when flag clicked
       clear
   </div>

Voor meer informatie over de te gebruiken blokken vind je op de Scratch Wiki:
`Block Plugin/Syntax <https://en.scratch-wiki.info/wiki/Block_Plugin/Syntax>`_
