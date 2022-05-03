```latex
\newenvironment{amatrix}[1]{%
  \left(\begin{array}{@{} *{\numexpr#1-1}{c} | c @{}}
}{%
  \end{array}\right)
}

```



$$


\begin{amatrix}{r|}
1 & 2 & 2
\end{amatrix}



\begin{amatrix}{cc|c}
  1 & 2 & 3 & a\\
  4 & 5 & 9 & a
\end{amatrix}



$$