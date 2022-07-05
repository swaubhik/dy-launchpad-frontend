<template>
    <div class="layout">
        <Header />
        <main>
            <LatestIFO />
            <TakePart />
            <FAQ />
        </main>
        <Footer />
    </div>
</template>

<script>
import Header from './Header.vue';
import Footer from './Footer.vue';
import LatestIFO from './LatestIFO.vue';
import TakePart from './TakePart.vue';
import FAQ from './FAQ.vue';

export default {
    components: { Header, Footer, LatestIFO, TakePart, FAQ }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;600;700&family=Oxygen:wght@700&display=swap');

:root {
    --color-primary: rgba(0, 232, 162, 1);
    --color-secondary: rgba(0, 173, 232, 1);
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Nunito', sans-serif;
    font-style: normal;
    background-color: black;
    color: white;
}

* {
    box-sizing: border-box;
}

a {
    color: inherit;
    text-decoration: inherit;
}

.btn {
    padding: 1rem 2rem;
    color: #FFFFFF;
    background: rgba(0, 0, 0, 0.5);
    border: 1px solid #FFFFFF;
    backdrop-filter: blur(1px);
    border-radius: 10px;
}

.heading {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 5rem;
}

.btn-primary {
    background-color: var(--color-primary);
    border-radius: 10px;
    border-color: var(--color-primary);
    padding: 1rem 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

.icon {
    height: 1.2rem;
    width: 3rem;
    margin-left: 1rem;
}

.text-primary {
    color: var(--color-primary);
}

.mt-2 {
    margin-top: 2rem;
}

.bold {
    font-weight: 700;
}

.semibold {
    font-weight: 600;
}

.light {
    font-weight: 300;
    font-size: 0.8rem;
}

@media (max-width: 768px) {

    .btn {
        margin-bottom: 2rem;
        padding: 1rem 3.5rem;
    }
}
</style>