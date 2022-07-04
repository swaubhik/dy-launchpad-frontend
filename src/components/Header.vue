<template>
    <header class="header">
        <div class="header__logo">
            <h1>IFO: Initial Farm Offerings</h1>
            <p>Buy new tokens launching on Chain</p>
            <div class="header__buttons">
                <button class="btn">How does it work?</button>
                <button class="btn-primary">Participate Now
                    <right-arrow class="arrow" />
                </button>
            </div>
        </div>
    </header>
</template>

<script>
import rightArrow from '../assets/icons/right-arrow.vue'
export default {
    components: { rightArrow },
}
</script>

<style>
.header__logo {
    background-image: url('../assets/images/bg-header.webp');
    background-repeat: no-repeat;
    background-size: 100% 100%;
    padding: 5rem 4rem;
}

.header__buttons {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 5rem;
}

.btn {
    padding: 1rem 2rem;
    color: #FFFFFF;
    background: rgba(0, 0, 0, 0.5);
    border: 1px solid #FFFFFF;
    backdrop-filter: blur(1px);
    border-radius: 10px;
}

.btn-primary {
    background-color: var(--color-primary);
    border-radius: 10px;
    border-color: var(--color-primary);
    padding: 1rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.arrow {
    height: 1.2rem;
    width: 3rem;
    margin-left: 1rem;
}



/* mobile */
@media (max-width: 768px) {
    .header__logo {
        background-size: cover;
    }

    .header__buttons {
        flex-direction: column;
    }

    .btn {
        margin-bottom: 4rem;
        padding: 1rem 3.5rem;
    }
}
</style>     