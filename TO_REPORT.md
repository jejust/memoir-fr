# Corrections to report to Memoir's maintainer

- "occured" --> "occurred".
- "authorative" --> "authoritative".
- "comming" --> "coming".

- Add the bib entry:
```
\bibitem[Gra07]{GRATZER07}
  George Grätzer.
  \newblock \emph{\textsl{More} math into LaTeX}.
  \newblock Springer, 2007.
  \newblock ISBN 978--387--32289--6.
```
and cite it near the string `\textit{Math into \ltx}`.

- in `memsty.sty`, add:
```
\providecommand\CTANpkg{}
\AtBeginDocument{
  \@ifpackageloaded{hyperref}{
    \renewcommand*\CTANpkg[1]{\href{http://ctan.org/pkg/#1}{\nolinkurl{/pkg/#1}}}
  }{
    \renewcommand*\CTANpkg[1]{\url{/pkg/#1}}
  }
}
```
and use it for packages refered as \CTANpkg{/pkg/...})


- In bibitem `IMPATIENT`, replace
```
  \newblock (Available at
             \url{ftp://tug.org/tex/impatient})
```
with
```
  \newblock (Available at
             \CTANpkg{impatient})
```




## Maybe:

- in the bibligraphy, the UK FAQ URL should be "https://texfaq.org/".
