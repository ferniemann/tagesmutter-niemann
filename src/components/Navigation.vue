<template>
<div class="navigation">
  <input type="checkbox" name="" id="toggle-nav" class="toggle-nav">
  <label for="toggle-nav" class="toggle-label">
      <div class="hamburger hamburger-upper"></div>
      <div class="hamburger hamburger-middle"></div>
      <div class="hamburger hamburger-lower"></div>
  </label>
  <nav>
      <router-link to="/" class="menu-link" @click="collapseMenu()">Startseite</router-link>
      <router-link to="/kontakt" class="menu-link" @click="collapseMenu()">Kontakt</router-link>
  </nav>
</div>
</template>

<script>
export default {
    name: "Navigation",
    data() {
        return {
            test: "Test"
        }
    },

    methods: {
        collapseMenu() {
            const toggle = document.getElementById("toggle-nav")

            if (toggle.checked) {
                toggle.checked = false
            }
        }
    }
}
</script>

<style>
.navigation {
    text-align: center;
    left: 0;
    right: 0;
    justify-content: center;
    align-items: center;
    padding: .5rem 0;
    z-index: 10;
}

.toggle-label {
    display: flex;
    flex-direction: column;
    margin-top: 1rem;
    transition: .2s;
}

.hamburger {
    width: 2rem;
    height: 2px;
    background-color: var(--color-light);
    margin: 0 auto;
    margin-bottom: .5rem;
}

.toggle-nav {
    all: unset;
    displaY: none;
}

.toggle-label {
    color: var(--color-light);
    font-size: 1rem;
    margin-right: .5rem;
    cursor: pointer;
}

nav {
    display: none;
}

nav a {
    padding: .5rem 1rem;
    color: var(--color-light);
    background: var(--color-accent-dark);
    width: 40%;
    margin: .5rem auto;
    border-radius: .5rem;
}

.toggle-nav:checked ~ nav {
    display: flex;
    flex-direction: column;
}

@media screen and (min-width: 768px) {
    .toggle-nav, .toggle-label {
        display: none;
    }

    .navigation {
        position: relative;
    }

    nav {
        display: flex;
        justify-content: center;
        gap: 1rem;
    }

    nav a {
        width: unset;
        transition: .2s;
        margin: unset;
        border: 2px solid transparent;
    }

    nav a:hover {
        background-color: var(--color-main);
        transition: .2s;
    }

    .router-link-active {
        border-color: white;
    }
}
</style>