---
layout: default
title: Sidebar Tests
---

This page (and section) uses the [Metro UI sidebar component](http://metroui.org.ua/sidebar.html) to provide sidebar navigation.

The component demonstrates:

* Section headers
* Dropdowns
* Items with and without icons
* Items with "sticks" (coloured tabs)
* Dividers between dropdown icons
* A disabled item (URL will also be disabled)
* Current page is marked as active


The TOC used here is defined in **/_data/metrosidebar/sidebar-toc.yml**. The format to specify the above components is as shown below. Note that the "active" item is determined automatically, as is the name of the item linked by the URL (unless specified)

{% highlight yaml %}
- heading: Tests Group

- url: /tests/components/sidebar/index.html
  stick: bg-green
  icon: icon-home

- dropdown: Test Dropdown
  contents:
   - url: /tests/components/sidebar/sidebar1.html
     stick: bg-green
     icon: icon-home

   - divider: true

   - url: /tests/components/sidebar/sidebar2.html
     name: This name set in YAML


- dropdown: Another drop down
  contents:
   - url: /tests/components/sidebar/sidebar3.html

   - url: /tests/components/sidebar/sidebar4.html


- url: /tests/components/sidebar/sidebar5.html
  icon: icon-cube-2

- url: /tests/components/sidebar/sidebar6.html
  stick: bg-blue

- divider: true

- url: /tests/components/sidebar/sidebar7.html
  stick: bg-red
  disabled: true
  icon: icon-cog

- heading: Another heading

- url: /tests/components/sidebar/sidebar8.html
{% endhighlight %}


The tests have shown the following limitations:

* Dropdowns only support a single level of nesting (you can specify nested dropdowns, but these render badly). See [issues675](https://github.com/olton/Metro-UI-CSS/issues/675).
* There is no way to specify that a dropdown must be open on page load. The implication is that if the page is loaded and the current document is in a dropdown it will not be shown.
