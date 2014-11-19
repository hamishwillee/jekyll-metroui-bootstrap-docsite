---
layout: default
title: Welcome
---

This site demonstrates a prototype Jekyll *documentation* theme based on [Metro UI Bootstrap](http://metroui.org.ua/), a library of CSS and JS that makes it easy to emulate the look and feel of Windows 8. The site uses no plugins and can be (is) automatically built by Github's version of Jekyll.

Currently the project is a prototype:

* It is full of debug information and it lacks features that a real site might need (SEO integration, analytics, feedback mechanisms, search). 
* The documentation is fragmentary - this is an experiment for me to determine what is possible, more than something intended for sharing.
* The responsive theme is not working properly
* All the navigation elements are generated from YML data files using include file functions. While this is a good idea for a TOC (which will regularly be updated by users), in practise the navbar menu would normally be hard-coded.
* The breadcrumb is only implemented for pages using the treeview sidebar
* If there is a problem with the library behaviour, I haven't attempted to fix it.

As this is a documentation theme, the "interesting" part is the implementation of a sidebar to provide a table-of-contents navigation for a document set based on a TOC definition in YML data files. MetroUI provides two sidebar components, and I've tested them both:

* [Sidebar](/tests/components/sidebar/index.html): A sidebar component that supports grouping and up to two levels of nesting. There is no way to autoamatically open the sidebar to a "current" page
* [Treeview](/tests/components/treeview/index.html): A jquery Treeview. This provides any level of nesting and the ability to open tree to current page on page load. 

In addition, the [Breadcrumb](/tests/components/treeview/index.html) is implemented for treeview TOCs, and there are some experiments with navbars (see the "Tests" menu item.)
S
Developers are welcome to extend or fork the project on [Github here](https://github.com/hamishwillee/jekyll-metro-bootstrap-docsite/tree/gh-pages).
