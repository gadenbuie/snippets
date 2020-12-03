## Snippets for RStudio

Various custom snippets designed for RStudio, but possibly useful elsewhere.

Copy the snippets into the correct language file from the **Global Options** > **Code** > **Edit Snippets** menu.

Or use [dgrtwo/snippr](https://github.com/dgrtwo/snippr) to install:

```r
# remotes::install_github("dgrtwo/snippr")
library(snippr)

# For all snippets
snippets_install_github("gadenbuie/snippets")

# For just the R snippets
snippets_install_github("gadenbuie/snippets", language = "r")

# For just an individual snippet
snippets_install_github("gadenbuie/snippets", language = "r", name = "aa")
```

For manual installation, copy the snippets to `~/.R/snippets/r.snippets` or `~/.config/rstudio/snippets` for RStudio 1.3. (Windows uses a different directory that I don't know off the top of my head, sorry.). `usethis::edit_rstudio_snippets()` may provide better advice.

```r
local({
  snippets_dir <- fs::path_home(".config", "rstudio", "snippets")
  fs::dir_create(snippets_dir) # make sure ~/.R/snippets exists

  gh_base_url <- "https://raw.githubusercontent.com/gadenbuie/snippets/master/"

  for (snippet in paste0(c("r", "markdown", "css", "html"), ".snippets")) {
    download.file(
      paste0(gh_base_url, snippet),
      fs::path(snippets_dir, snippet)
    )
  }
})
```

You may be able to find other useful snippets using [this GitHub search](https://github.com/search?q=in%3Apath+r.snippets+type%3Acode&type=Code).
