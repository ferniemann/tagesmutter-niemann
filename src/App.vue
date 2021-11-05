<template>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css" integrity="sha384-DyZ88mC6Up2uqS4h/KRgHuoeGwBcD4Ng9SiP4dIRy0EXTlnuz47vAwmeGwVChigm" crossorigin="anonymous">
  <Header />
  <router-view/>
</template>

<script>
import Header from "@/components/Header.vue"
export default {
  components: {
    Header
  }
}
</script>

<style>
@import url(https://fonts.googleapis.com/css?family=Schoolbell:regular);
@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,regular,500,600,700,800,300italic,italic,500italic,600italic,700italic,800italic);

*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --color-main: #94778B;
  --color-main-op: rgba(148 119 139 / .8);
  --color-bg: #82D4BB;
  --color-accent-dark: #829298;
  --color-accent-light: #82C09A;
  --color-light: white;
  --color-dark: black;
  --bp-tablet: 768px;
  --bp-desktop: 900px;
}

html {
  font-family: 'Open Sans';
}

a {
  text-decoration: none;
  color: currentColor;
}

h1, h2, h3, h4, h5, h6 {
  color: var(--color-main);
  font-family: 'Schoolbell';
  text-transform: uppercase;
  letter-spacing: .1em;
  text-shadow: 0.05em 0.05em var(--color-light);
}

p {
  line-height: 1.8;
}

body {
  overflow-y: scroll;
  color: var(--color-dark);
}

@media screen and (min-width: 768px) {
  html {
    font-size: 20px;
  }
}
</style>
