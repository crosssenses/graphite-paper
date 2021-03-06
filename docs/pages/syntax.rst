========
 Syntax
========

WORKING FILE:

https://docs.google.com/spreadsheets/d/1bp6Y3C1jGtIH9GvygYurikihPT6EIarLHO20KirznWM/edit#gid=0


Markdown for text
-----------------

Blank lines divide logical blocks (e.g. paragraphs including asides).

Example for markdown:

.. code-block:: md

    # Markdown

    This an *bold* example with a bullet list:

    * one
    * two
    * three

Further resources on markdown

-  https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
-  https://guides.github.com/features/mastering-markdown/
-  https://github.github.com/gfm/


Graphite specific plugins and markup
------------------------------------

Inline elements
^^^^^^^^^^^^^^^



**(1) Import external markdown file or plugin**

::

    :--- test.md ---:

or

::

    :--- PLUGIN | config.yaml ---:

**(2) Plugin within the text**

::

    :--- PLUGIN ---:
    param1: abc
    param2: xyz
    param_list:
      - a1
      - b2
      - c3
    :--------------:

**(3) Add one or more paragraph-wide side-notes**

::

    Lorem impsum und so weiter
    :--- NOTE ---:
    First side note
    :--- NOTE ---:
    Second side note
    :------------:

**(4) Add a side note, which is linked to a word (foot-note-style)**

::

    Lorem ipsum [: NOTE | test :] und so weiter
    :--- NOTE | test ---:
    Here we go…
    :-----------------:

--------------



Objects are defined as yaml objects
-----------------------------------

::

    Lorem ipsum dolor[: NOTE:test :] sit amet
    sdfasdsd
    :--- NOTE:test ---:
    This is a test note
    :-----------------:

    Or as stand-alone objects:

    :------------------- CODE ----------------------:
    class Test:
        def __init__(self, name):
            self.name = name
    :-----------------------------------------------:

External files
--------------

::

    :--- file.md ---:

    :--- PLUGIN:file.yaml ---:

Marginal notes
--------------

Marginal notes can have multiple origins. They can be extracted from the
markdown (e.g. footnotes or glossary entries) – syntax to be determined.

Marginal notes concerning the entire paragraph can be separated by three
dashes. Example:

.. code:: md

    This is a paragraph
    :--- NOTE ---:
    First marginal note
    :--- NOTE ---:
    Second marginal note for the same paragraph
    :------------:



