---
title: "Contribute Post"
date: 2022-02-04T21:28:19+01:00
draft: true
toc: false
images:
tags:
  - hugo
  - R
  - R Markdown
  - tutorial
---

## Contributing

There are multiple ways to contribute a blog post. 

The simplest way is to contact us, and provide a blog post in whatever format you
feel comfortable writing.

To streamline the process, providing an Rmd document with the blog post will 
make the process quicker.

The best quickest way to contribute, is to [fork](#fork) the repository on GitHub, create the blog
post, and submit a pull request.

## Fork 'n write {#fork}

To do this, you will need a GitHub account, and have Hugo installed.

You can install Hugo with the **blogdown** package:

```{r eval=FALSE}
install.packages("blogdown")

blogdown::install_hugo()
```

### Creating a new post

The quickest way to start a new post is to use `hugo new posts/<name-of-post>/<name-of-post>.Rmd`,
substituting `<name-of-post>` with a computer-friendly name (i.e. using hyphens instead
of spaces).

This will create a new file called `<name-of-post>.Rmd` with the following YAML
header:

```yaml
---
title: "Name of Post"
date: 2021-09-05T14:12:00+02:00
draft: true
toc: false
images:
tags:
  - untagged
---
```

Or, you can do this in RStudio with the **blogdown** package:

```{r eval=FALSE}
blogdown::new_content("posts/<name-of-post>/<name-of-post>.Rmd)
```

Once you have finished creating your post, you can run `blogdown::serve_site()`
to render the post in the appropriate format, and view it in the 'Viewer' tab.
