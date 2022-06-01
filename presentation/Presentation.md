# HTML & CSS

---

# HTML & CSS

👋 Hi, I'm David

  
🏡  Edegem

💼  Tech Lead @ ZinderLabs

👨‍🏫  Coach @ The Campus

📷 🎸 @ Het Huis Van Vier

👨 👩 👦 👶

🐦  @hirviid
🐱  @zl-david

---


# Agenda

1. HTML
2. CSS
	- Building Blocks
	- 💻   Exercise _(flexbox)_
	- Other Properties
	- 💻   Exercise
	- Structuring CSS with BEM & SMACSS
3. SASS
	- Concepts
	- 💻   Exercise _(clean css)_

---


# 📃 HTML
> "Hyper Text Markup Language"

HTML describes the structure of a Web page

---

### HTML 5 Empty document

```html
<!DOCTYPE html>
<html>
	<head></head>
	<body></body>
</html>

```

DOCTYPE is used by browsers to validate the HTML document according to a specific standard

---

### HTML 4 Empty document

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
	<head></head>
	<body></body>
</html>
```

---

![[toppng.com-twitter-icon-transparent-400x400.png|200]]

---

### HTML5 Tags (1/2)

- `article`: Defines an article
- `aside` : Defines some content loosely related to the page content
- `audio` : Embeds a sound, or an audio stream in an HTML document
- `footer` : Represents the footer of a document or section
- `header`: Represents the header of a document or section

---

### HTML5 Tags (2/2)

- `main`: Represents the main or dominant content of the document
- `nav`: Defines a section of navigation links
- `section`: Defines a section of a document, such as header, footer, etc
- `video`: Embeds video content in an HTML document

[https://www.tutorialrepublic.com/html-reference/html5-tags.php](https://www.tutorialrepublic.com/html-reference/html5-tags.php)


---

# 💅 CSS
> "Cascading Style Sheets"

CSS describes how HTML elements are to be displayed on screen, paper, or in other media


---

What can you do with CSS?

- https://codepen.io/onediv/pen/BprVzp
- https://codepen.io/hrtzt/pen/JdYaEZ
- [https://codepen.io/amit_sheen/pen/XWMXwvJ](https://codepen.io/amit_sheen/pen/XWMXwvJ)

---

### Learning CSS

![[Pasted image 20220524162107.png]]

---

### Learning CSS
#### Starts simple

```css
.warning-text {
  color: red;
  font-style: italic;
}
```

---

### Learning CSS
#### Is hard
- Implicit language
- Browser dependent
- No exceptions or error logs
- Unexpected results

---

### 4 ways to include CSS

1. Inline CSS 
2. Internal CSS 
3. External CSS 
4. Using @𝗶𝗺𝗽𝗼𝗿𝘁

---

### Cascade & Specificity
 Mechanisms that control which CSS rule applies

---

### Cascade & Specificity

```css
#testId {
  background-color: purple;
}

div:first-child {
  background-color: blue;
}

.testClass {
  background-color: red;
}

body div {
  background-color: green
}
```

```html
<div class="testClass" id="testId"></div>
```

What's the background color of the `div`?

---

### The Cascade

1. Position and order of appearance 
2. Origin 
3. Importance {`!important` keyword}
4. Specificity 

---

### The Cascade
#### Specificity

1. Inline styles (`style="..."`)
2. Id selector (`#example`)
3. Pseudo class selector (`:hover`, `:first-child`)
4. Class selector (`.example`)
5. Element selector (`body div`)

---

## 🎯 Key takeaway

Specificity makes CSS hard.

Minimize specificity hell by **using only classes** to style your HTML.

---

### Inheritance

> Inheritance controls what happens when no value is specified for a property on an element.

1. Inherited properties
2. Non-inherited properties

---

### Controlling Inheritance

- `prop: inherit`: Use parent styling
- `prop: initial`: Browser default
- `prop: unset`:  if the property is naturally inherited it acts like `inherit`, otherwise it acts like `initial`.

---

### The Box Model

```html
<style>
  .parent {
    width: 200px;
    border: 2px solid black;
  }
  .box {
    width: 100%;
    border: 2px solid hotpink;
    padding: 20px;
  }
</style>

<div class="parent">
  <div class="box"></div>
</div>
```

How wide is the `.box` element?

1. 200px
2. 240px
3. 244px
4. 0px

---

![[Pasted image 20220530133854.png]]

---

### Layout Algorithms

1. Flow (= default)
2. Positioned (e.g. `position: absolute`)
3. Flexbox
4. Table
5. Grid

---

### Layout Algorithms
- There's no "`layout-mode`" property
- Several properties can tweak the layout algorithm used 

---

### Layout Algorithms
CSS property applied to an element: 

```css
.help-widget {
  /* Uses Positioned layout, because of this declaration: */
  position: fixed;
  right: 0;
  bottom: 0;
}

.floated {
  /* Uses Float layout, because of this declaration: */
  float: left;
  margin-right: 32px;
}
```

---

### Layout Algorithms
CSS property applied to _**the parent element**_: 

```html
<style>
  .row {
    display: flex;
  }
</style>

<ul class="row">
  <li class="item"></li>
  <li class="item"></li>
  <li class="item"></li>
</ul>
```

---

#### Layouts

1. Flow (= default)
2. Positioned (e.g. `position: absolute`)
3. Flexbox
4. Table
5. Grid

---

### 💻  DIY
  
https://flexboxfroggy.com/

## 🐸

---

### Properties
Real world example

---

### 💻  DIY

https://github.com/zl-david/2022-05-31-css-exercise

---

# 💅 CSS - Keeping it Clean

With SMACSS & BEM

---

### SMACSS

> *Scalable and Modular Architecture for CSS*

a.k.a Folder organisation

---

### SMACSS
#### Organize your CSS in 3 folders

1. base
2. modules
3. state

---

### SMACSS
#### Base
Base styles are just **Normalize** plus some **basic default element styles** (colors, typography, margins & padding).


---

### SMACSS
#### Modules
Modules are standalone, reusable components that have no knowledge of their parent container.

---

### SMACSS
#### State

Module-specific state classes are defined in the same file as the module itself (e.g. .my-module--is-active) but we keep **global state classes** separate, e.g. .is-hidden.


---

### BEM
> *Block, Element and Modifier*

a.k.a. Class naming convention

---

![[css-bem.png]]

- Green: Block
- Blue: Element
- Red: Modifier

---

### BEM
#### Block
Standalone entity that is meaningful on its own.

*E.g.: menu*

---

### BEM
#### Element
A part of a block that has no standalone meaning and is semantically tied to its block.

E.g.: *.menu__item*

---

### BEM
#### Modifier
A flag on a block or element. Use them to change appearance or behavior.

E.g.: *.button--big*


---

### 💻  DIY

https://github.com/zl-david/2022-05-31-css-exercise


---

# 👓 SASS
> **Syntactically awesome style sheets**


Sass is a stylesheet language that’s compiled to CSS. It allows you to use [variables](https://sass-lang.com/documentation/variables), [nested rules](https://sass-lang.com/documentation/style-rules#nesting), [mixins](https://sass-lang.com/documentation/at-rules/mixin), [functions](https://sass-lang.com/documentation/modules), and more, all with a fully CSS-compatible syntax.

---

### SASS docs
https://sass-lang.com/guide


---

### 💻  DIY

https://github.com/zl-david/2022-05-31-css-exercise

