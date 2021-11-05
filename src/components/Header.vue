<template>
<header>
    <div class="logo">
        <h1 class="title">Tagesmutter <span>Regina Niemann</span></h1>
        <h2 class="sub-title">Kindertagespfelege für Ratzeburg und Umland</h2>
    </div>
    <Navigation />
</header>
</template>

<script>
import Navigation from "@/components/Navigation.vue"
export default {
    name: "Header",
    components: {
        Navigation
    }
}
</script>

<style>
    header {
        padding: 1rem 0;
        background-color: var(--color-bg);
        margin-bottom: 1rem;
    }

    .logo {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .title {
        font-size: 2rem;
    }

    .title span {
        display: block;
        color: var(--color-light);
        text-shadow: 0.05em 0.05em var(--color-main);
    }

    .sub-title {
        font-size: .75rem;
        font-family: "Open Sans";
        font-weight: 400;
        text-shadow: none;
        color: var(--color-light);
        background-color: var(--color-main);
        padding: .1rem .2rem;
        border-radius: .5rem;
        letter-spacing: 0;
    }

    @media screen and (min-width: 768px) {
        header {
            display: flex;
            flex-direction: column;
            margin-bottom: 0;
        }
    }

    @media screen and (min-width: 1000px) {
        header {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-evenly;
        }
    }
</style>