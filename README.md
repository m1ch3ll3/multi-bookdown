# multi-bookdown

This is a minimal multi-bookdown example.

The idea of a multi-bookdown template came from my work colleagues. After exploring several file structures, I came up with the structure presented in this repository. 

One advantage of the multi-bookdown file structure is that multiple bookdown projects can access Rmd/md files stored together in a separate folder outside each bookdown project folder.

Another advantage of this example is that it truly contains the minimal number of files that are required to render a bookdown.

## how to use it

* Just place in the `rmd` folder all the Rmd/md files that the bookdowns will use
* Create one `bookdown-n` folder per bookdown project.

For each bookdown project:
* Change title, author and content of `index.Rmd`. Do not modify site, documentclass or output.
* Modify `_bookdown.yml` by listing all the Rmd files that comprise each book. Make sure to use relative paths (`../rmd/`)
* Run `bookdown-minimal.Rproj`and click the button Build Book on the Build tab
* The html output is generated to the `_book` directory.

## minimal example

Notice that each `bookdown-n` folder only contains:
    + `index.Rmd`
    + `_bookdown.yml`
    + `_book` folder
    + `bookdown-minimal.Rproj`
    
Also, `index.Rmd`and `_bookdown.yml` contain the smallest amount of code to have multi-bookdown up and running!

## where to find more 

This repository is the result of several hours spent playing with bookdown after exploring the following documents:
* Yihui Xie's book [bookdown: Authoring Books and Technical Documents with R Markdown](https://bookdown.org/yihui/bookdown/acknowledgments.html) 
* Sean Kross's post on [How to Start a Bookdown Book](http://seankross.com/2016/11/17/How-to-Start-a-Bookdown-Book.html)

Hope this helps!

Sincerely,

m1ch3ll3
