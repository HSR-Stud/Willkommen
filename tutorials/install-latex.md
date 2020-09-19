# Install LaTeX

*You may be interested in the [LaTeX Workshop](https://github.com/openhsr/LaTeX-Workshop) organized by OpenHSR.*

## Introduction (what do I need?)

To use LaTeX, you need 3 things: A text editor, a PDF viewer, and a (La)TeX compiler. For each of the three, there are many options to choose from. Note that a LaTeX *distribution* usually comes with all of the 3 in a single package (plus some extras).

For the editor and the PDF viewer, you can use literally anything, but the experience is nicer when the editor has syntax highlighting and compiler integrations for LaTeX and the PDF viewer supports *SyncTex*. For example a bad combo would be Notepad + Adobe PDF viewer, whereas a good one could be TeXWorks (has both an editor and viewer), MS VS Code with a plugin, or Vim + Zathura (you may want to look into [the tools sections in the resources document](../resources.md).

LaTeX compilers are discussed below.

## LaTeX2e distribution

We need to know a bit of history in order to avoid confusion later on. I'll keep it short I promise.

  - A (long) while ago Donald Knuth wrote the first version of this software, and was called *TeX*
  - TeX was rather difficult to use so one day Leslie Lamport, wrote another software on top of TeX, a kind of extension, and decided to name it *LaTeX*
  - This means that one can write TeX code inside a LaTeX document because LaTeX is built op top of TeX, but it is generally considered bad practice
  - This was in 1984 (a long time ago)
  - Time went on and LaTeX became the standard for academic papers
  - In the 2000's many people wanted to fix some old nasty problems (mainly UTF-8 support) that the original TeX and LaTeX had, so they decided to rewrite most of the software thus creating
    - XeTeX and with it XeLaTeX in 2004 and
    - LuaTeX and LuaLaTeX in 2007

Today the situation is that we have

  - the very old language *TeX* and the tool *pdftex*
  - the improved language of *LaTeX* and an tool called *pdflatex*
    - Actually, LaTeX is being kept updated, the current version is known as *LaTeX2e*
  - two newer implementations of *LaTeX* (each with some extensions)
    - XeLaTeX
    - LuaLaTeX

## Get an editor or IDE

