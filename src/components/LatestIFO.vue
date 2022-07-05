<template>
    <section class="latest__ifo">
        <h2 class="heading">Latest <span class="text-primary">IFO</span></h2>
        <div class="card__component">
            <div class="label__wrapper">
                <span class="label right bold">Coming Soon</span>
            </div>
            <h2>Lorem ipsum</h2>
            <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tempor,</span>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tempor, justo vel dapibus hendrerit,
                dolor enim feugiat purus, quis congue eros
                lacus varius est. Donec vitae pellentesque nisi. Duis sodales eget nibh sed tristique. Donec et nibh
                velit. Sed mollis cursus neque, non
                dapibus erat vestibulum rutrum.
            </p>
            <div class="flex__container">
                <div class="timer">
                    <stopWatch />
                    <div class="timer__text">
                        <span>Sale Starts in</span>
                        <span class="text-primary">10D 25 Mins 23 Seconds</span>
                    </div>
                </div>
                <div class="timer">
                    <svg width="60" height="60" viewBox="0 0 60 60" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="29.6445" cy="30.498" r="28.5" stroke="#00E8A2" stroke-width="2" />
                    </svg>
                    <div class="timer__text">
                        <span>ON SALE</span>
                        <span class="text-primary bold">20,000,000 GOAL</span>
                    </div>
                </div>
                <Button msg="Connect Wallet" class="btn-primary mt-2">
                    <AddIcon class="icon" />
                </Button>
            </div>
            <div class="flex">
                <div class="text__container">
                    <span class="semibold">$600,000 MMF</span>
                    <span class="light">Funds to raise: </span>
                </div>
                <div class="text__container">
                    <span class="semibold">6 Hours</span>
                    <span class="light">Launchpad duration: </span>
                </div>
                <div class="text__container">
                    <span class="semibold">0.03</span>
                    <span class="light">Price per GOAL: </span>
                </div>
                <div class="text__container">
                    <span class="semibold">20th March, 8am UTC</span>
                    <span class="light">Launchpad starts at: </span>
                </div>
                <div class="text__container">
                    <span class="semibold">20th March, 2pm UTC</span>
                    <span class="light">Launchpad ends at: </span>
                </div>
            </div>
            <div class="buttons">
                <Button msg="Learn more about Lorem ipsum" class="btn" />
                <Button msg="Lorem ipsum Project Site" class="btn" />
            </div>
        </div>
    </section>
</template>

<script>
import AddIcon from '../assets/icons/add-icon.vue';
import stopWatch from '../assets/icons/stop-watch.vue';
import Button from './Button.vue';
export default {
    components: { stopWatch, AddIcon, Button },
};
</script>

<style lang="scss" scoped>
.latest__ifo {
    margin-top: 10rem;
    background-image: url("../assets/images/bg-latestIfo.svg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    padding: 0 8rem;

    .card__component {
        position: relative;
        padding: 310px 2rem 2rem 2rem;
        background: linear-gradient(180deg, #000000 28.13%, rgba(0, 0, 0, 0.5) 66.15%);
        border: 1px solid #5dfdb0;
        backdrop-filter: blur(1px);
        border-radius: 10px;
        overflow: hidden;
        min-height: 1500px;
        max-width: 820px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        @media (max-width: 768px) {
            margin: 0 1rem;
        }


        p {
            font-weight: 300;
        }

        h2 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .label__wrapper {
            right: 0px;
            position: absolute;
            top: 0px;
            /* Size */
            height: 200px;
            width: 200px;

            /* Hide the part of its children which is displayed outside */
            overflow: hidden;

            .label {
                right: -68px;
                position: absolute;
                top: 50px;

                /* Size */
                height: 34px;
                width: 300px;

                /* Displayed diagonally */
                transform: rotate(45deg);

                /* Background color */
                background: linear-gradient(225.09deg, #00E8A2 25.04%, #00ADE8 94.09%);
                box-shadow: -9px 4px 11px rgba(0, 0, 0, 0.51);

                /* Centerize the text content */
                text-align: center;
                font-size: 1.6rem;
                color: #000000;
            }
        }

        .flex__container {
            display: flex;
            margin-top: 2rem;
            flex-direction: column;

            .timer {
                display: flex;
                margin-top: 2rem;

                .timer__text {
                    display: flex;
                    justify-content: center;
                    flex-direction: column;
                    margin-left: 2rem;
                }
            }
        }

        .flex {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

            .text__container {
                margin: 0rem 3rem;
                display: flex;
                justify-content: space-between;
                margin-top: 2rem;
                flex-direction: column;
            }
        }
    }

    .buttons {
        display: flex;
        justify-content: space-between;
        margin-top: 2rem;
        flex-wrap: wrap;
    }

    @media screen and (max-width: 768px) {
        padding: 0;
    }

}
</style>
