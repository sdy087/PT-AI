USING LATEX TO PREPARE A CHAPTER FOR THE PT-AI PROCEEDINGS

The contents of this package were prepared by
    Aaron Sloman
    http://www.cs.bham.ac.uk/~axs
    Email: a.sloman@cs.bham.ac.uk

as part of the process of preparing a contribution for the volume.

The Springer style files used unchaged are svmult.cls and spbasic.bst

I found some of the instructions and samples confusing, ambiguous or incomplete, so I
set up a test directory in which I tried to get a modified version of the latex
sample files to work using Latex on a linux machine running Fedora 19 with the latex
texlive/pdflatex/bibtex libraries. This has also been tested on two other machines.

In order to conform to the instructions for formatting citations and references given
here
    http://www.pt-ai.org/2013/submission

namely

    We will use the Author-Date style "Springer SocPsych" for references.

I found it necessary to use only these two style files from the author 'styles'
package:

    spbasic.bst
        Bibliography style file left unchanged, and invoked in the author source file
        ( pt-ai-author.tex ) as

        \bibliographystyle{spbasic}

    svmult.cls
        This should be re-named if edited, and invoked with the new name.

        This is invoked in pt-ai-author.tex by heading for the file:

            \documentclass[graybox]{svmult}

    Note that the use of [graybox] is not essential for the PT-AI volume, though
    I have left an example in the author latex file.

    In order to use graybox you may have to fetch the texlive-framed package.
    It may be simpler just to remove 'graybox' from the header. I.e. use

            \documentclass[]{svmult}

    The Springer file referenc.tex provided some pre-compiled index entries
    in the wrong format for the PT-AI volume, so I transferred some of that
    file to the body of the pt-ai-author.tex file and the bibliography
    entries in bibtex format here:

        author.bib

    This is invoked near the end of the pt-ai-author.tex file in the command:

        \bibliography{author}

    The springer template files provided an image file figure.eps. However
    that does not work with the pdflatex command so I produced a converted
    version figure.pdf. The .eps graphic file is used if the 'latex' command
    is used. Otherwise, if the 'pdflatex' command is used the .pdf graphic
    file is used.

Files provided here:

    AREADME.txt
        This file.

    figure.eps
    figure.pdf
        Two versions of the figure file.

    author.bib
        File with references, in format required by Bibtex.
        Copy and edit to create you references.

    pt-ai-author.tex
        Template author file: copy and edit, then run

            pdflatex pt-ai-author
            bibtex pt-ai-author
                (should create author.bbl file)
            pdflatex pt-ai-author
            pdflatex pt-ai-author

and once more for luck!
            pdflatex pt-ai-author
                (Should create the pt-ai-author.pdf file to be
                used for your chapter.)

    Other files included:

    pdf/pt-ai-author.pdf

        sample output of pdflatex created using this
        procedure.

    pt-ai-author.bbl
        output of 'bibtex' command.

Springer files included for simplicity of testing:

    spbasic.bst
    svmult.cls

May be needed. Not yet used. May be needed for creating an index.

    svind.ist
    svindd.ist

Before you see this, this file should have been checked by

    Vincent Müller, PT-AI Chair, and editor of the book.

Aaron Sloman
25 Nov 2013
