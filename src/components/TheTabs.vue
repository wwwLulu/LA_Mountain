<template>
    <div class="container">
        <div class="container-2">
            <p @click="tab = true" class="tab" :class="{ 'tab--active': tab }">
                MOUNTAIN 1
            </p>
            <p
                @click="tab = false"
                class="tab"
                :class="{ 'tab--active': !tab }"
            >
                MOUNTAIN 2
            </p>
        </div>
    </div>
    <TabContent :background="tab ? 'Tab_1.png' : 'Tab_2.png'" />
</template>

<script>
import TabContent from '@/components/TabContent'

export default {
    components: {
        TabContent,
    },
    data() {
        return {
            tab: true,
        }
    },
}
</script>

<style lang="scss" scoped>
.container {
    width: 100%;
    background: var(--primary-color);
    display: flex;
    justify-content: center;
}

.container-2 {
    display: flex;
    width: 70%;
}

.tab {
    cursor: pointer;
    font-size: 2rem;
    font-weight: 700;
    font-family: 'Oswald';
    font-weight: bold;
    padding: 1rem 1rem;
    color: #aab0bd;
    margin: 0 1rem;
    &--active {
        background: #aab0bd;
        text-decoration: underline;
        color: var(--primary-color);
    }
}
</style>
