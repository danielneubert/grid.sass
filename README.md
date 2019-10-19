<h1 align="center">grid.sass</h1>

<p align="center">
    <a href="https://www.npmjs.com/package/grid.sass">
        <img src="https://img.shields.io/npm/v/grid.sass?color=%2350C322&label=version" alt="Package name">
    </a>
    <a href="https://cdn.jsdelivr.net/npm/grid.sass/grid.css">
        <img src="https://img.shields.io/jsdelivr/npm/hy/grid.sass?color=%231384C5&label=downloads" alt="Downloads each month">
    </a>
    <a href="https://cdn.jsdelivr.net/npm/grid.sass/grid.css">
        <img src="https://img.shields.io/npm/dt/grid.sass?color=%2337A5DB&label=installations" alt="Downloads each month">
    </a>
    <a href="https://github.com/danielneubert/grid.sass/blob/dev/LICENSE">
        <img src="https://img.shields.io/npm/l/grid.sass?color=%234E9384" alt="Latest Stable Version">
    </a>
</p>



## 💡 About grid.sass

The **grid.sass** package is a tiny and easy to use **Sass file** for creating a grid-based layout across all common browsers **including Internet Explorer 11**.



## ⚓️ Anchors

- [**Download / Install**](#-download--install)
- [**Classes**](#-classes)
- [**Examples**](#-examples)
- [**Variables**](#%EF%B8%8F-variables)
- [**Modify grid.sass**](#-modify-gridsass)
- [**Licence**](#-licence)



## 📦 Download / Install

### CDN

If the [**default configuration**]() for **grid.sass** suits your needs, the recommended way for including the CSS file to your project is via CDN:

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/grid.sass/css/grid.css">
```


### NPM

If you want to directly include the created classes to your project files or want to [**modify grid.sass**]() feel free to get the package:

```sh
npm install grid.sass
```

After that you can easily include **grid.sass** to your Sass or Scss file like so:

```scss
// Scss
@import '~grid.sass';

// Sass
@import '~grid.sass'
```


### Direct Download

While not recommended you can also download the project files here:

Get [**grid.css** (compiled version)](https://cdn.jsdelivr.net/npm/grid.sass/grid.css) or 
[**grid.sass** (raw version)](https://cdn.jsdelivr.net/npm/grid.sass/grid.sass).

[**⬆ back to top**](#gridsass)



## 💅 Classes

The `grid.sass` compiles to a set of classes you can see listed here:

|CSS class              |Description                                                    |
|-----------------------|---------------------------------------------------------------|
|`grid`                 |Required class for the wrapping container.                     |
|`grid--full*`          |Span a children across all columns.                            |
|`grid--span-{columns}*`|Span a children across multible columns.                       |
|`grid--flex`           |Required class for a flexible column layout.                   |
|`grid--flex-{columns}*`|Defines the amount of columns all children will be placed with.|

*Classes with an  `*` star at the end can be used with a [breakpoint modifier]() like `--t`.*

[**⬆ back to top**](#gridsass)



## 📖 Examples

In order to use **grid.sass** you can simply add the `grid` class to your wrapping element and already get you column-based layout. *(12 columns by default)*

Below you will find some examples using [all classes](#-classes) the **grid.sass** package is providing. Keep in mind that your configuration for **grid.sass** may vary.


**All examples:**

1. [**Basic Setup**](1-basic-setup)
2. [**Span Across Multible Columns**](2-span-across-multible-columns)
3. [**Using Breakpoint Modifiers**](3-using-breakpoint-modifiers)

### 1. Basic Setup

Setting up **grid.sass** is as easy as think. Simply add the `grid` class to the wrapping container and you are done:

```html
<div class="grid">
    <div>Column 1</div>
    <div>Column 2</div>
    <!-- ... -->
</div>
```

[**⬆ Examples**](#-examples)  |  [**⬆ back to top**](#gridsass)


### 2. Span Across Multible Columns

Since in most cases you will need to span across multible columns *(e.g. three boxes side by side)* **grid.sass** has a handy helper for that:

```html
<div class="grid">
    <div class="grid--span-4">Box 1</div>
    <div class="grid--span-4">Box 2</div>
    <div class="grid--span-4">Box 3</div>
</div>
```

[**⬆ Examples**](#-examples)  |  [**⬆ back to top**](#gridsass)


### 3. Using Breakpoint Modifiers

In some cases your content may vary between different types of devices / screens. For that **grid.sass** provides the easy to [use **breakpoint modifiers**](grid-sass--breakpoints).

The following example will show three boxes side by side. *(See [Example #2](#2-span-across-multible-columns))* But for mobile devices the boxes will be spanned across the full layout.

```html
<div class="grid">
    <div class="grid--span-4 grid--full--m">Box 1</div>
    <div class="grid--span-4 grid--full--m">Box 2</div>
    <div class="grid--span-4 grid--full--m">Box 3</div>
</div>
```

[**⬆ Examples**](#-examples)  |  [**⬆ back to top**](#gridsass)


### 4. Flexible Grid Layout

In some cases you will run into a limit with your given column layout. *(e.g. displaying 5 equal columns on a 12-column-based layout)*

Therefore the `grid--flex` class can help you as long as you don't need to span across multible columns.

```html
<div class="grid grid--flex grid--flex-5">
    <div>Box 1</div>
    <div>Box 2</div>
    <div>Box 3</div>
    <div>Box 4</div>
    <div>Box 5</div>
</div>
```

[**⬆ Examples**](#-examples)  |  [**⬆ back to top**](#gridsass)


### 5. Breakpoint Modifiers for grid-flex

Like the normal gird you can also use the [**breakpoint modifiers**](grid-sass--breakpoints) to change the layout of the `grid--flex` class.

With the given Example above you might want to change layout for mobile devices to a 3-column-based layout on tablets like here:

```html
<div class="grid grid--flex grid--flex-5 grid--flex-3--t">
    <div>Box 1</div>
    <div>Box 2</div>
    <div>Box 3</div>
    <div>Box 4</div>
    <div>Box 5</div>
</div>
```

[**⬆ Examples**](#-examples)  |  [**⬆ back to top**](#gridsass)



## ♻️ Variables

The **grid.sass** package is build with modification in mind. Therefor everthing can be changed or alternated to your needs.

You can modify these variables:
- [**$grid-sass--flex** (Boolean)](#grid-sass--flex)
- [**$grid-sass--columns** (Number)](#grid-sass--columns)
- [**$grid-sass--gaps** (Map)](#grid-sass--gaps)
- [**$grid-sass--breakpoints** (Map)](#grid-sass--breakpoints)

### $grid-sass--flex

The flex variable determines whether the `grid--flex` class and its helper classes should generated.

**Default Value:**
```scss
$grid-sass--flex: true;
```

[**⬆ Variables**](#%EF%B8%8F-variables)  |  [**⬆ back to top**](#gridsass)

### $grid-sass--columns

Determines the amount of columns your layout should be based on.

**Default Value:**
```scss
$grid-sass--columns: 12;
```

[**⬆ Variables**](#%EF%B8%8F-variables)  |  [**⬆ back to top**](#gridsass)

### $grid-sass--gaps

> The **grid.sass** package uses the **Map**-type for Sass/Scss. These can be basically seen as objects containing key-value pairs.

For the gap configuration the gap size has to given with the key `null`.

If you have alternating gap sizes *(like the default one)* you can name the breakpoint as well as the changed gap size. 

**Note:** You mustn't provide a gap size for each breakpoint since it will bloat the resulting file size.

**Default Value:**
```scss
$grid-sass--gaps: (
    null: 2rem,
    '--t': 1rem
);
```

[**⬆ Variables**](#%EF%B8%8F-variables)  |  [**⬆ back to top**](#gridsass)

### $grid-sass--breakpoints

> The **grid.sass** package uses the **Map**-type for Sass/Scss. These can be basically seen as objects containing key-value pairs.

In order to provide alternating column configuration or [gap sizes](#grid-sass--gaps) you will need to define one or multible breakpoints.

In order to work properly you need to have a `null: null` pair within the Map.

Besides that you can add as many breakpoints as you like. The key of each pair is the breakpoint modifier *(conatining the `--`)* and the respective value contains the media query *(without the `@media` keyword)* when the breakpoint starts.

**Default Value:**
```scss
$grid-sass--breakpoints: (
    null: null,
    '--t': '(max-width: 1299px)',
    '--m': '(max-width: 699px)'
);
```

[**⬆ Variables**](#%EF%B8%8F-variables)  |  [**⬆ back to top**](#gridsass)



## 🛠 Modify grid.sass

For most projects you might want to modify **grid.sass** to your needs.

You can easily modify the configuration for this by simply defining the [**variables** listed above](#%EF%B8%8F-variables) before you import **grid.sass**.

Here is a short example in Sass:
```scss
$grid-sass--flex: false
$grid-sass--columns: 8

@import '~grid.sass'
```

[**⬆ back to top**](#gridsass)



## 🗝 Licence

Pile is released under the MIT License. See the bundled [LICENSE](LICENSE) file for details.

[**⬆ back to top**](#gridsass)
