CIC-style
=========

Definição de estilos para LaTeX para uso no [CIC/UnB](https://www.cic.unb.br/).

CICflowchart
------------

Estilo para elaboração de fluxogramas usando [Tikz](http://sourceforge.net/projects/pgf/).

Exemplo:

    \begin{tikzpicture}[node distance=3em]
        \node[startstop] (1) {Início};
        \node[decision, below of=1, yshift=-3em] (2) {Condição verdadeira?} edge[from] (1);
        \node[process, below of=2, yshift=-3em] (3) {Ação 2};
        \node[process, right of=2, xshift=6em] (4) {Ação 1};
        \node[startstop, below of=3] {Fim} edge[from] (3);
        \draw [to] (2) -- node[anchor=east] {não} (3);
        \draw [to] (2) -- node[anchor=south] {sim} (4);
        \draw [from] (3) -| (4);
    \end{tikzpicture}}
    

CIClistings
-----------

Estilo para apresentação de código usando [listings](http://www.ctan.org/pkg/listings).
São definidos 3 estilos:

* _CIC-style_ (padrão)
* _C-code_ (para código C)
* _pseudo-code_ (para pseudocódigo)

Exemplo:

    \begin{lstlisting}[style=C-code]
    #include <stdio.h>
    int main() {
        printf("Hello world!");

        return 0;
    }
    \end{lstlisting}

CIC
---

Incorporação de _CICflowchart_ e _CIClistings_ para uso com a classe 
[UnBeamer](https://github.com/gnramos/UnBeamer).