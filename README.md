# Rchaeology Website

![Site status](https://github.com/rchaeology/rchaeology.github.io/actions/workflows/gh-pages.yml/badge.svg)

A [Hugo](https://gohugo.io/) site hosted by GitHub at <https://rchaeology.github.io>, using the awesome [Hello Friend NG](https://github.com/rhazdon/hugo-theme-hello-friend-ng) theme.

## Make changes locally

To work on the site locally before submitting a pull request, [fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) this repository and clone your fork **with the `--recursive` flag**:

```shell
git clone --recursive https://github.com/<username>/rchaeology.github.io.git
```

The `--recursive` flag ensures that you also get the [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) containing the site's theme.

If you already have a clone, but without the submodule you can run

```shell
git pull && git submodule init && git submodule update && git submodule status
```

### Using hugo on the command line

You will need to have [hugo](https://gohugo.io/getting-started/installing/)
installed to build the site and preview changes with `hugo server`. Use the `-D` flag
to preview the site with drafts (pages with `draft: true`).

### Using RStudio and blogdown

You can also use the [**blogdown**](https://bookdown.org/yihui/blogdown/) package to
make changes to the website. When dealing with .Rmd pages, **blogdown** is required.

If you haven't already, install **blogdown**:

```r
install.packages("blogdown")
```

Then use blogdown to install hugo:

```r
blogdown::install_hugo()
```

You can now serve the site. To do this you must set your working directory as the 
root of the site. This will preview the site in the Viewer pane of RStudio.

```r
blogdown::serve_site()
```

When you are done, use:

```r
blogdown::stop_server()
```


When you are finished, commit your changes and submit a pull request.
The site is automatically rebuilt when a pull request is accepted, so there is no need to use `hugo build` manually.

