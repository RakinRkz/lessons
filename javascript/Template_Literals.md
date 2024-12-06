# Template Literals


- Template literals are enclosed by backtick (\`) characters and can contain placeholders (${expression}) for **string interpolation**
- Multi-line strings
- Special constructs called tagged templates
- The default function for template literals is string interpolation, **but a custom tag function can be used for other operations**
- To escape a backtick in a template literal, use a backslash ( \ ) before the backtick
- Template literals coerce their expressions directly to strings, unlike the addition operator
- Tagged templates are an advanced form of template literals that allow for parsing template literals with a function

```js
`string text`

`string text line 1
 string text line 2`

`string text ${expression} string text`

tagFunction`string text ${expression} string text`
```

### Nesting

```js
const classes = `header ${
  isLargeScreen() ? "" : `icon-${item.isCollapsed ? "expander" : "collapser"}`
}`;
```


## Tagged Templates, Tag Function

Tags allow to parse template literals with a function.

The first argument of a tag function contains an array of string values. The remaining arguments are related to the expressions.
