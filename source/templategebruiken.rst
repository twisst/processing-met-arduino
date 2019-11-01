Het template gebruiken
======================

Veel voorkomende opmaak
-----------------------

Hoofdstukken
^^^^^^^^^^^^

Hoofdstukken worden gemaakt door de titel te onderlijnen over de volledige lengte. Dus bijvoorbeeld:

.. code::

   ##########
   deel titel
   ##########

   ***************
   hoofdstuk titel
   ***************

   sectie
   ======

   sub-sectie
   ----------

   sub-sub-sectie
   ^^^^^^^^^^^^^^

   paragrafen
   """"""""""

Dit voorbeeld volgt `Python's Style Guid for documenting <https://docs.python.org/devguide/documenting.html#style-guide>`_,
maar in principe zegt het karakter niets over welk niveau het is. De niveaus worden bepaald door de volgorde van de
karakters als onderlijning.

Tekst formatering
^^^^^^^^^^^^^^^^^

 - `*schuin*` : *schuin*
 - `**vet**`: **vet**
 - `\``code\```: ``code``

Lijsten
^^^^^^^

.. code::

   * dit is een lijst met bullets
   * het heeft twee items, waarbij het tweede
     twee regels beslaat.

   1. dit is een genummerde lijst
   2. het heeft ook twee regels

   #. dit is een automatisch genummerde lijst
   #. het heeft ook twee regels

Geneste lijsten zijn ook mogelijk, maar moeten wel door een lege regel van elkaar gescheiden worden:

.. code::

   * dit is een lijst
   * met meerdere regels

     * en meerdere
     * niveaus

   * en dan weer door

Zo dus:

 * dit is een lijst
 * met meerdere regels

   * en meerdere
   * niveaus

 * en dan weer door

Tabellen
^^^^^^^^

.. code::

   +------------------------+------------+----------+----------+
   | Header row, column 1   | Header 2   | Header 3 | Header 4 |
   | (header rows optional) |            |          |          |
   +========================+============+==========+==========+
   | body row 1, column 1   | column 2   | column 3 | column 4 |
   +------------------------+------------+----------+----------+
   | body row 2             | ...        | ...      |          |
   +------------------------+------------+----------+----------+

Wordt:

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+

Of simpeler, maar beperkter:

.. code::

   =====  =====  =======
   A      B      A and B
   =====  =====  =======
   False  False  False
   True   False  False
   False  True   False
   True   True   True
   =====  =====  =======

Wordt:

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

Links
^^^^^

``http://url.com`` wordt http://url.com

```label <url>`_`` wordt `label <url>`_.

Als de link meerdere keren op de pagina wordt gebruikt, kun je de link en de doel definitie scheiden:

.. code::

   | Dit stukje bevat een `link`_.
   | En deze regel dezelfde `link`_.

   .. _link: http://url.com

Wordt:

| Dit stukje bevat een `link`_.
| En deze regel dezelfde `link`_.

.. _link: http://url.com

Plaatjes
^^^^^^^^

.. code::

   .. image:: imgs/plaatje.jpg

   .. image:: imgs/plaatje.jpg
      :height: 100px
      :width: 200 px
      :scale: 50 %
      :alt: alternate text
      :align: right

Waarbij het plaatje relatief ten opzichte van de ``source/`` directory staat.

Meer informatie
^^^^^^^^^^^^^^^

Meer gedetaileerde informatie over reStructuredText kun je vinden op http://docutils.sourceforge.net/rst.html.

Toevoegingen aan het template
-----------------------------

Scratch blokken gebruiken
^^^^^^^^^^^^^^^^^^^^^^^^^

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

Uitklapbaar element
^^^^^^^^^^^^^^^^^^^

Regelmatig worden Ninja's gestimuleerd om eerst zelf eens te proberen iets uit te vinden. Mocht het niet lukken,
dan kan er een voorbeeld worden open geklapt.

.. code::

   .. container:: toggle

      .. container:: header

          klik om voorbeeld te tonen

      .. code:: python

         def toon_voorbeeld:
           println('voorbeeld')


.. container:: toggle

   .. container:: header

      klik om voorbeeld te tonen

   .. code:: python

      def toon_voorbeeld:
        println('voorbeeld')


HTML genereren
--------------

Hoewel het HTML genereren zoveel mogelijk geautomatiseerd wordt uitgevoerd na het pushen van de reStructuredText, is het
handig om ook lokaal de HTML te genereren om te zien hoe het er uit ziet vóórdat het gepushed wordt.

Het commando om de HTML te genereren is:

.. code::

   sphinx-build -M html source/ build/

Op Ubuntu met `build-essential` geïnstalleerd, kun je ook shell-script `./make` gebruiken. Dit script verplaatst de
gegenereerde HTML naar de `docs/` directory, zoals gebruikt door GitHub. Ook maakt het een `.nojekyll` bestandje, zodat
GitHub er niet de Jekyll template engine probeert te gebruiken.