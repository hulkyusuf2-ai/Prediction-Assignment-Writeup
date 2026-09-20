# Practical Machine Learning – Course Project 392

Predicting the manner in which participants performed barbell lifts (`classe` A–E) from
accelerometer data (Weight Lifting Exercise Dataset, Velloso et al., 2013).

* `pml-project.Rmd` – analysis source
* `pml-project.html` – compiled report
* `predictions/` – one file per test case (for the prediction quiz)

## Reproduce

```r
install.packages(c("caret", "randomForest", "gbm", "rpart", "ggplot2", "e1071", "rmarkdown"))
rmarkdown::render("pml-project.Rmd")
```

## Publish on GitHub Pages

```bash
git init
git add pml-project.Rmd pml-project.html README.md
git commit -m "Course project"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main

# gh-pages branch so the HTML is viewable online
git checkout -b gh-pages
cp pml-project.html index.html
git add index.html && git commit -m "Add index for gh-pages"
git push -u origin gh-pages
```

The report is then at `https://<user>.github.io/<repo>/`.

## Data citation

Velloso, E.; Bulling, A.; Gellersen, H.; Ugulino, W.; Fuks, H. *Qualitative Activity Recognition of
Weight Lifting Exercises.* Proceedings of the 4th International Conference in Cooperation with SIGCHI
(Augmented Human '13). Stuttgart, Germany: ACM SIGCHI, 2013.
