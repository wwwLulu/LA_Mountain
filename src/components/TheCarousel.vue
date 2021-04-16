<template>
    <div class="carousel">
        <div class="container">
            <div class="carousel__images">
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
            </div>
            <div class="carousel__dots">
                <div
                    @click="showGroup1"
                    class="carousel__dot"
                    :class="{
                        'carousel__dot--active':
                            accordion_1 ||
                            (!accordion_1 && !accordion_2 && !accordion_3),
                    }"
                ></div>
                <div
                    @click="showGroup2"
                    class="carousel__dot"
                    :class="{ 'carousel__dot--active': accordion_2 }"
                ></div>
                <div
                    @click="showGroup3"
                    class="carousel__dot"
                    :class="{ 'carousel__dot--active': accordion_3 }"
                ></div>
            </div>
        </div>
    </div>
    <div class="accordion">
        <div
            @click="closeAll"
            v-if="accordion_1 || accordion_2 || accordion_3"
            class="accordion__title"
        >
            CLOSE
        </div>
        <div class="accordion--1">
            <div @click="showGroup1" class="accordion__title">1</div>
            <div class="images" :class="{ active: accordion_1 }">
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
            </div>
        </div>
        <div class="accordion--2">
            <div @click="showGroup2" class="accordion__title">2</div>
            <div class="images" :class="{ active: accordion_2 }">
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
            </div>
        </div>
        <div class="accordion--3">
            <div @click="showGroup3" class="accordion__title">3</div>
            <div class="images" :class="{ active: accordion_3 }">
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_1.png" alt="" />
                </div>
                <div class="img-container">
                    <img src="../assets/Carousel_2.png" alt="" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            accordion_1: false,
            accordion_2: false,
            accordion_3: false,
        }
    },
    mounted() {},
    methods: {
        closeAll() {
            this.accordion_1 = false
            this.accordion_2 = false
            this.accordion_3 = false
        },
        showGroup1() {
            this.accordion_1 = true
            this.accordion_2 = false
            this.accordion_3 = false
        },
        showGroup2() {
            this.accordion_1 = false
            this.accordion_2 = true
            this.accordion_3 = false
        },
        showGroup3() {
            this.accordion_1 = false
            this.accordion_2 = false
            this.accordion_3 = true
        },
    },
}
</script>

<style lang="scss" scoped>
.active {
    display: flex !important;
    flex: 0 1 100%;
    flex-wrap: wrap;
}

.accordion {
    @media (min-width: 1200px) {
        display: none;
    }
    cursor: pointer;
    position: absolute;
    bottom: 0;
    z-index: 10000;
    *:not(:last-child) {
        border-bottom: 1px solid white;
    }
    .images {
        display: none;
        .img-container {
            // width: 30rem;
            flex: 1 1;
            img {
                object-fit: cover;
                object-position: center;
                width: 100%;
                height: 100%;
            }
        }
    }
    &__title {
        padding: 1rem 0;
        color: white;
        width: 100vw;
        background: var(--primary-color);
        text-align: center;
        font-size: 3rem;
        transition: background 0.3s, color 0.3s;
        &:hover {
            cursor: pointer;
            background: white;
            color: var(--primary-color);
        }
    }
}

.carousel {
    @media (max-width: 1200px) {
        display: none;
    }
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100vw;
    height: 25rem;
    background: rgba(61, 80, 109, 0.8);
    &__images {
        width: 100%;
        display: flex;
        justify-content: space-between;
        .img-container {
            // width: 20%;
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: center;
            }
        }
    }
    &__dots {
        margin-top: 1rem;
        display: flex;
    }
    &__dot {
        cursor: pointer;
        margin: 0 0.5rem;
        background: grey;
        width: 1rem;
        height: 1rem;
        border-radius: 50%;
        &--active {
            background: white;
        }
    }
}
.container {
    width: 70%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}
</style>
