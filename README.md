[![DOI](https://zenodo.org/badge/791698287.svg)](https://doi.org/10.5281/zenodo.16631976)

# Code Publishing Tutorial

This repository contains a tutorial on code publishing created for the LMU Open Science Center.
It can be viewed online at <https://lmu-osc.github.io/code-publishing/>.

The tutorial pages are contained in the `*.qmd` files in the root folder.
All images are contained in the folder `images`.

## Previewing and rendering the tutorial

The tutorial is written in Markdown and uses [Quarto][quarto] to render it as a website.
To render the tutorial on your own computer, you need to have Quarto installed.

[quarto]: https://quarto.org/

Further, the R package [`renv`][renv] is used to track the project's dependencies.

[renv]: https://cran.r-project.org/package=renv

One can install `renv` as follows in R:

```r
install.packages("renv")
```

Then, also from within R, one can restore the dependencies tracked with `renv`:

```r
renv::restore()
```

While you are working on the tutorial, you can preview it as follows:

```sh
quarto preview
```

This will open the tutorial in your browser.
If you make any changes, the website will automatically reload.

If you are done editing and would like to render the tutorial to a static website,
run the following:

```sh
quarto render
```

## Contributing

If you are contributing to this tutorial,
please read the [contributing notes](CONTRIBUTING.md) before.

## License

Except where noted otherwise, the narrative text in this tutorial is licensed under [CC\ BY-SA\ 4.0][cc-by-sa];
the code without any narrative text is also (at your option) available under [CC0\ 1.0][cc0].

[cc-by-sa]: LICENSE-CC-BY-SA.txt
[cc0]: LICENSE-CC0.txt
