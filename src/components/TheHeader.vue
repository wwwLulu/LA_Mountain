<template>
    <section class="header">
        <div class="header__navbar">
            <img src="../assets/Logo.svg" alt="logo" class="header__logo" />
            <nav class="header__navigation">
                <ul>
                    <a href="#history"><li>01. HISTORY</li></a>
                    <a href="#climb"><li>02. TEAM</li></a>
                </ul>
            </nav>
        </div>
        <div class="header__heading">
            <p class="header__heading--losangeles">LOSANGELES</p>
            <p class="header__heading--mountains">MOUNTAINS</p>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.header {
    position: relative;
    width: 100vw;
    height: 100vh;
    background-image: url('../assets/Header_Background.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    display: flex;
    flex-direction: column;
    align-items: center;
    &__navbar {
        width: 70%;
        padding: 1rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    &__navigation {
        ul {
            display: flex;
            list-style: none;
            justify-content: right;
        }
        li {
            cursor: pointer;
            margin: 0 1rem;
            color: white;
            text-decoration: underline;
            font-size: 1.4rem;
            font-weight: 900;
            font-style: italic;
        }
    }
    &__logo {
        width: 5rem;
        height: 5rem;
    }
    &__heading {
        margin-top: 20vh;
        letter-spacing: 1px;
        color: #4d4d4d;
        font-family: 'Bebas Neue', cursive;
        font-size: 13.5rem;
        @media (min-width: 1200px) {
            margin-left: -20rem;
        }
        @media (max-width: 800px) {
            font-size: 9rem;
        }
        &--losangeles {
            color: #4d4d4d;
        }
        &--mountains {
            margin-top: -4rem;
            background: #404f6b;
            background: linear-gradient(to bottom, #404f6b, #000000);
            background-clip: text;
            color: transparent;
        }
    }
}
</style>
