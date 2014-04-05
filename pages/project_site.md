---
layout: page
title: Making a project site
---

If you want to make a website for a GitHub-hosted project, as I've
done for my [R/qtlcharts package](http://kbroman.github.io/qtlcharts),
you just follow my
[instructions for making an independent site](independent_site.html),
with just a few modifications.

Go to your local repository and create a `gh-pages` branch and then
switch to that new branch

    cd my_repo
    git branch gh-pages
    git checkout gh-pages

Remove _everything_, and then commit having removed everything.

    git rm -r .
    git commit -m "Remove everything frmo gh-pages"

Now go back one directory and clone
[the present repository](http://github.com/kbroman/simple_site).

    cd ..
    git clone git://github.com/kbroman/simple_site

Change into that directory and remove the `.git/` directory.

    cd simple_site
    \rm -rf .git

Move all of the stuff from that directory into _your_ repository
(in the new and empty `gh-pages` branch).

    cd ../my_repo
    cp -r ../simple_site/. .

Edit everything [as before](independent_site.html).
Commit everything and push the `gh-pages` branch to github.
