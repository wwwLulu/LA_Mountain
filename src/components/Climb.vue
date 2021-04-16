<template>
    <div id="climb" class="container">
        <div class="container__heading">
            <div class="heading">
                <h2 class="heading__number">02</h2>
                <div class="heading__number--aside">
                    <p>Climb</p>
                    <div class="square"></div>
                </div>
            </div>
            <p class="heading__paragraph">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis,
                harum nemo maxime veritatis incidunt totam aliquid nesciunt
                earum voluptatem natus officia quos obcaecati delectus
                recusandae?
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    position: relative;
    z-index: -1;
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    &__heading {
        margin: 0 auto;
        width: 70%;
        display: flex;
        flex: 0 0 100%;
        padding: 1rem 0;
        padding-bottom: 2rem;
        @media (max-width: 800px) {
            flex-direction: column;
            padding-bottom: 5rem;
        }
    }
}
.heading {
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
        display: flex;
        justify-content: center;
        align-items: center;
        padding-left: 2rem;
        max-width: 814px;
        max-height: 339px;
        font-size: 2.4rem;
        line-height: 2.4rem;
        color: #000000;
        font-weight: 300;
        font-family: 'Lato';
    }
}
</style>
