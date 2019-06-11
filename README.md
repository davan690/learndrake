
[![Travis build
status](https://travis-ci.org/wlandau/learndrake.svg?branch=master)](https://travis-ci.org/wlandau/learndrake)
[![Codecov test
coverage](https://codecov.io/gh/wlandau/learndrake/branch/master/graph/badge.svg)](https://codecov.io/gh/wlandau/learndrake?branch=master)

# Machine learning workflow management with drake

Machine learning workflows can be difficult to manage. A single round of
computation can take several hours to complete, and routine updates to
the code and data tend to invalidate hard-earned results. You can
enhance the maintainability, hygiene, speed, scale, and reproducibility
of such projects with the [`drake`](https://github.com/ropensci/drake) R
package. [`drake`](https://github.com/ropensci/drake) resolves the
dependency structure of your analysis pipeline, skips tasks that are
already up to date, executes the rest with [optional distributed
computing](https://ropenscilabs.github.io/drake-manual/hpc.html), and
organizes the output so you rarely have to think about data files. This
workshop will teach you how to create and maintain machine learning
projects with [`drake`](https://github.com/ropensci/drake)-powered
automation.

# Installation

To obtain the workshop materials, simply install the `learndrake`
package.

``` r
install.packages("remotes")
library(remotes)
install_github("wlandau/learndrake")
```

# Usage

The functions in `learndrake` help navigate and deploy the workshop
materials.

| Function           | Purpose                                                                                                                                                  |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `view_slides()`    | Open the introductory slides in a web browser.                                                                                                           |
| `save_notebooks()` | Save the tutorials to your computer: R notebooks and supporting files.                                                                                   |
| `launch_app()`     | Launch a Shiny app that accompanies a tutorial.                                                                                                          |
| `save_app()`       | Save the app files so you can deploy to [shinyapps.io](https://www.shinyapps.io) or [Shiny Server](https://www.rstudio.com/products/shiny/shiny-server). |

# Introductory slides

The workshop begins with an introductory presentation on
[`drake`](https://github.com/ropensci/drake). View the slides at
<https://wlandau.github.io/learndrake/index.html> or open them
yourself in a browser with `view_slides()`.

# Tutorials

After the introductory presentation, students work through a sequence of
R notebooks in order. Use `save_notebooks()` to save the notebooks and
supporting files to your
computer.

| Notebook      | Topic                                                                                     |
| ------------- | ----------------------------------------------------------------------------------------- |
| `1-churn.Rmd` | Deep learning case study                                                                  |
| `2-setup.Rmd` | Convert the case study to a new [`drake`](https://github.com/ropensci/drake) project.     |
| `3-flow.Rmd`  | Develop, work, and iterate on the project.                                                |
| `4-plans`     | A deep dive into [`drake` plans](https://ropenscilabs.github.io/drake-manual/plans.html). |
| `5-files`     | Custom input and output data files.                                                       |
| `6-reports`   | Special considerations of `knitr` and R Markdown reports.                                 |
| `7-hpc`       | High-performance computing                                                                |

# Apps

Notebooks `3-flow.Rmd` and `4-plans.Rmd` come with supporting Shiny apps
to conduct the learning
exercises.

| App                                                                                  | Notebook      | Deploy locally               | Public URL                                    |
| ------------------------------------------------------------------------------------ | ------------- | ---------------------------- | --------------------------------------------- |
| Iterate on a [`drake`](https://github.com/ropensci/drake) workflow                   | `3-flow.Rmd`  | `launch_app("flow")`         | <http://wlandau.shinyapps.io/learndrakeflow>  |
| Exercises on [`drake` plans](https://ropenscilabs.github.io/drake-manual/plans.html) | `4-plans.Rmd` | `launch_app("plans")`        | <http://wlandau.shinyapps.io/learndrakeplans> |
| Visualize [`drake`](https://github.com/ropensci/drake) projects                      | `4-plans.Rmd` | `launch_app("drakeplanner")` | <http://wlandau.shinyapps.io/drakeplanner>    |

# Thanks

| Thanks to                                   | For                                                                                                                                                         |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Edgar Ruiz](https://github.com/edgararuiz) | Uniting `drake` and `keras` at <https://github.com/sol-eng/tensorflow-w-r> and providing valuable advice on the construction of the workshop.               |
| [Matt Dancho](https://github.com/mdancho84) | Publishing the original [blog post](https://blogs.rstudio.com/tensorflow/posts/2018-01-11-keras-customer-churn/) with the workshop’s underlying case study. |
| [Eric Nantz](https://github.com/rpodcast)   | Reviewing and providing feedback on this workshop.                                                                                                          |
