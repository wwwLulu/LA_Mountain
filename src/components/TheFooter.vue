<template>
    <footer class="footer">
        <div class="container">
            <img src="../assets/Footer_Logo.png" alt="" />
            <p>COPYRIGHT 2016. ALL RIGHTS RESERVED.</p>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.footer {
    background: var(--primary-color);
    height: 4.5rem;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    img {
        height: 3rem;
        padding: 0 1rem;
    }
    p {
        font-size: 1.2rem;
        letter-spacing: 1px;
        color: #63769d;
        font-weight: 900;
        font-style: italic;
        font-family: 'Lato';
    }
}

.container {
    width: 70%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>
