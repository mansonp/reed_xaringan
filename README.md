# reed_xaringan

Minimalist `R` xaringan theme for html presentations using Reed style/colors.

Reed style guide a [https://www.reed.edu/public-affairs/assets/downloads/reed-graphic-standards.pdf](https://www.reed.edu/public-affairs/assets/downloads/reed-graphic-standards.pdf).

## Example Title Slide

Here is the title slide:

![img/ex/titleslide.png](img/ex/titleslide.png)

## Full Example Presentation

Example presentation at [https://mansonp.github.io/reed_xaringan/]( https://mansonp.github.io/reed_xaringan/). 

## Usage

just fork this and edit the front-matter YAML at the start of your Rmd file containing your presentation.


```
---
title: "your title"
subtitle: "subtitle"
author: "Your name"
date: "`r Sys.Date()`"
output:
  xaringan::moon_reader:
    lib_dir: libs
    css: [default, "reed.css", "reed-fonts.css"]
    nature:
      beforeInit: ["../js/ru_xaringan.js"]
      highlightStyle: github
      highlightLines: true
      countIncrementalSlides: false
      ratio: "16:9"
    includes:
      in_header: "./libs/partials/header.html"
---
```

## Offline Usage

* One big drawback is (used to be) that HTML presentations require a working internet connection during the presentation. 
* It's not always possible to guarantee that. Sigh.
* There is a great alternative/backup. Just print the HTML slides to PDF with [decktape](https://github.com/astefanutti/decktape)! I.e. you do

    ```
    decktape index.html presentation.pdf --chrome-arg=--disable-web-security
    ```
    to end up with this [PDF](presentation.pdf)

