# Lessons learned from testing 2500+ Shiny Apps every day

## Event
2023 Appsilon Shiny Conference <br />
March 15, 2023 <br />
https://shinyconf.appsilon.com/conference-scheduler/ <br />
https://hopin.com/events/shinyconference2023

## Slides

* HTML:
http://schloerke.com/presentation-2023-03-15-appsilon-nightly-testing/

* PDF:
http://schloerke.com/presentation-2023-03-15-appsilon-nightly-testing/appsilon-nightly-testing.pdf

* Recording: https://www.youtube.com/watch?v=WQ_sbmR-IPQ&list=PLexAKolMzPcriOdeLwoMxQOyHRnMguEv4&index=8


## Resources for learning more

* [`{shinytest2}`](https://rstudio.github.io/shinytest2/) [:octocat:](https://github.com/rstudio/shinytest2): Regression Testing for Shiny Applications

* [`r-lib/actions` :octocat:](https://github.com/r-lib/actions): GitHub Actions for the R language

* [`{testthat}`](https://testthat.r-lib.org/) [:octocat:](https://github.com/r-lib/testthat/): Unit Testing for R

* [`{shiny}`](https://https://shiny.rstudio.com/) [:octocat:](https://github.com/rstudio/shiny): Web Application Framework for R

* :book: Mastering Shiny, [Chapter 21: Testing](https://mastering-shiny.org/scaling-testing.html)
* :book: R Packages, [Chapter 12: Testing](https://r-pkgs.org/tests.html)


## Abstract

The Shiny team tests 2500+ different combinations of Shiny Applications, R versions, and operating systems to verify no feature regressions occur within the bleeding edge of the Shiny-verse. Over the past few years, we have learned a few lessons to keep our tests robust and honest. There is a non-zero chance that a test failure is not your fault. When working with CI systems, external influences such as installation failures or slower computing power will prevent tests from executing properly. A picture is worth a thousand tests but visual testing is known to have a non-zero false-positive rate. To address this, we have utilized threshold based image comparisons for flaky tests. We have found that it is best to test the minimal amount of content where possible. Changes in App package dependencies can produce unintended changes in expected outputs. These hard learned lessons have reduced unreliable test results allowing the Shiny team to quickly respond to feature regressions.

<!-- > _Updated_ -->
