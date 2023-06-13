# styles

In Vue 3, you can define component styles using various approaches. Let's explore three common methods: inline styles, scoped styles, and CSS modules.

## Inline Styles:
Inline styles allow you to define component styles directly in the template using the style attribute. Here's an example:

```vue
<template>
  <div :style="{
    backgroundColor: 'red',
    color: 'white',
    padding: '10px'
  }">
    Inline Styles Example
  </div>
</template>
```

In this example, the div element has a red background color, white text color, and 10 pixels of padding.

## Scoped Styles:
Scoped styles isolate the component's styles to affect only the component's elements. You can achieve this by using the scoped attribute in the <style> tag of the component. Here's an example:

```vue
<template>
  <div class="scoped-example">
    Scoped Styles Example
  </div>
</template>

<style scoped>
.scoped-example {
  background-color: blue;
  color: white;
  padding: 10px;
}
</style>
```
In this case, the styles defined within the <style> tag will only be applied to the elements inside the component template. This helps prevent style conflicts between components.

## CSS Modules:
CSS Modules provide local scoping of styles by generating unique class names for each component. You need to configure your build tool (e.g., webpack) to use CSS Modules. Here's an example:  

```vue
<template>
  <div :class="$style.moduleExample">
    CSS Modules Example
  </div>
</template>

<style module>
.moduleExample {
  background-color: green;
  color: white;
  padding: 10px;
}
</style> 
```

In this case, the $style object is automatically generated, and the class name moduleExample is scoped to the component. You can access it using the $style object.

Note: To use CSS Modules, you need to configure your project and build tool accordingly. The exact configuration steps might differ depending on your setup.

These are three common ways to apply styles in Vue 3: inline styles, scoped styles, and CSS Modules. Each approach has its advantages and use cases, so choose the one that best suits your project requirements.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
