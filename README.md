# multi-bookdown

This is a minimal multi-bookdown example.

Working with data is a back and forth process where proper communication with the internal teams and clients is fundamental. As such, it is common to have multiple Rmd/md's prepared for different purposes/audiences. These documents might share some content. As conditions, analysis, models and results evolve, documents that share part of their content start to diverge. Then either having to modify multiple documents becomes a burden, or the number of documents increases painfully.

The idea of a multi-bookdown template came from discussions with my data scientist colleagues. Our aim was to find a way of producing several documents/reports that could share part of their content without having to go through each document and make changes to each one separately.

After exploring several file structures that could help us achieve this, I came up with the structure presented in this repository. 

* One advantage of the multi-bookdown file structure is that multiple bookdown projects can access Rmd/md files stored together in a separate folder outside each bookdown project folder.

* Another advantage of this example is that it truly contains the minimal number of files that are required to render a bookdown, so looking into the contents of `bookdown-1` should help getting started with any bookdown project.

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

This repository is the result of several hours spent playing with bookdown and exploring previous work on the matter:
* Yihui Xie's book [bookdown: Authoring Books and Technical Documents with R Markdown](https://bookdown.org/yihui/bookdown/acknowledgments.html) 
* Sean Kross's post on [How to Start a Bookdown Book](http://seankross.com/2016/11/17/How-to-Start-a-Bookdown-Book.html)
* Alex Jackson blog [Fast and reproducible reports with bookdown](https://www.symbolix.com.au/blog-main/jagejccjfs77z6hndamhmwapt2tz3z)

Hope this helps!

Sincerely,

m1ch3ll3
