# Frequently Asked Questions (FAQ)

### Where do I find these documents?

See [document-list](document-list.md)

### How do you write "collaboratively"?

We use LaTeX to write documents and Git to synchronize them across our machines.

### How can I help?

See [contributing](contributing.md)

### What is LaTeX?

In short: LaTeX (read as LAH-tekh or LAY-tekh) is a software *to typeset documents* built on top of TeX, a tool originally written by Donald Knuth a long time ago. LaTeX works like a compiler, documents are written in plain text with a declarative structure and then compiled into pdf, postscript or dvi using a tool like xelatex, lualatex or pdflatex.

### How is LaTeX different from something like Microsoft Word?

Microsoft Word and similar software such as LibreOffice or Pages are *word processors*, and not really typesetting systems although they all can typeset nice documents if you put in the effort. The main difference is in the workflow. To write a file in MS Word, you need to have word installed, because only it can open its documents.

LaTeX on the other hand is just a plain text document, you can use whatever software you like to write it using a declarative syntax and then you feed the document to the "compiler" once you're done writing. The advantage is that the LaTeX compiler is quite smart and can create a very good looking document with relatively low effort (once you learn the syntax), on the contrary a low effort document produced from a word processor usually looks very bad, especially for difficult to typeset texts like maths.

### Can I use LaTeX?

Of course, LaTeX is completely free! To install LaTeX see [tutorials/install-latex](./tutorials/install-latex.md), then you may want to look into [tutorials/first-latex-document](./tutorials/first-latex-document.md) to learn to write your first document.

TODO: merge previous resources such as HSR-Stud/HowTo

### How do I do *X* in LaTeX?

TODO: Link to tutorials and contact infos.

### What is Git?

[Git](https://git-scm.org) is a *distributed version control system*, which means: a tool to synchronize your documents and at the same time keep track of how they changes over time. You can find a ton of resources online and more in [tutorials/install-git](./tutorials/install-git.md)

### What is Github?

The tool Git synchronizes documents between many computers, and although not strictly necessary, there is usually one computer that acts as the *origin* or "central server". Github is a service that offers that, a place to put your documents that everyone can easily reach from anywhere (plus some other things, like an issue tracker, ...).

### What is Travis CI?

CI stands for *Continuous integration* and Travis is Github's CI product. Continuous integration for our purposes is a computer, kindly offered by Github, that automatically compiles our LaTeX sources, to check for its correctness and to publish them as PDFs for those who don't have LaTeX installed on their computers. To set up Travis for your document see [tutorials/setup-travis](./tutorials/setup-travis.md).
