<template>
    <div>
        <div class="navbar-anchor">
            <b-navbar toggleable="lg" type="dark" variant="primary">
                <div class="container">
                    <b-navbar-nav class="d-none d-lg-flex">
                        <slot></slot>
                    </b-navbar-nav>

                    <b-navbar-brand to="/" class="navbar-logo">
                        <img src="../assets/open-ubi-project-logo-solid.svg" alt="OpenUBI Project logo">
                    </b-navbar-brand>

                    <b-navbar-nav class="d-none d-lg-flex">
                        <b-nav-item href="#">Twitter</b-nav-item>
                        <b-nav-item href="#">Facebook</b-nav-item>
                        <b-nav-item href="#">Discord</b-nav-item>
                        <b-nav-item href="#">Github</b-nav-item>
                    </b-navbar-nav>
                </div>
            </b-navbar>
        </div>
        <div class="navbar-offset mb-n4 d-lg-none"></div>
    </div>
</template>

<script>
    export default {
        name: 'NavBar'
    }
</script>

<style lang="scss">
.navbar-anchor {
    position: fixed;
    width: 100%;
    z-index: 100;
    top: 0;
    height: 95px;
}

.navbar-offset {
    height: 95px;
}

.navbar-logo {
    position: relative;
    left: 50%;
    transform: translateX(-50%);

    img {
        max-height: 55px;
    }
}

.nav-link {
    font-size: 0.9rem;
}

@media (min-width: 992px) {
    .navbar-anchor {
        position: initial;
        height: initial;
    }

    .navbar-logo {
        position: initial;
        transform: initial;
    }
}

@media (min-width: 1200px) {
    .nav-link {
        font-size: 1rem;
    }
}
</style>