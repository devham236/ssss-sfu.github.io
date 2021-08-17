# Software Systems Student Society Website

|     | Version | Release Date      | Main Developer |
| --- | ------- | ----------------- | -------------- |
| ✅  | v2.0    | August 17, 2021   | Kiaan Castillo |
|     | v1.0    | November 17, 2020 | Andy Wang      |

## General Structure

- `assets`: Anything that is put on the site that is not code
- `pages`: HTML files of all the pages that the site has
- `styles`: All CSS files go in here (more [in depth explanation can be read here](#file-structure))
- `index.html`: Landing page of the site

```
.
├── assets/
│   └── ...
├── pages/
│   └── ...
├── styles/
│   ├── sass/
│   │   └── ...
│   └── main.min.css
├── .gitignore
├── favicon.ico
├── index.html
└── README.md
```

## CSS

SASS, more specifically SCSS, is used as the CSS pre-compiler for this project for its easy modularization capabilities. Everything was made from scratch and according to the SSSS brand guidelines and design system (Figma file coming soon).

### File Structure

- `components`: Styles for components
- `layouts`: Styles for things like wrapper classes that dictate layouts and page structure
- `utilities`: Styles for buttons, fonts, and colours that are used globally
- `main.scss`: Main SCSS file that brings everything together. Whenever a new stylesheet is added to the `components` folder, it should be linked in here using the `@use` rule.

```
styles/
└── sass/
    ├── components/
    │   └── ...
    ├── layouts/
    │   └── ...
    ├── utilities/
    │   └── ...
    └── main.scss
```

### SCSS to CSS

Run this command to process `main.scss` into a compressed `main.min.css` file

```
sass main.scss ../main.min.css --style=compressed
```

This produces one CSS file that is a compressed, compilation of all of the SCSS files. All HTML files then link to this compressed CSS file.
