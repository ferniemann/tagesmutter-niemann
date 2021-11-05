<template>
<div class="navigation">
  <label for="toggle-nav" class="toggle-label">Menu</label>
  <input type="checkbox" name="" id="toggle-nav" class="toggle-nav">
  <nav>
      <router-link to="/">Startseite</router-link>
      <router-link to="/kontakt">Kontakt</router-link>
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
    }
}
</script>

<style>
.navigation {
    text-align: center;
    position: absolute;
    background-color: var(--color-bg);
    left: 0;
    right: 0;
    justify-content: center;
    align-items: center;
    padding: .5rem 0;
    z-index: 10;
}

.toggle-nav {
    all: unset;
}

.toggle-label {
    color: var(--color-light);
    font-size: 1rem;
    margin-right: .5rem;
    cursor: pointer;
}

.toggle-nav::before {
    content: "";
    display: inline-block;
    cursor: pointer;
    width: 1rem;
    height: 2px;
    padding: 2px;
    border-bottom: 2px solid var(--color-light);
    border-top: 2px solid var(--color-light);
}

.toggle-nav:checked::before {
    content: "X";
    border-color: transparent;
    color: var(--color-light);
    font-size: 1rem;
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

.toggle-nav:checked + nav {
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