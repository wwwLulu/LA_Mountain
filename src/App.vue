<template>
    <TheHeader />
    <StickyNav />
    <History />
    <Climb />
    <TheTabs />
    <TheFooter />
</template>

<script>
import TheHeader from '@/components/TheHeader'
import StickyNav from '@/components/StickyNav'
import History from '@/components/History'
import Climb from '@/components/Climb'
import TheTabs from '@/components/TheTabs'
import TheFooter from '@/components/TheFooter'

export default {
    name: 'App',
    components: {
        TheHeader,
        StickyNav,
        History,
        Climb,
        TheTabs,
        TheFooter,
    },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
:root {
    --primary-color: #3d506d;
    --number-color: #414f6bb7;
}
html {
    scroll-behavior: smooth;
    font-size: 62.5%;
    @media (max-width: 800px) {
        font-size: 50%;
    }
}

* {
    margin: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Lato', sans-serif;
}
</style>
