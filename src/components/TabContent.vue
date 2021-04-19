<template>
    <section>
        <img
            :src="require('../assets/' + background)"
            alt=""
            class="background"
        />
        <div class="container">
            <div class="card">
                <h2 class="card__heading">SCHEDULE</h2>
                <div class="card__details">
                    <p>{{ date1 }}</p>
                    <p>{{ date2 }}</p>
                    <br />
                    <p>{{ date3 }}</p>
                    <br />
                    <p>{{ date4 }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: ['background', 'date1', 'date2', 'date3', 'date4'],
};
</script>

<style lang="scss" scoped>
.background {
    z-index: -1;
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
}
section {
    position: relative;
    width: 100vw;
    height: 50rem;
    display: flex;
    justify-content: center;
}

.container {
    width: 65%;
}

.card {
    padding: 1rem 2rem;
    margin-top: 5rem;
    width: 30rem;
    background: rgba(255, 255, 255, 0.7);
    &__heading {
        font-size: 3.2rem;
        color: #414f6b;
        font-weight: 700;
        font-family: 'Oswald';
    }
    &__details {
        font-size: 1.6rem;
        line-height: 2.4rem;
        color: #000000;
        font-weight: 300;
        font-family: 'Lato';
    }
}
</style>
