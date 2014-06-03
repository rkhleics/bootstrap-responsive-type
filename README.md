# Responsive Type for Bootstrap

We're sure you know already, but [Bootstrap](http://getbootstrap.com) is a sleek, intuitive, and powerful front-end framework for faster and easier web development, created by [Mark Otto](http://twitter.com/mdo) and [Jacob Thornton](http://twitter.com/fat), and maintained by the [core team](https://github.com/twbs?tab=members) with the massive support and involvement of the community.

This project has been created to add some additional 'Responsive Type' related functionality to boostrap implementations, which bootstrap doesn't yet have by default.

## Specific Aims

### 1) Allow for base font-size and line-height to be set for each breakpoint

In the past, we've found ourselves needing to adjust base font size at different breakpoints, to help text flow better, and to make the most out of whatever space is available. 

This project offers a new set of variables, allowing you to set individual font-size and line-height settings for each of bootstrap's default breakpoints.

### 2) Use scale values to reliably calculate heading sizes

We know the web is a vastly different world to print, but the practice of using type scales to control the differences in sizing between key type elements exists out of desire to improve consistency, and to preserve a relationship between type elements - Something that is applicable, whatever the medium.

This project aims to change the general approach of setting pixel-value variables to control heading sizes, and instead, allow you to specify scale values to determine heading sizes automatically and consistently.

### 3) Allow for different type scales to be applied for each breakpoint

Over time, we've often found ourselves hitting the same issues when it comes to heading sizes. e.g. 
> "That big H1 is fine when there is room for it, but at 320px wide, it takes up 2 whole screens". 

Rather than use just a single type scale, this project allows scales to be set for each of bootstrap's default breakpoints, allowing you to easily 'tighten-up' heading size difference when screen width is limited, and allow for bigger increments when that limitation is reduced.

## Project Limitations

For now, this project is only concerned with the sizes of headings and standard body text. Any bootstrap elements which define a font-size based on the **@base-font-size** variable (or it's derivitives), will not be effected by the integration of boostrap-responsive-type. Currently, this applies to buttons, badges, tooltips and popovers, carousel controls and some form elements.

## How To Install

The LESS files provided are designed to work with Bootstrap version v3.1.1, which is available to download here:
<https://github.com/twbs/bootstrap/archive/v3.1.1.zip>

1) After adding bootstrap to your project, go to bootstrap's less folder, and copy **less/responsive-type.less** and **less/responsive-type-variables.less** into it.

2) Open up **bootstrap.less** (in the same folder)

3) Add a new line after the **variables.less** import line, to add the new variables into your project. e.g. 
```
@import "responsive-type-variables.less";
```

Or, if you'd rather have all your variables in one file, you can copy and paste everything from **responsive-type-variables.less** into **variables.less** 

4) Add a new line after the **type.less** import line, to add responsive type functionality into your project. e.g. 
```
@import "responsive-type.less";
```

5) Recompile **bootstrap.less**

### Experimentation is key!

The default values should be enough to get you going, but the whole purpose of this project is to give you power, which you should fully exploit. Tweak the font-size, line-height and scale variables depending on your design and font selections, and find what works best for each breakpoint. The included **typetest.html** may be able to help you with this.

## Want to see some results quickly?

1. Add **typetest.html** to your project, and make sure it pulls in the newly compiled **bootstrap.css**
2. Open up **typetest.html** to see how your type and headings look, and use as a test for tweaking the values from **responsive-type-variables.less** according to your font selections and requirements

## Want to know a bit more?

See the comments within **responsive-type-variables.less** to get a better understanding about the variables, and how they are calculated. 

## Authors

**Andy Babic** - <http://twitter.com/andyjbabic>
