# shogi_typesetting
A set of LaTeX macros (not a package) to typeset shogi articles.

## Commands
``\imgmed``

This is to create a medium sized, centred board diagram. The default sizes are based on the output of https://shogi.zukeran.org/shogi-draw/. 

Sample Usage:

``
\imgmed{''The Attack Rolls in Like a Sudden Tide''}{diagram1}
``

Parameter 1: Caption, placed above the image \
Parameter 2: diagram filename

``\imgsmall``

A small-sized image, **not** automatically centred. For use in a 2 column format (see next). 

``\sidebyside``

A two column format, intended for board diagrams to be 'side by side' with commentary/analysis. The two parameters are the contents of the first and second columns, respectively.

Sample Usage:

``
\sidebyside{\imgsmall{caption}{filename}}{\colpara{analysis}}
`` 

``\colpara``

This is another custom command. It generates an unindented paragraph, followed by extra space. See above for usage. It's not necessary to have paragraphs in a column unindented, but in my opinion it looks nicer.

## Environments
There are two custom environments in this set of macros. Both generate a table of moves: ``chessmoves`` generates chess-style movenumbering (1 move = 1 move by each player), \
and ``shogimoves`` generates shogi-style numbering (1 move = 1 move by one player).
Each environment has its own command to generate each move.

### ``chessmoves``

``
\begin{chessmoves}
\cm{Nf3}
\end{chessmoves}
``

### ``shogimoves``

``
\begin{shogimoves}
\sm{G'22}
\end{shogimoves}
``
