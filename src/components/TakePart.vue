<template>
    <section class="take__part">
        <h2 class="heading">How to <span class="text-primary">Take Part?</span></h2>
        <div class="container">
            <div class="progress">
                <div class="gradient">1</div>
                <div class="number">2</div>
                <div class="number">3</div>
                <div class="number">4</div>
            </div>
            <div class="Profile card">
                <div class="gradient__border">
                    <h2 class="text-primary">Activate your Profile</h2>
                    <p class="light">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tempor, justo vel
                        dapibus
                        hendrerit,</p>
                    <Button msg="Connect Wallet" class="btn-primary">
                        <AddIcon class="icon" />
                    </Button>
                </div>
            </div>
            <div class="pool card">
                <div class="gradient__border">
                    <h2 class="text-primary">Stake in IFO pool</h2>
                    <p class="light">Nulla neque nulla, varius in sodales eget, rhoncus vel felis. Duis interdum, nulla
                        ac pellentesque imperdiet, libero odio vehicula turpis, nec eleifend urna ex in tortor. Cras
                        vitae augue risus. Orci varius natoque penatibus et magnis dis parturient montes, nascetur
                        ridiculus mus. Quisque sit amet mauris gravida nulla facilisis volutpat. Curabitur in libero
                        dolor. </p>
                    <a href="#">How is the IFO credit calculated?</a>
                </div>
            </div>
            <div class="commit card">
                <div class="gradient__border">
                    <h2 class="text-primary">Commit</h2>
                    <p class="light">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tempor, justo vel
                        dapibus hendrerit, </p>
                </div>
            </div>
            <div class="tokens card">
                <div class="gradient__border">
                    <h2 class="text-primary">Claim your tokens and achievement</h2>
                    <p class="light">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec tempor, justo vel
                        dapibus hendrerit, </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import AddIcon from '../assets/icons/add-icon.vue'
import Button from './Button.vue'
export default {
    components: { Button, AddIcon },

}
</script>

<style lang="scss" scoped>
.take__part {
    margin-top: 8rem;
    padding: 2rem 8rem;
    position: relative;
    background: url('../assets/images/bg-takePart.svg');
    background-size: cover;
    background-position: center;
    z-index: -10;
}

.container {
    font-weight: 700;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr;
    gap: 0px 0px;
    grid-auto-flow: row;
    grid-template-areas:
        ". progress Profile"
        "pool progress ."
        ". progress commit"
        "tokens progress .";

    .progress {
        grid-area: progress;
        display: flex;
        flex-direction: column;
        position: relative;
        justify-content: space-around;
        align-items: center;
        font-size: 2rem;

        &:after {
            content: ' ';
            background: linear-gradient(180deg, rgba(0, 173, 232, 0) -2.23%, rgba(0, 232, 162, 0.71) 45.71%, rgba(0, 173, 232, 0.71) 84.6%);
            border-radius: 10px;
            display: block;
            height: 4rem;
            width: 10px;
            position: absolute;
            top: 11rem;
            left: 50%;
            transform: translateX(-50%);
            z-index: -1;

            // mobile
            @media (max-width: 768px) {
                top: 15rem;
            }

            // tablet
            @media (min-width: 768px) and (max-width: 1180px) {
                top: 12rem;
            }
        }

        &:before {
            content: ' ';
            background: rgba(0, 0, 0, 0.75);
            border: 1px solid rgba(0, 232, 162, 0.25);
            border-radius: 10px;
            display: block;
            width: 10px;
            position: absolute;
            top: 10rem;
            bottom: 10rem;
            left: 50%;
            transform: translate(-50%);
            z-index: -2;

            // mobile
            @media (max-width: 768px) {
                top: 15rem;
                bottom: 15rem;

            }

            // tablet
            @media (min-width: 768px) and (max-width: 1180px) {
                top: 11rem;
                bottom: 11rem;
            }
        }

        .gradient {
            color: #000000;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 5rem;
            height: 5rem;
            border-radius: 50%;
            background: linear-gradient(225.09deg, #00E8A2 25.04%, #00ADE8 94.09%);
            box-shadow: -8px 14px 17px rgba(0, 0, 0, 0.25);

            &:before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: linear-gradient(225.09deg, rgba(0, 232, 162, 0.5) 25.04%, rgba(0, 173, 232, 0.5) 94.09%);
                filter: blur(25px);
                z-index: -1;

            }
        }

        .number {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 5rem;
            height: 5rem;
            border-radius: 50%;
            background: #000000;
            border: 1px solid rgba(0, 232, 162, 0.5);

        }


    }

    .Profile {
        grid-area: Profile;
    }

    .pool {
        grid-area: pool;
    }

    .commit {
        grid-area: commit;
    }

    .tokens {
        grid-area: tokens;
    }

    .card {
        display: flex;
        justify-content: center;
        align-items: center;

        .gradient__border {
            background:
                linear-gradient(rgba(0, 0, 0, 0.896), rgba(0, 0, 0, 0.94)) padding-box,
                linear-gradient(225.09deg, #00E8A2 25.04%, #00ADE8 94.09%) border-box;
            border-radius: 10px;
            border: 1px solid transparent;
            padding: 2rem;
            box-shadow: 0px 14px 17px 20px rgba(0, 0, 0, 0.15);
            backdrop-filter: blur(5px);

            a {
                text-decoration: underline;
                cursor: pointer;
            }
        }
    }

}

// mobile
@media (max-width: 768px) {
    .take__part {
        padding: 0 1rem;
    }
    .container {
        position: relative;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr 1fr;
        gap: 0 1rem;
        grid-template-areas:
            "progress Profile"
            "progress pool"
            "progress commit"
            "progress token";

        .progress {
            grid-area: progress;
        }

        .Profile {
            grid-area: Profile;
        }

        .pool {
            grid-area: pool;
        }

        .commit {
            grid-area: commit;
        }

        .tokens {
            grid-area: token;
        }
    }
}

// tablet
@media (min-width: 768px) and (max-width: 1024px) {
    .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr 1fr;
        gap: 0px 0px;
        grid-template-areas:
            "progress Profile"
            "progress pool"
            "progress commit"
            "progress token";

        .progress {
            grid-area: progress;
        }

        .Profile {
            grid-area: Profile;
        }

        .pool {
            grid-area: pool;
        }

        .commit {
            grid-area: commit;
        }

        .tokens {
            grid-area: token;
        }
    }

}
</style>