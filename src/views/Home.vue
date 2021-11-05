<template>
<div @click="collapseMenu()">
  <div class="hero">
    <img alt="Vue logo" src="../assets/img/spielecke_regal.jpg">
    <h2 class="hero-title">Kindertagespflege für Ratzeburg und Umland</h2>
    <h2 class="hero-action">Es sind noch Plätze frei!</h2>
  </div>
  <section class="call-to-action">
    <h2>Sichern Sie sich einen Platz</h2>
    <p>Kontaktieren Sie mich am Besten noch heute! Ich entlaste Sie gerne und übernehme mit Herz und Leidenschaft die Tagespflege Ihres Kindes oder Ihrer Kinder.</p>
    <router-link to="/kontakt" class="contact-button">Kontakt</router-link>
  </section>
</div>
</template>

<script>

export default {
  name: 'Home',
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

<style scoped>

img {
  max-width: 100%;
}

.hero {
  position: relative;
}

.hero-title {
  color: var(--color-light);
  background: var(--color-main-op);
  text-shadow: unset;
  padding: .5rem 1rem;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  text-align: center;
}

.hero-action {
  font-family: "Open Sans";
  color: var(--color-light);
  background-color: var(--color-bg);
  position: absolute;
  bottom: 10%;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  font-size: 1rem;
  border: 2px solid var(--color-main);
  border-radius: .2rem;
  text-shadow: unset;
  padding: .25em .5em;
}

.call-to-action {
  padding: 1rem;
}

.contact-button {
  background-color: var(--color-main);
  color: white;
  padding: .5rem 1rem;
  display: inline-block;
  border-radius: .2rem;
  margin-top: 1rem;
  margin: 0 auto;
}
@media screen and (min-width: 768px) {
  .hero img {
    height: 75vh;
    width: 100%;
    object-fit: cover;
    object-position: center -300px;
  }

  .hero-title {
    font-size: 2rem;
    border-radius: .2rem;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .hero-action {
    font-size: 1.25rem;
  }

  .call-to-action {
    padding: 2rem;
  }

  .call-to-action h2 {
    font-size: 2.5rem;
  }

  .call-to-action p {
    font-size: 1.75rem;
    margin: 3rem 0;
  }

  .contact-button {
    display: inline-block;
    font-size: 1.75rem;
    margin-top: 3rem;
  }
}
</style>