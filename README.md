# README

## Creating an RStudio project under version control

1. Create the repository on GitHub

1. Create a new project in RStudio -> version control -> Git

1. Enter git url of new repository, something like https://github.com/myname/myrepo.git

1. Make a short README file that describes the repo, this is usually a .Rmd or .md file.

1. Make your first commit - can be from command line or git tab in upper right of RStudio window

1. This is the basic workflow for every commit:

     * `git add -A` to 'stage' all files for a commit or `git add README.md` to stage a specific file

     * `git commit -m "informative message"` makes the commit with the message, make your messages short but informative so future you (or someone else) can understand the reason for the commmit

     * `git push` pushes the local commits to the remote repository

## Working on a repository with others

The workflow for setting up the repository follows steps 1 - 3 above. However, you will have to make sure you are always working with the current version for your local repository. An additional step is needed before pushing new commits to the local repository. Follow this workflow:

* Open the RStudio project before you make any changes, run git pull to retrieve any additions to the remote repository since your last commit.

* Make changes/edits.

* `git add -A` to 'stage' all files for a commit or git add README.md to stage a specific file

* `git commit -m "informative message"` makes the commit with the message, make your messages short but informative so future you (or someone else) can understand the reason for the commmit

* `git pull` will pull any changes that may have occurred since opening the project.

* `git push` pushes the local commits to the remote repository.

Occasionally you will have merge conflicts if remote changes cannot be automatically merged with your local version. You will have to fix these by hand and commit the manual changes. See [here](https://www.git-tower.com/learn/git/ebook/en/command-line/advanced-topics/merge-conflicts).

## RMarkdown

[Cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)

These documents let you integrate R code and output with markdown text to create an integrated pdf, word, or html file. Text in an RMarkdown file lives either in or out of a code chunk. Text outside of a code chunk can be HTML, markdown, or plain text and text in code chunks is regular R code. The document is converted to HTML or pdf output by pressing the knit button on the top left of the RStudio console. This renders the Rmd file to md and then md to html or pdf.

The top of each RMarkdown file includes YAML text that defines the overall format of the html or pdf final document. Here you specify things like title, author, type of output, including a table of contents, etc. See [here](http://rmarkdown.rstudio.com/html_document_format.html#overview) for more info.

The code chunks are processed as R code using options that are defined at the top of each chunk. These control the output of the code and how the code is displayed in the final document. See the [cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf) or go [here](https://yihui.name/knitr/options/) for complete documentation.

You can open an RMarkdown template by opening a new file from the File menu.

RMarkdown documents can be hosted on a web page in a project under version control. In the repository under settings, the web page source must be changed from 'none' to 'master'. All web-enabled content in your repository can now be accessed through a URL. For example, an HTML file named `myfile.html` in the repository with the URL https://github.com/myname/myrepo can be viewed from  https://myname.github.io/myrepo/myfile.
