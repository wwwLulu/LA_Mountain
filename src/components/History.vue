<template>
    <div class="background"></div>
    <div id="history" class="container">
        <div class="container__heading">
            <div class="heading">
                <h2 class="heading__number">01</h2>
                <div class="heading__number--aside">
                    <p>HISTORY</p>
                    <div class="square"></div>
                </div>
            </div>
            <p class="heading__paragraph">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Deserunt exercitationem facilis magnam maiores officia possimus
                eveniet quam dolorem libero, sit accusamus voluptatum fugit
                doloribus autem, aspernatur neque architecto quae repudiandae
                corrupti vero laudantium? Iusto.
            </p>
        </div>
        <TheCarousel />
    </div>
</template>

<script>
import TheCarousel from '@/components/TheCarousel'

export default {
    components: {
        TheCarousel,
    },
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');
.background {
    z-index: -1;
    position: absolute;
    width: 100vw;
    min-height: 100vh;
    background-image: url('../assets/History_Background.png');
    background-size: cover;
}

.container {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    &__heading {
        margin: 0 auto;
        width: 70%;
    }
}
.heading {
    width: 70%;
    display: flex;
    &__number {
        font-size: 13.6rem;
        color: var(--number-color);
        font-weight: 700;
        font-family: 'Oswald', sans-serif;
    }
    &__number--aside {
        align-self: center;
        display: flex;
        flex-direction: column;
        margin-top: 5.5rem;
        p {
            font-size: 3.2rem;
            color: #414f6b;
            font-weight: 700;
            font-family: 'Oswald';
        }
        .square {
            width: 2rem;
            height: 2rem;
            background: var(--number-color);
        }
    }
    &__paragraph {
        max-width: 814px;
        max-height: 339px;
        line-height: 2.4rem;
        color: #000000;
        font-weight: 300;
        font-size: 2.4rem;

        font-family: 'Lato';
        margin-left: 7rem;
    }
}
</style>
