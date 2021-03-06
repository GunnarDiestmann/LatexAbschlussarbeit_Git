# Thesis Template for LaTeX

## Compiling

#### Prerequisites
- use of TeXmaker is recommended (all platforms)
- in order for `makeglossaries` to work, your latex installation folder must be added to `$PATH`
  - find out the folder: type `$ which latex` in console
  - add folder to `$PATH` (Linux):
    - in console: `$ PATH=$PATH:<latexpath>` (replace `<latexpath>`)
    - in TeXmaker: Options -> Configure TeXmaker -> "Add to path:" `<latexpath>`
  - install perl and added installation folder to `$PATH`
  - otherwise, you will get errors like `***Call to xindy failed***`
- if using TeXmaker: configure "makeglossaries" as user defined command
  - user -> user commands -> edit user commands
  - menuitem: `makeglossaries`; command: `makeglossaries %`

#### Compiling order
- either in console or in TeXmaker
  - `pdflatex thesis`
  - `bibtex thesis`
  - `makeglossaries thesis` (if using glossaries)
  - `pdflatex thesis`
  - `pdflatex thesis`
- or use latexmk
  - see http://ctan.org/pkg/latexmk (included in TeXLive and MiKTeX)
  - `latexmk -pdf` to generate the pdflatex
  - `latexmk -c` to delete the regeneratable files generated by latex and bibtex except pdf

## Other Information

#### Online References
- as webpages are not considered citeable, but sometimes pictures or sensor characteristics are taken from there, an
additional list is introduced; its use is neither comfortable nor obligatory, but its a way to avoid footnotes for
online references