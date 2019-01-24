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

You may be able to find other useful snippets using [this GitHub search](https://github.com/search?q=in%3Apath+r.snippets+type%3Acode&type=Code).
