# [gh-bootstrap](https://github.com/mturquette/gh-bootstrap)

Simple bootstrap for a [Jekyll](http://jekyllrb.com/)-generated, [Twitter
Bootstrap](http://getbootstrap.com/)-powered website.

A better name would have been jekyll-bootstrap but it was already taken.

# tl;dr
For the impatient, follow these Exact Steps&trade;:

	git clone git://github.com/mturquette/gh-bootstrap.git
	cd gh-bootstrap
	jekyll serve

Open your browser and navigate to
[http://localhost:4000](http://localhost:4000) on Linux or
[http://0.0.0.0:4000](http://0.0.0.0:4000) on Mac OS X and you'll see an
exact replica of
[starter-template.html](http://getbootstrap.com/examples/starter-template/).

# branches

## master
Currently based on 3.0.x

## v2.3.2
This branch is frozen and uses the now unmaintained v2.3.2 tag of
Bootstrap. No work is being done on this branch.

## gh-pages
The source for gh-pages.com. Use this as an example, but the master
branch is where you should start for making your own website.

# design goals

The goal of this project is to provide a baseline for Jekyll-powered
websites using Bootstrap. I tried to keep it as
[opinion-free](http://stackoverflow.com/questions/802050/what-is-opinionated-software)
as possible.

From the [Bootstrap
website](http://getbootstrap.com/getting-started/#customizing),
"Bootstrap is best maintained when you treat it as a separate and
independently-versioned dependency in your development environment.
Doing this makes upgrading Bootstrap easier in the future." gh-bootstrap
maintains a copy of Twitter Bootstrap as a git submodule to achieve
this. This means you can switch to whatever version of Bootstrap you
want without messing up the gh-bootstrap sources.

gh-bootstrap provides a Jekyll **layout** corresponding to every example
in the Bootstrap ["Getting
started"](http://getbootstrap.com/getting-started/#examples) guide. We
use the
[starter-template](http://getbootstrap.com/examples/starter-template/)
example for gh-bootstrap's index.html. The other layouts each have a
Jekyll **post** to show them off.

For more details about gh-bootstrap's structure and how to use it for
your own blog please see README.getting-started.md

# contributing
Open a [new
issue](https://github.com/mturquette/gh-bootstrap/issues/new). If you
submit a patch please include a verbose changelog and a Signed-off-by
with your real human name, not an alias or psuedonym.

Enjoy!
