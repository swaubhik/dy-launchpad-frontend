<template>
    <header class="header">
        <div class="header__logo">
            <h1>IFO: Initial Farm Offerings</h1>
            <p>Buy new tokens launching on Chain</p>
            <div class="header__buttons">
                <Button msg="How does it work ?" class="btn" />
                <Button msg="Participate now" class="btn-primary">
                    <right-arrow class="icon" />
                </Button>
            </div>
        </div>
    </header>
</template>

<script>
import rightArrow from '../assets/icons/right-arrow.vue'
import Button from './Button.vue'
export default {
    components: { rightArrow, Button },
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

/* mobile */
@media (max-width: 768px) {
    .header__logo {
        background-size: cover;
    }

    .header__buttons {
        flex-direction: column;
    }
}
</style>     