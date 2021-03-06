# nzGREENGridDataR
Code to process data from the [NZ GREEN Grid](https://www.otago.ac.nz/centre-sustainability/research/energy/otago050285.html) project.

[NZ GREEN Grid](https://www.otago.ac.nz/centre-sustainability/research/energy/otago050285.html) data includes:

 * 1 minute electricity power (W) data for c 40 households in NZ monitored from early 2014 using [gridSpy](https://gridspy.com/) monitors on each power circuit (and the incoming power)
 * Occupant time-use diaries (focused on energy use)
 * Dwelling & appliance surveys

NB: *None* of the data is held in this [repo](https://github.com/dataknut/nzGREENGridDataR) so *none* of the code here will work unless you also have access to the data. 

----

## About

The code in this [repo](https://github.com/dataknut/nzGREENGridDataR) does two things:

 * Data processing and reporting:
    - processes the original data to a 'safe' form for archiving and third party re-use (code will only work if you have the original data). As it does so it creates two check plots for each household: monthly mean power profiles & the number of observations over time
    - produces original data processing reports (code will only work if you have the original data)
    - produces cleaned 'safe' data reports (code will work on the archived 'safe' data)
 * Provides examples of code to:
    - extract 'Heat Pump' profiles from the 'safe' data between two dates
    - link the household survey and extracted 'Heat Pump' data for analysis

Guide to folders:

 * data - misc data (not the research data)
 * checkPlots - data quality/check plots for each household produced during processing
 * dataProcessing - r scripts to process data and generate data quality reports
 * examples - r script examples to use on the clean 'safe' data
 * includes - .Rmd files use in report generation
 * man - r package documentation (auto-created using [roxygen](https://cran.r-project.org/web/packages/roxygen2/))
 * R - r code implementing the package functions
 * docs - data quality reports published via [githhub pages](https://dataknut.github.io/nzGREENGridDataR/)
 
## Data Access

A link to the archived 'safe' version of the data will appear here soon. 

Access to the original data which is stored on the University of Otago's High-Capacity Central File Storage [HCS](https://www.otago.ac.nz/its/services/hosting/otago068353.html) is restricted.

## Using the code
This repo is intentionally structured as an R package so you can install it and re-use the code. You can do this in two ways:

*Clone/fork the repo from github* - this will give you a replication of the package as a local repo which you can edit & install locally. You can then (if you wish) submit pull requests for any improvements you make. Inevitably [#YMMV](http://en.wiktionary.org/wiki/YMMV).

*Install the package* - this will install it wherever your version of R(Studio) stores packages. It will also install any dependencies. However you will not (easily) be able to edit or amend the code. To do this:

 * install the R [devtools](http://r-pkgs.had.co.nz/git.html) package: `> install.packages("devtools")`;
 * run `> devtools::install_github(dataknut/nzGREENGridDataR)` - this should install the package and any [dependencies](http://r-pkgs.had.co.nz/description.html#dependencies) you may not have;
 * inevitably [#YMMV](http://en.wiktionary.org/wiki/YMMV).

## Re-Use and Contribution

### Terms of Re-Use

In general you can re-use the code and results provided you give appropriate attribution (citation) and retain the same usage terms in your own work.

### Re-Using the results
If you want to re-use any of the results in the md/html/pdf reports please cite them using the format described in the reports and observe the license terms applied (usually [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)).

### Re-Using the code

If you want to re-use the code in your own work, please read the repo [License](LICENSE) file for specific guidance. 

Inevitably [#YMMV](http://en.wiktionary.org/wiki/YMMV)

### Comments & suggestions:
Please use git [issues](https://github.com/dataknut/nzGREENGridDataR/issues) to make a comment or point out an error. We also use issues to manage our 'to do' list so please check your comment is not already open :-)
 
### Contributing code
Feel free to [fork](https://help.github.com/articles/fork-a-repo/) the repository (or a [branch](https://help.github.com/articles/about-branches/) if you are a collaborator with write access to this repo) and contribute your own additions through the normal git [pull request](https://github.com/dataknut/nzGREENGridDataR/pulls) process (ideally R or [RMarkdown](http://rmarkdown.rstudio.com/) please!). If you haven't used github before, now is a good time to [learn](https://guides.github.com/) - it works for any codebase, not just R. For R, we recommend using [RStudio](http://www.rstudio.com)'s integrated github features.

If you make a substantive addition to any of the exisiting RMarkdown reports please add yourself as an author. Your contributions will, in any case, be [tracked by github](https://help.github.com/articles/tracing-changes-in-a-file/) and so fully visible to the world in perpetuity :-)

