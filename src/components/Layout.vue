<template>
    <div class="layout">
        <Header />
        <main>
            <slot />
        </main>
        <Footer />
    </div>
</template>

<script>
import Header from './Header.vue';
import Footer from './Footer.vue';
export default {
    components: { Header, Footer }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;600;700&family=Oxygen:wght@700&display=swap');

:root {
    --color-primary: rgba(0, 232, 162, 1);
    --color-secondary: rgba(0, 173, 232, 1);
    margin: 0;
    padding: 0 2rem;
    box-sizing: border-box;
    font-family: 'Nunito', sans-serif;
    background-color: black;
    color: white;
}

a {
    color: inherit;
    text-decoration: inherit;
}
</style>