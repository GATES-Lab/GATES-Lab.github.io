### Repo structure
```
.
|-- Gemfile - necessary to deploy websites on local
|-- README.md
|-- _config.yml - website config including theme and plugins
|-- _data
|   `-- navigation.yml - items in the navigation bar
|-- _pages - individual pages
|   |-- about.md
|   |-- data.md
|   |-- methodology.md
|   |-- projects.md
|   |-- publications.md
|   `-- team.md
|-- assets - uploaded items, by type
|   |-- animations
|   |   `-- footprint_test_201605_marker.gif
|   |-- css - colors and fonts setup, overrides the template colours 
|   |   `-- main.scss
|   `-- images
|       `-- sahara_fp_1.png
|-- how_tos - folder with little guides
|   |-- editing.md
|   `-- local_development.md
|-- index.md - landing page
```

### Adding a page and page fomat
Each page .md file should start with the following structure:
```markdown
---
layout: single
title: "Page name"
permalink: /pagename/
---
Page content here
```
Each will be a website published at `gates-lab.github.io/pagename`

You can add a link to another page with a [relative link](/_pages/team.md) (`[relative link](/_pages/team.md)`) or a link to another website.

### Adding images to a page

Use images from the `assets/images/` folder so paths stay consistent.

1. Basic image in Markdown

```markdown
![Short description of image](/assets/images/my_figure.png)
```

2. Image with a set size (use HTML inside Markdown)

```html
<img src="/assets/images/my_figure.png" alt="Short description of image" width="500">
```

3. Responsive image (recommended for mixed desktop/mobile viewing)

```html
<img src="/assets/images/my_figure.png" alt="Short description of image" style="max-width: 70%; height: auto;">
```

4. Wrap text around an image

```html
<img src="/assets/images/my_figure.png" alt="Short description of image" style="float: right; width: 260px; margin: 0 0 1rem 1rem;">

Your paragraph text starts here and will wrap around the image.
Add as much text as needed.

<div style="clear: both;"></div>
```

Notes:
- Always include `alt` text for accessibility.
- Use leading `/` in image paths (for example `/assets/images/...`) so links work from any page.



