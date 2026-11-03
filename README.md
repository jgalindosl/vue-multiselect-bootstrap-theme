# Bootstrap 3/4/5 theme for [vue-multiselect](https://vue-multiselect.js.org/)

Compiled from different comments on this [github issue](https://github.com/shentao/vue-multiselect/issues/718)

## Installation

    npm install vue-multiselect-bootstrap-theme

## Usage

Include the scss stylesheet into your main styles file, after the `vue-multiselect.min.css` file. Include the version that matches your bootstrap version (3,4,5)

```scss
@import "vue-multiselect/dist/vue-multiselect.min.css";
@import "vue-multiselect-bootstrap-theme/dist/vue-multiselect-bootstrap4.scss";
```

The theme imports Bootstrap without the webpack `~` prefix, so it works with Vite, Dart Sass (`--load-path=node_modules`), sass-loader >= 8 and other modern toolchains. Existing webpack projects that import it with `~vue-multiselect-bootstrap-theme/...` keep working.

### Legacy toolchains

If your toolchain can only resolve `node_modules` imports with the `~` prefix (e.g. sass-loader < 8), use the `legacy` entry points instead:

```scss
@import "~vue-multiselect-bootstrap-theme/dist/legacy/vue-multiselect-bootstrap4.scss";
```

### Customizing

All theme variables use `!default`, so you can override them before importing the theme. If you already import Bootstrap's functions and variables yourself, you can import only the theme partial:

```scss
@import "vue-multiselect-bootstrap-theme/dist/themes/bootstrap5";
```
