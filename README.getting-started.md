---

Feel free to delete all of the Jekyll **posts** under _posts/ and 

I recommend that you add the following

Each of these Jekyll posts set **published: false** in the YAML
front-matter. This is so that you can 

---

# how to use it

gh-bootstrap tries to be somewhat future-proof. The bootstrap 

---


# design
Bootstrap itself is a git submodule with no additions or modifications
on my part. It can be found in the **\_includes** directory. Any user
cloning gh-bootstrap can modify that submodule to point at any version
of Bootstrap that they see fit, including their own modified version. As
Bootstrap releases new versions this git submodule will be updated to
reflect the new version, but there is no hard rule stating that
gh-bootstrap users must follow along this upgrade path.

The assets located outside of the **\_includes** directory are all
derived from Bootstrap. **index.html** simply contains the content from
the `container` div of **starter-template.html**. The rest of
**start-template.html** exists in **\_layouts/layout.html**. The
top-level **js** and **css** directories each contain a file which uses
an empty [YAML front-matter](http://jekyllrb.com/docs/frontmatter/) and
several `{% include ... %}` statements to glob the js and css files from
the Boostrap repo into one file which is included by the layout. Credit
goes to
[gkwelding](http://in-the-attic.com/2013/01/04/building-a-blog-using-jekyll-bootstrap-and-github-pages-a-beginners-guide/)
for making me aware of this trick.

The Jekyll-specific bits CNAME, atom.xml, and \_config.yaml are sane
defaults filled in with "Example" and "example.com" placeholders. In
particular \_config.yaml has `author` & `description` sections that will
be used in several key areas by the [Liquid
Template](http://jekyllrb.com/docs/variables/) system. If you see any
strings with "Example" in them, such as a page title, metadata, etc.
then it is likely that you forgot to update these sections. These files
represent the full extent of my customization efforts, such is my _epic_
sense of restraint.

# what's missing?
Content!  In trying to keep this project as opinion-free as possible I
neglected to include posts, layouts, custom javascript, custom css and
all of the stuff that makes a website a website. That's your job.

# make it yours
Store your custom javascript and style sheets in
**\_includes/js/custom.js** and **\_includes/css/custom.css**. Or if you
are really cool, put your custom stuff into a separate git repository
and add it to gh-bootstrap as a git submodule in **\_includes**.
Additionally any libraries or plugins that you import into the
**\_includes** directory can be added as a git submodule which is really
great for pulling in projects like underscore.js, backbone.js, etc.
Simply edit **js/all.js** and **css/all.css** to include the assets you
want.

gh-bootstrap also makes it easy to rapidly deploy websites using Jekyll.
Just fork the project, add in your favorite libraries, plugins,
frameworks and boilerplate/glue and save that as your own
boostrapgh-bootstrap. Dude ... so meta, right?  With an unopinionated
baseline you stand to benefit from more reuse as others create their own
opinionated gh-bootstrapbootstrap and follow a similar layout to your
own.


---

# Adding dependencies

Use git submodules to add in new dependencies (e.g. backbone.js).
Aggregate any new CSS or JS assets by adding an additional **include**
directive in `css/all.css` or `js/all.js`.
