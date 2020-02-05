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
  :maxdepth: 3

  h1/toctree.rst
  h2/toctree.rst
  h3/toctree.rst  

SECTIE 1: Inleiding
:::::::::::::::::::

.. rubric:: Leer programmeren met de tekenschildpad

In dit boek maak je kennis met de tekenschildpad: de *turtle*.
Deze kun je via je programma's opdrachten geven om te tekenen.
Je maakt mooie figuren en leert intussen de beginselen van het programmeren.

Je ziet hieronder al een eerste voorbeeld.
Je hoeft het programma nog niet te begrijpen - geniet eerst maar van de ijverige tekenschildpad.
Door op de knop "Start" te klikken voer de schildpad het programma uit.

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




This is just a sample of what you can do.  The index.rst file is the table of contents for your entire project.  You can put all of your writing in the index, or  you can include additional rst files.  Those files may even be in subdirectories that you can reference using a relative path.


::


   .. toctree::
      :maxdepth: 2

      some/path/myfile.rst


Section 2: Links
::::::::::::::::

Runestone uses the ``restructuredText`` (rst) markup language.  We chose this over markdown largely because rst is extensible.  Nearly all of the basic markup tasks are already handled by restructuredText.  You should check out the docs for the basics of restructuredText (link below). Our extensions are all for the interactive elements.  One key hint about restructuredText:  Its like **Python** -- *indentation matters!*

* `restructuredText Docs <http://docutils.sourceforge.net/rst.html>`_
* `Runestone Docs <https://runestone.academy/runestone/static/authorguide/index.html>`_
* Join the discussion on our `Google Group <https://groups.google.com/forum/#!forum/runestone_instructors>`_
* Tell us about problems on `Github <https://github.com/RunestoneInteractive/RunestoneComponents>`_



SECTION 3: Sample Directives
::::::::::::::::::::::::::::

ActiveCode
----------

.. activecode:: codeexample1
   :coach:
   :caption: This is a caption

   print("My first program adds a list of numbers")
   myList = [2, 4, 6, 8, 10]
   total = 0
   for num in myList:
       total = total + num
   print(total)

Multiple Choice
---------------

.. mchoice:: question1_2
    :multiple_answers:
    :correct: a,b,d
    :answer_a: red
    :answer_b: yellow
    :answer_c: black
    :answer_d: green
    :feedback_a: Red is a definitely on of the colors.
    :feedback_b: Yes, yellow is correct.
    :feedback_c: Remember the acronym...ROY G BIV.  B stands for blue.
    :feedback_d: Yes, green is one of the colors.

    Which colors might be found in a rainbow? (choose all that are correct)

These are just two of the many interactive components for writing online course materials.  You can see examples of all of them `On our Example Page <http://interactivepython.org/runestone/static/overview/overview.html>`_

Now feel free to modify this file to start creating your own interactive page.


Section 4: Theme
:::::::::::::::::::

You can override the style rules in the default theme by adding css rules to a file named **theme-overrides.css** (the filename is important - this will replace an existing file). Make sure the file's directory is part of the ``html_static_path``. You can do so by placing it in a folder **_static**, then modifying ``html_static_path`` in conf.py to include that folder:

.. code::
    html_static_path =  runestone_static_dirs() + ['_static']


If you want to do more significant changes to the theme, you should copy the files in the runestone/common/project/template/sphinx_bootstrap to a directory like ``_templates/my_theme``. Then make sure these values are set in conf.py:

.. code::

    html_theme_path = ["_templates"]
    html_theme = 'my_theme'
