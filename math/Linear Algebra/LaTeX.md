```latex
\newenvironment{amatrix}[1]{%
  \left(\begin{array}{@{} *{\numexpr#1-1}{c} | c @{}}
}{%
  \end{array}\right)
}

```



$$

\newenvironment{amatrix}[1]{%
  \left(\begin{array}{@{} *{\numexpr#1-1}{c} | c @{}}
}{%
  \end{array}\right)
}

\begin{amatrix}{cc|c}
  1 & 2 & 3 & a\\
  4 & 5 & 9 & a
\end{amatrix}

\begin{amatrix}{ccc|c}
  1 & 2 & 3 & a\\
  4 & 5 & 9 & u & a
\end{amatrix}

$$

ㅇ띄어쓰기
```LaTeX
	f
	\,     space
	\;     double space
	\quad  tab
	\qquad double tab
```
$$
	f
	\,     space
	\;     double space
	\quad  tab
	\qquad double tab
	$$