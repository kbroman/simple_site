---
layout: page
title: Making an independent website
---

This is what to do if you just want a website.

### First things

Start by cloning
[the repository for the present site](http://github.com/kbroman/simple_site). (Or,
alternatively, fork it and then clone your own version.)

    git clone git://github.com/kbroman/simple_site

Then change the name of that directory to something meaningful.

    mv simple_site something_meaningful

(Of course, don't use `something_meaningful` but rather
&ldquo;something meaningful.&rdquo;)

I've placed
[the present repository](http://github.com/kbroman/simple_site) in the
[public domain](http://creativecommons.org/publicdomain/zero/1.0/), so
do with it what you will, and cite
[me](http://www.biostat.wisc.edu/~kbroman) or not, as you feel is
appropriate.

Now change into that directory and remove the `.git` directory
(because you don't want the history of _my_ repository).

    cd something_meaningful
    rm -r .git

Now make it a git repository again.

    git init

### Things not to change

You'll need to keep the following files and directories largely unchanged.

    Rakefile
    _includes
    _layouts
    _plugins
    assets/themes

We _will_ change one file within `_includes/`; see below.

### Edit the `_config.yml` file

The
[`_config.yml`](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml)
file contains a bunch of configuration information. You'll want to
edit this file to replace my information with your information.

Perhaps edit the
[line with `exclude:`](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L5)
if you've named `License.md` and/or `ReadMe.md` differently. (I've
edited this line a bit, here.)

    exclude: [..., "ReadMe.md", "Rakefile", "License.md"]

Edit the
[lines about the site name and author](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L11-L17).

    title : simple site
    author :
      name : Karl Broman
      email : kbroman@gmail.com
      github : kbroman
      twitter : kwbroman
      feedburner : nil

Edit the
[`production_url` line](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L19)
by replacing `kbroman` with _your_ github user name, and replace
`simple_site` with the name that your repository will have on github
(`something_meaningful`?).

    production_url : http://kbroman.github.io/simple_site

Replace the
[`BASE_PATH` line](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L52)
with the same url.

    BASE_PATH : http://kbroman.github.io/simple_site

Replace the
[`ASSET_PATH` line](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L62)
in a similar way.

    ASSET_PATH : http://kbroman.github.io/simple_site/assets/themes/twitter

### Edit `_includes/themes/twitter/default.html`

The
[`_includes/themes/twitter/default.html`](https://github.com/kbroman/simple_site/blob/gh-pages/_includes/themes/twitter/default.html)
file defines how a basic page will look on your site. In particular,
it contains a bit of html code for a footer, if you want one.

Find the
[footer for my site](https://github.com/kbroman/simple_site/blob/gh-pages/_includes/themes/twitter/default.html#L46-L53)
and remove it or edit it to suit. This is the only bit of html you'll
have to deal with.

    <-- start of Karl's footer; modify this part -->
        <a href="http://creativecommons.org/publicdomain/zero/1.0/">

           ... blah blah blah ...

        href="http://github.com" target="_blank">github</a>
    <-- end of Karl's footer; modify this part -->
