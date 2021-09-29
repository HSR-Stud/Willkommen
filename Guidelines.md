# General LaTeX Guidelines

*Most documents are quite old and do terrible typetting, here are some common mistakes.*

## Absolute Basics (to not ruin the typesetting)

### Text and structure

1. Avoid using `\\` (line breaks) at all costs except where it is part of the syntax (for ex. in `tabular`). You should instead leave *an empty line* to break a paragraph.  
    Don't:  
    ```latex
    This is my first paragraph. \\
    This is my second paragraph.
    ```  
    Do:
    ```latex
    This is my first paragraph.

    This is my second paragraph.
    ```

2. Never use old macros `\bf`, `\it`, `\em` to change the font weight or shape, use `\textbf{}`, `\textit{}`, `\emph{}`. That is because `{\bf {\it ...}}` is **not** bold italic, whereas `\textbf{\textit{...}}` is. If you really need to use `\bf`, or `\it` use `\bfseries` resp. `\itshape` instead.  
    Don't:  
    ```latex
    I want to change the {\bf {\it style of this part}}
    ```  
    Do:  
    ```latex
    I want to change the \textbf{\textit{style of this part}}
    ```  
    All font specs are 
      - `\bfseries` bold, `\mdseries` medium, `\lfseries` light,
      - `\upshape` upright, `\itshape` italic, `\slshape` slanted, `\scshape` smallcaps, 
      - `\rmfamily` serif, `\sffamily` sans-serif, `\ttfamily` typerwriter

3. Avoid manually styling your document, i.e. avoid using `\textbf{}` (bold), `\textit{}` (italic), etc. for emphasis use `\emph{}` (emphasis) instead.  
    Don't:  
    ```latex
    I want \textbf{this part} of the sentence to stand out
    ```  
    Do:  
    ```latex
    I want \emph{this part} of the sentence to stand out
      ```  
    Why? Because `\emph{}` switches the shape correctly, for example if the text is already in emphasis, then the next emphasis will be upright, i.e. `\emph{... \emph{...}}` works, whereas `\textit{... \textit{...}}` doesn't.

4. Avoid manually styling your document, *bis*. Do not use `\textbf` and co. to build paragraph titles, section headings or anything similar. There are some appropriate constructs for that:
    - Numbered headings `\part`, `\chapter`, `\section`, `\subsection`, `\subsubsection`, `\paragraph` ...
    - Unnumbered headings `\section*`, `\subsubsection*`, ...

    And they can be configured using the [titlesec](https://ctan.org/pkg/titlesec) package.  
    Don't:  
    ```latex
    % NEVER do this
    \textit{\textsf{My custom heading}} \\[1em]
    ```
    Do:
    ```latex
    % in the preamble
    \usepackage{titleset}

    \titleformat{\paragraph}[hang]
      {\normalfont\itshape\sffamily}{\theparagraph}{1em}{}

    % later in the document
    \paragraph{My custom heading}
    ```

4. Let LaTeX decide where to put floatings, it generally results in a nicer typeseting. To refer to figures use references in captions.  
  Don't:  
    ```latex
    ... as in the figure below ...
    \begin{figure}[h!] % or table
      % ...
    \end{figure}
    ... in the figure above ...
    ```  
    Do:
    ```latex
    ... as in figure \ref{fig:that-figure}.
    \begin{figure} % or table
      % ...
      \caption{
        Meaningful description
        \label{fig:that-figure}
      }
    \end{figure}
    ... in figure \ref{fig:that-figure} ..
    ```
### Mathematics

5. Do not use `$` and `$$`. These are old TeX macros and will f\*ck up the spacing.  
    Don't: 
    ```latex
    $$ \gamma = \alpha + j\beta $$
    ```  
    Do:
    ```latex
    \[ \gamma = \alpha + j\beta \]
    ```



7. Avoid using nested `\include`. This makes debugging terribly hard and should be used only for **very** large documents such as books, or dissertations (not your case!). Generally keep a somewhat flat directory structure.

## Make your markup readable (for future users)
