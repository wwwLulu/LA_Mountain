<template>
    <div class="container">
        <div class="navbar">
            <img
                src="../assets/StickyNavLogo.png"
                alt="logo"
                class="navbar__logo"
            />
            <nav class="navbar__navigation">
                <ul>
                    <a href="#history"><li>01. HISTORY</li></a>
                    <a href="#climb"><li>02. TEAM</li></a>
                </ul>
            </nav>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    width: 100%;
    display: flex;
    justify-content: center;
    position: sticky;
    top: 0;
    background: white;
    z-index: 50000;
}
.navbar {
    width: 70%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem;
    &__navigation {
        ul {
            display: flex;
            list-style: none;
            justify-content: right;
        }
        li {
            cursor: pointer;
            margin: 0 1rem;
            color: #3d506d;
            text-decoration: underline;
            font-size: 1.4rem;
            font-weight: 900;
            font-style: italic;
        }
    }
    &__logo {
        height: 3rem;
    }
}
</style>
