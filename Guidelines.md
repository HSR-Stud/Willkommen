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
    \usepackage{titlesec}

    \titleformat{\paragraph}[hang]
      {\normalfont\itshape\sffamily}{\theparagraph}{1em}{}

    % later in the document
    \paragraph{My custom heading}
    ```

5. Let LaTeX decide where to put floatings, it generally results in a nicer typeseting. To refer to figures use references in captions.  
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

6. **Do not use minipages**. Just don't use them. They make your document look ugly if you don't know what you're doing (and I bet you don't know what you're doing). If you need to make things compact use something like [`multicol`](https://www.overleaf.com/learn/latex/Multiple_columns).


### Mathematics

1. Do not use `$` and `$$`, use `\(..\)` and `\[ .. \]` instead. The former are old TeX macros and will f\*ck up the vertical spacing.  
    Don't: 
    ```latex
    $$ \gamma = \alpha + j\beta $$
    ```  
    Do:
    ```latex
    \[ \gamma = \alpha + j\beta \]
    ```

2. Use `\text{}` when you have words or sentences in math mode. `\textbf{}` etc. are also available, and will fix the spacing between words.  
    Don't:
    ```latex
    \[
      % this will look very ugly
      Accelleration = \frac{Force}{Mass}
    \]
    ```
    Do:
    ```latex
    \[
      \text{Accelleration} = \frac{\text{Force}}{\text{Mass}}
    \]
    ```


## Make your it readable (for future contributors)

1. Avoid using nested `\include`. This makes debugging terribly hard and should be used only for **very** large documents such as [books](https://github.com/AndreasFMueller/SeminarMatrizen), or dissertations (not your case!). Generally keep a somewhat flat directory structure.

2. Make the source code of your formulas readable, add spaces and break lines so that you can make sense of what will be typeset. Which of the two code snips below do you find more understandable?  
    Don't:
    ```latex
    \[
      \int_\mathcal{C}f(\vec{r})\,d\ell=\int_\mathcal{C}f(\vec{r})\,|d\vec{r}|=\int_a^bf(\vec{r}(t))|\vec{r}'(t)|\,dt.
    \]
    ```
    Do:
    ```latex
    \[
      \int_\mathcal{C} f(\vec{r}) \,d\ell 
      = \int_\mathcal{C} f(\vec{r}) \,|d\vec{r}|
      = \int_a^b f(\vec{r}(t)) |\vec{r}'(t)| \, dt .
    \]
    ```

### Suggestion for indentation

LaTeX is very weird at first, because on one hand it feels like a programming language where indentation should be mandatory, but on the other hand it kinda isn't. Here I have some (opinionated) suggestions to make indentation in your LaTeX sources consistent.


1. Use an indentation of 2 spaces. This is because you can get many nested expressions. You could go with 4, but keep in mind that you will need a wider screen.

2. Indent only `\begin{...} \end{...}` blocks and open parenthesis `()` brackets `[]` or braces `{}`. Example:  
    ```latex
    \begin{table}
      \begin{tabular}{l l}
        \toprule
        % ...
      \end{tabular}
      \caption{
        A decently indented table.
        \label{tab:another-table}
      }
    \end{table}
    ```
    Another example for maths:
    ```latex
    \[ % yes these count as brackets
      y = \bar{y} \pm \sigma_y
        \approx f(\bar{\vec{x}}) \pm \sqrt{\sum_{i=1}^m \left( % and these as well
          \partial_{x_i} f(\bar{\vec{x}}) \sigma_{x_i}
        \right)^2}
    \]
    ```

3. The only exception is `\begin{document}` and `\end{document}`, which should not be indented. **This is the only exception**. The reasoning behind this is that (unless you use `\include`) everything will be be indented which is not very useful.

4. Section headings etc. do not cause indentation. You should think of these macros as just putting there the title, not as a block.
    ```latex
    \section[VHSIC Hardware Description Language (VHDL)]{
      VHDL: Very high-speed integrated circuits program
      Hardware Description Language
    }

    \subsection{Basic syntax and identifiers}

    In VHDL an identifier is a case insensitive string composed of \texttt{A-Z a-z 0-9 \_} that
    \begin{itemize}
      \item is not a keyword,
      \item does not start with a number or \texttt{\_},
      \item does not have two or more \texttt{\_} in a row.
    \end{itemize}
    ```

5. Align tables to the `&`, if the content is short. For example
    ```latex
    \begin{table}
      \centering
      \begin{tabularx}{\linewidth}{>{\ttfamily}c l X}
        \toprule
        \textrm{Value} & Meaning & Usage \\
        \midrule
        U & Uninitialized  & In the simulator \\
        X & Undefined      & Simulator sees a bus conflict \\
        0 & Force to 0     & Low state of outputs \\
        1 & Force to 1     & High state of outputs \\
        Z & High Impedance & Three state ports \\
        W & Weak Unknown   & Simulator sees weak a bus conflict \\
        L & Weak Low       & Open source outputs with pull-down resistor \\
        H & Weak High      & Open drain output with pull-up resistor \\
        - & Don't care     & Allow minimization \\
        \bottomrule
      \end{tabularx}
      \caption{
        Possible values for \vhdl{std_logic} signals.
        \label{tab:std-logic-1164-types}
      }
    \end{table}
    ```
    If the cells have text that is too long (> 100 characters) put a cell on each line, and leave an empty line between rows.
    ```latex
    \begin{tabularx}{\linewidth}{m{10cm} X}

      \textbf{Produktregel} \newline \(k\) Positionen m\"ussen unabh\"angig von einadner markiert werden, wobai \(n_i\) verschiedene Markierungen zur Verf\"ugung stehen.
      & \(\displaystyle n_1 n_2\cdots n_k = \prod_{i=1}^k n_i \)
      \\

      \textbf{Permutation} \newline Auf wie viele Arten lassen sich \(n\) verschiedene Objekte anordnen?
      & \(\displaystyle P_n = n(n-1)(n-2)\cdots1 = n! \)
      \\

      \textbf{Kombination} \newline Auf wie vielen Arten kann man \(k\) aus \(n\) verschiedenen Objekte ausw\"ahlen?
      & \(\displaystyle C_n^k = {n \choose k} = \frac{n!}{k!(n-k)!}\)
      \\

      % ...
    \end{tabularx}
    ```
