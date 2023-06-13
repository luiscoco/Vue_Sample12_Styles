<template>
  <div
    :style="{
      backgroundColor: 'red',
      color: 'white',
      padding: '10px',
    }"
  >
    Inline Styles Example
  </div>

  <div class="scoped-example">Scoped Styles Example</div>

  <div :class="$style.moduleExample">CSS Modules Example</div>
</template>

<style scoped>
.scoped-example {
  background-color: blue;
  color: white;
  padding: 10px;
}
</style>

<style module>
.moduleExample {
  background-color: green;
  color: white;
  padding: 10px;
}
</style>
