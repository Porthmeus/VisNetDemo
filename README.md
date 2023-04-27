# How to use the repository

The repository contains the files which creates the `visNetDemo.html` file - this is a [reveal.js](https://revealjs.com/) slide presentation and should be displayed by your browser. However it is not self contained, thus you would need to do the following to open it.

```
git clone https://github.com/Porthmeus/VisNetDemo.git
```

After that navigate to the cloned directory and open `visNetDemo.html`.


# Changing and recompiling

The source code for the slide show is written in RMarkdown and can be found in the `visNetDemo.Rmd` file. If you want to modify it and recompile it, you need to install the *rmarkdown* and *revealjs* package for R and pandoc must be in your path.

```
sudo apt-get install pandoc
Rscript -e 'install.packages(c("rmarkdown","revealjs"))'
```



A small introduction how to write RMarkdown for reveal.js can be found [here](https://bookdown.org/yihui/rmarkdown/revealjs.html). To compile the slide show run:

```
Rscript -e 'rmarkdown::render("./visNetDemo.Rmd", output_dir = ".")'
```
