# Contributing Notes

There are some things to consider when contributing to this repo:

- make screenshots in high resolution
  by temporarily increasing the font scaling factor in your OS
  and using a large display
- limit the width of images and center them, for example, as follows:
  
  ```md
  ![](images/my_image.png){width=500px fig-align="center"}
  ```
- annotate code blocks with `filename="Terminal"` and`filename="Console"`
  to differentiate Bash and R that should be entered by the user
  (if there is no file from which the code is an excerpt)
- Put optional content into a collapsed note
- Put important content into warning
- hierarchy of callouts
  - note
  - tip
  - caution
  - warning
  - important
- headings (including tabset tabs and callout titles) are written in title case
- on any page, start headings at level 2 (i.e., use `##`) and above
  because the page title is already at level 1
- maintain the hierarchy of headings, that is,
  only create headings at level `n` if there's already a heading at level `n-1`
- also maintain the hierarchy of headings for callouts:
  callouts use heading levels that are one below the current heading level
- R package names are typeset in `monospace`
- Prefer R packages that follow the [tinyverse](https://www.tinyverse.org/) philosophy,
  that is, have a lightweight dependency footprint.
  All packages need to be downloaded by `renv` and (worst case) compiled during the tutorial,
  which better not take too long.
  Use `pak::pkg_deps()` to count the total number of package dependencies.
- Write license abbreviations with [no-break spaces][no-break-space]
  (e.g., write `CC\ BY\ 4.0` rather than `CC BY 4.0`)
- When writing markdown:
  - use [semantic linefeeds][semantic-linefeeds] to ease change tracking,
    except for exact quotes (as they won't be updated)
    and for example code in code blocks
    (to allow for wrapping on the website as required by the user's screen width)
  - use [regular footnotes][regular-footnotes] rather than [inline footnotes][inline-footnotes]
    to increase the readability of markdown
    (except for short notes or at the end of lines)
  - use [reference links][reference-links] rather than [inline links][inline-links]
    to increase the readability of markdown
    (except for short links or at the end of a line)
- If the (R package/system) dependencies that are required to work through the tutorial change,
  make sure to adjust the respective section in `make_readme.qmd` accordingly.
- When making significant contributions,
  add people to the `CITATION.cff` file and mention them in `about.qmd`.
- keep usage of terms consistent, for example:
  - always write _data dictionary_ or always write _codebook_ (but don't mix)
    - in the case of this tutorial, the convention is to write _data dictionary_
  - always write _data set_ or always write _dataset_ (but don't mix)
    - in the case of this tutorial, the convention is to write _data set_

[no-break-space]: https://pandoc.org/MANUAL.html#extension-all_symbols_escapable:~:text=A%20backslash%2Descaped%20space%20is%20parsed%20as%20a%20nonbreaking%20space.
[semantic-linefeeds]: https://rhodesmill.org/brandon/2012/one-sentence-per-line/
[regular-footnotes]: https://pandoc.org/MANUAL.html#extension-footnotes
[inline-footnotes]: https://pandoc.org/MANUAL.html#extension-inline_notes
[reference-links]: https://pandoc.org/MANUAL.html#reference-links
[inline-links]: https://pandoc.org/MANUAL.html#inline-links
