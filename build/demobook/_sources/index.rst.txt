===============
Turtle graphics
===============

.. Here is were you specify the content and order of your new book.

.. Each section heading (e.g. "SECTION 1: A Random Section") will be
   a heading in the table of contents. Source files that should be
   generated and included in that section should be placed on individual
   lines, with one line separating the first source filename and the
   :maxdepth: line.

.. Sources can also be included from subfolders of this directory.
   (e.g. "DataStructures/queues.rst").

.. toc_version: 2

.. _t_o_c:

.. toctree::
  :numbered:
  :maxdepth: 2

  h1/toctree.rst
  h2/toctree.rst
  h3/toctree.rst

Inleiding
:::::::::

.. rubric:: Leer programmeren met de tekenschildpad

In deze cursus maak je kennis met de tekenschildpad: de *turtle*.
Deze kun je via je programma's opdrachten geven om te tekenen.
Je maakt mooie figuren en leert intussen de beginselen van het programmeren.

Je ziet hieronder al een eerste voorbeeld.
Je hoeft het programma nog niet te begrijpen - geniet eerst maar van de ijverige schildpad.
Door op de knop "Run" te klikken voer de schildpad het programma uit.

.. activecode:: ch03_1
    :tour_1: "Overall Tour"; 1-6: Example01_Tour01_Line01; 3: Example01_Tour01_Line02; 4: Example01_Tour01_Line03; 5: Example01_Tour01_Line04; 6: Example01_Tour01_Line05;
    :tour_2: "Line by Line Tour"; 1: Example01_Tour02_Line01; 2: Example01_Tour02_Line02; 3: Example01_Tour02_Line03; 4: Example01_Tour02_Line04; 5: Example01_Tour02_Line05; 6: Example01_Tour02_Line06;
    :nocodelens:

    import turtle               # allows us to use the turtles library
    wn = turtle.Screen()        # creates a graphics window
    alex = turtle.Turtle()      # create a turtle named alex
    alex.forward(150)           # tell alex to move forward by 150 units
    alex.left(90)               # turn by 90 degrees
    alex.forward(75)            # complete the second side of a rectangle
