# [gh-bootstrap](https://github.com/mturquette/gh-bootstrap)

Simple bootstrap for a [Jekyll](http://jekyllrb.com/)-generated,
[Twitter Bootstrap](http://twitter.github.io/bootstrap/)-powered
website.

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

# why?
While redesigning [my blog](http://deferred.io) I decided to use
Bootstrap. Many [github-pages](http://pages.github.com/) use Bootstrap,
but cloning someone's blog or project page and reworking it is a pain. I
also wanted to avoid rolling my own solution like every other
github-page out there and adding to the chaos. What I wanted was a
**framework**. I was surprised not to find many options for this, and
the ones I found where either very
[opinionated](http://stackoverflow.com/questions/802050/what-is-opinionated-software)
or did not provide a clear upgrade path to future versions of Bootstrap.

Instead of simply rolling my own solution and immediately spoiling the
environment with my own hideous css and javascript I opted to create a
bootstrap of Bootstrap for a bare bones github page. Hence gh-bootstrap.

From the [Bootstrap website](http://getbootstrap.com/getting-started/#customizing), "Bootstrap is best maintained when you treat it as a separate and independently-versioned dependency in your development environment. Doing this makes upgrading Bootstrap easier in the future."

Managing Bootstrap as a git submodule is the right way to do this.

# goal
The goal of this project is to provide a pristine baseline for github-pages using Bootstrap. Almost no personal preference, opinion, customization or religion is present. Instead this skeleton aims to perfectly reproduce the **starter-template.html** example from the Bootstrap documentation with Jekyll and do nothing more.

# design
Bootstrap itself is a git submodule with no additions or modifications on my part. It can be found in the **\_includes** directory. Any user cloning gh-bootstrap can modify that submodule to point at any version of Bootstrap that they see fit, including their own modified version. As Bootstrap releases new versions this git submodule will be updated to reflect the new version, but there is no hard rule stating that gh-bootstrap users must follow along this upgrade path.

The assets located outside of the **\_includes** directory are all derived from Bootstrap. **index.html** simply contains the content from the `container` div of **starter-template.html**. The rest of **start-template.html** exists in **\_layouts/layout.html**. The top-level **js** and **css** directories each contain a file which uses an empty [YAML front-matter](http://jekyllrb.com/docs/frontmatter/) and several `{% include ... %}` statements to glob the js and css files from the Boostrap repo into one file which is included by the layout. Credit goes to [gkwelding](http://in-the-attic.com/2013/01/04/building-a-blog-using-jekyll-bootstrap-and-github-pages-a-beginners-guide/) for this great trick.

The Jekyll-specific bits CNAME, atom.xml, and \_config.yaml are sane defaults filled in with "Example" and "example.com" placeholders. In particular \_config.yaml has `author` & `description` sections that will be used in several key areas by the [Liquid Template](http://jekyllrb.com/docs/variables/) system. If you see any strings with "Example" in them, such as a page title, metadata, etc. then it is likely that you forgot to update these sections. These files represent the full extent of my customization efforts, such is my _epic_ sense of restraint.

# what's missing?
Content!  In trying to keep this project as opinion-free as possible I neglected to include posts, layouts, custom javascript, custom css and all of the stuff that makes a website a website. That's your job.

# make it yours
Store your custom javascript and style sheets in **\_includes/js/custom.js** and **\_includes/css/custom.css**. Or if you are really cool, put your custom stuff into a separate git repository and add it to gh-bootstrap as a git submodule in **\_includes**. Additionally any libraries or plugins that you import into the **\_includes** directory can be added as a git submodule which is really great for pulling in projects like underscore.js, backbone.js, etc. Simply edit **js/all.js** and **css/all.css** to include the assets you want.

gh-bootstrap also makes it easy to rapidly deploy websites using Jekyll. Just fork the project, add in your favorite libraries, plugins, frameworks and boilerplate/glue and save that as your own boostrapgh-bootstrap. Dude ... so meta, right?  With an unopinionated baseline you stand to benefit from more reuse as others create their own opinionated gh-bootstrapbootstrap and follow a similar layout to your own.

# contributing
Got a beef, an axe to grind, or a bone to pick?  Open a [new issue](https://github.com/mturquette/gh-bootstrap/issues/new). If you submit a patch please include a verbose changelog summary and a Signed-off-by with a real human name, not an alias or psuedonym.

Enjoy!
