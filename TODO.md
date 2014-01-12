Create a gh-pages branch that has an "article" for every twbs example. See:
http://getbootstrap.com/getting-started/#examples

To do this, create a layout template under _layouts which serves as each type of example. All that is needed is content.

---

Goals for today:

1) finish all css and js aggregation
2) clean up commits
3) finish documentation
	README.md
	README.getting-started.md
	README.checklist.md ???
4) remove CNAME and other crap
5) generate gh-pages branch based on v3.0.3 with a single index.html using the starter-template

---

Future goals:

1) generate a post for each example
2) hook up gh-pages to the gh-pages.com URL from GoDaddy
3) create a nice index.html describing the project
4) explain how to use gh-pages branch as an example, but not a template. If you
clone the gh-pages branch as your starting point then you MISSED THE WHOLE
POINT.

---

Do NOT ship /js/custom.js or /css/custom.css in the master branch. Instead show how to use those in the gh-pages branch with some custom javascript + css for doing something crazy like changing the color of a div box when the mouse is clicked.
