
<!-- README.md is generated from README.Rmd. Please edit that file -->

The goal of geospatial-theme is to provide a base for geospatial
research at ITS.

## Technical note

The website was created using github and the following commands in bash:

``` bash
git clone git@github.com:ITSLeeds/geospatial-theme
rm -rv public
mv geospatial-theme public 
cd public
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index
git clean -fdx
echo "My GitHub Page" > index.html
git add .
git commit -a -m "First pages commit"
git push origin gh-pages
```

Then in R:

``` r
blogdown::new_site()
f = list.files(path = "content/post/", full.names = TRUE)
unlink(f, recursive = TRUE)
```
