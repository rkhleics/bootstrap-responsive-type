# Responsive Type for Bootstrap

In case you didn't know, [Bootstrap](http://getbootstrap.com) is a sleek, intuitive, and powerful front-end framework for faster and easier web development, created by [Mark Otto](http://twitter.com/mdo) and [Jacob Thornton](http://twitter.com/fat), and maintained by the [core team](https://github.com/twbs?tab=members) with the massive support and involvement of the community.

This project has been created to add some additional type-related functionality, which bootstrap doesn't have currently.

## Specific aims of this project

### 1) Adjust base font-size and line-height for different breakpoints

In the past, we've found ourselves needing to adjust general text size at different breakpoints, to help text flow better, and to make the most out of whatever space is available. 

This project offers font-size and line-height settings for each of bootstrap's default breakpoints, to make this easier to control.

### 2) Use scale values to reliably calculate heading sizes

We know the web is a vastly different world to print, but the practice of using fixed scale values to control the differences in sizing between certain type elements, exists out of desire for accuracy, consistency and a perseverance of a relationship between those elements. These concepts are applicable to all areas of design, whatever the format. 

This project aims to change the general approach of setting pixel-value variables to control heading sizes, and instead, use scale values to determine heading sizes automatically and consistently, maintaining that relationship between type elements.

### 3) Apply different type scales at different breakpoints

Over time, we've found ourselves hitting the same issues when it comes to heading sizes. e.g. "That big H1 is fine when there is room for it, but at 320px wide, it takes up 2 whole screens". 

Rather than use just a single type scale, this project allows scales to be set for each of bootstrap's default breakpoints, allowing you to easily 'tighten-up' heading size difference when screen width is limited, and allow for bigger increments when that limitation is reduced.

## Getting started

The LESS files provided are designed to work with Bootstrap version v3.1.1, which is available to download here:
<https://github.com/twbs/bootstrap/archive/v3.1.1.zip>

1. After adding bootstrap to your project, go to bootstrap's less folder, and copy **less/responsive-type.less** and **less/responsive-type-variables.less** into it.
2. Open up **bootstrap.less** (in the same folder)
3. Add a new line after the **variables.less** import line, to add the new variables into your project. e.g. **@import "responsive-type-variables.less";**. Or, if you'd rather have all your variables in one file, you can copy and paste everything from **responsive-type-variables.less** into **bootstrap/less/variables.less** 
4. Add a new line after the **type.less** import line, to add responsive type functionality into your project. e.g. **@import "responsive-type.less";**
5. Recompile **bootstrap.less**

### If you want to see results quickly

1. Add **typetest.html** to your project, and make sure it pulls in the newly compiled **bootstrap.css**
2. Open up **typetest.html** to see how your type and headings look, and use as a test for tweaking the values from **responsive-type-variables.less** according to your font selections and requirements


## Authors

**Andy Babic**

- <http://twitter.com/andyjbabic>
