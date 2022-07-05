<template>
    <section class="feed__back">
        <h2 class="heading">Frequently Asked <span class="text-primary">Questions</span></h2>
        <div class="container">
            <div class="logo">
                <Question />
            </div>
            <div class="questions">
                <Button msg="What’s the difference between a Public Sale and Private Sale?" class="btn">
                    <Chevron class="icon" />
                </Button>
                <Button msg="Which sale should I commit to? Can I do both?" class="btn">
                    <Chevron class="icon" />
                </Button>
                <Button msg="How much is the participation fee?" class="btn">
                    <Chevron class="icon" />
                </Button>
                <Button msg="Where does the participation fee go?" class="btn">
                    <Chevron class="icon" />
                </Button>
                <Button msg="How can I get an achievement for participating in the IFO?" class="btn">
                    <Chevron class="icon" />
                </Button>
            </div>
        </div>
    </section>
</template>

<script>
import Button from './Button.vue';
import Chevron from '../assets/icons/Chevron.vue';
import Question from '../assets/icons/Question.vue';
export default {
    components: { Button, Chevron, Question }
}
</script>

<style lang="scss" scoped>
.feed__back {
    padding: 0 8rem;

    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 2rem;

        @media screen and (max-width: 768px) {
            flex-direction: column;
        }

        @media (min-width: 768px) and (max-width: 1180px) {
            flex-direction: column;
        }

        .btn {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 600px;
            margin: 2rem 2rem;

            @media screen and (max-width: 768px) {
                margin-bottom: 1rem;
                width: 400px;
            }

            @media (min-width: 768px) and (max-width: 1180px) {
                width: 500px;
            }

            .icon {
                width: 1.5rem;
            }
        }
    }

    @media screen and (max-width: 768px) {
        padding: 0 1rem;
    }


}
</style>