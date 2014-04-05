---
layout: page
title: Testing your site locally
---

To test your site locally, you'll need

- [ruby](https://www.ruby-lang.org/en/)
- the [github-pages](https://github.com/github/pages-gem) gem

### Installing ruby


### Installing the github-pages gem

Run the following command:

    gem install github-pages

This will install the `github-pages` gem and all dependencies
(including [jekyll](http://jekyllrb.com/)).

Later, to update the gem, type:

    gem update github-pages


### Testing your site locally

To construct and test your site locally, go into the directory and
type

    jekyll build

This will create (or modify) a `_site/` directory, containing
everything from `assets/`, and then the `index.md` and all
`pages/*.md` files, converted to html. (So there'll be
`_site/index.html` and the various `_site/pages/*.html`.)

Type the following in order to &ldquo;serve&rdquo; the site.

    jekyll serve

Now open your browser and go to
[http://localhost:4000](http://localhost:4000)
