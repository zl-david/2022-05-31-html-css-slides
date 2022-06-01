# 📃 HTML - Head tags

There are more tags, but **these are the most used** / important head tags

```html
<head>
    <!-- prevent XSS -->
    <meta charset="utf-8" />

    <!-- SEO/UX -->
    <title>Page Title</title>

    <!-- for SEO -->
    <meta name="description" content="This is the page description" />
    <meta name="keywords" content="JavaScript,HTML,CSS" />

    <!-- gives the browser instructions on how to control the page's dimensions and scaling. -->
    <!-- important for mobile development -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- the color of the address bar on mobile devices -->
    <meta name="theme-color" content="#ff69b4" />

    <!-- defines base URI for any relative paths -->
    <base href="/3_head_tags/assets/" />

    <!-- links to external resources -->
    <link href="favicon.ico" rel="icon" />
    <link href="style.css" rel="stylesheet" />
    <link href="print.css" rel="stylesheet" media="print" />

    <style>
      body {
        font-weight: bold;
      }
    </style>

    <script>
      console.log('Hello world');
    </script>
  </head>
```


## Theme color

```html
<meta name="theme-color" content="#ff69b4" />
```

![Theme Color](/Users/david/Projects/campus/2021-06-01-slides-js-html-css/slides/images/html-themecolor.png)'


## Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Without & with viewport meta tag:

![Viewport](/Users/david/Projects/campus/2021-06-01-slides-js-html-css/slides/images/html-viewport.png)



# 📃 HTML - Body tags

### Style and Script tags

- `style` and `script` tag both in **head** and **body**.

### HTML5 tags

For a full list, check [https://www.tutorialrepublic.com/html-reference/html5-tags.php](https://www.tutorialrepublic.com/html-reference/html5-tags.php)

Here are the most commonly used tags:

- `article`: Defines an article
- `aside` : Defines some content loosely related to the page content
- `audio` : Embeds a sound, or an audio stream in an HTML document
- `footer` : Represents the footer of a document or section
- `header`: Represents the header of a document or section
- `main`: Represents the main or dominant content of the document
- `nav`: Defines a section of navigation links
- `section`: Defines a section of a document, such as header, footer, etc
- `video`: Embeds video content in an HTML document

### Elements get default browser styling

Example:

- `<div />` takes full horizontal space
- `<span />` are aligned next to each other
- `<p />` gets default margins
- `<a />`is underlined with blue color

# 🔧 Tools

- Browser: "View source code" / "Inspect element"
- Check if your markup is valid: [https://validator.w3.org/](https://validator.w3.org/)
