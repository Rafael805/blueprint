# What is Sass (Syntactically Awesome StyleSheets)? 

Sass is an easy-to-use styling language that helps reduce a lot of the repetition and maintainability challenges of traditional CSS. Learning Sass will not only let you scale styles when working on big web development projects, it will also make it much faster and efficient to write reusable styles from scratch for smaller projects. Transitioning from CSS to SCSS (Sassy CSS) is pretty smooth due to the familiar syntax. 

Sass can't be directly interpreted by your browser, so it must first be converted, or compiled, to CSS before the browser can directly understand it.

Compile SCSS to CSS by typing the following command in the terminal that takes in two arguments:

The input (main.scss)
The location of where to place that output (main.css)

```
sass main.scss main.css
```

# Variables
**Variables** in SCSS allow you to assign an identifier of your choice to a specific value. Why is that useful? Unlike in CSS, if you need to tweak a value, you'll only have to update it in one place and the change will be reflected in multiple rules. In Sass, ```$``` is used to define and reference a variable:

```
$translucent-white: rgba(255,255,255,0.3);
```

# Mixins

# Nesting
**Nesting** is the process of placing selectors inside the *scope* of another selector. In Sass, it's helpful to think of the scope of a selector as any of the code between its opening { and closing } curly brackets. Selectors that are nested inside the scope of another selector are referred to as children. The former selector is referred to as the parent. This is just like the relationship observed in HTML elements.

--example: 
```
.parent {
  color: blue;
  .child {
    font-size: 12px;
  }
}
```

The above SCSS would compile to the following, equivalent CSS:
```
.parent {
  color: blue;
}

.parent .child {
    font-size: 12px;
}
```

You can also nest common CSS properties if you append a : colon suffix after the name of the property.

--example: 
```
.parent {
  font : {
    family: Roboto, sans-serif;
    size: 12px;
    decoration: none;
  }
}
```
will compile to the following CSS:
```
.parent {
  font-family: Roboto, sans-serif;
  font-size: 12px;
  font-decoration: none;
}
```


