<template>
    <div>
        <b-navbar toggleable="lg" type="dark" variant="primary">
            <div class="container">
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav>
                        <slot></slot>
                    </b-navbar-nav>
                </b-collapse>

                <b-navbar-brand to="/">
                    <img class="navbar-logo" src="../assets/open-ubi-project-logo-solid.svg" alt="OpenUBI Project logo">
                </b-navbar-brand>

                <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav class="ml-auto">
                        <b-nav-item href="#">Twitter</b-nav-item>
                        <b-nav-item href="#">Facebook</b-nav-item>
                        <b-nav-item href="#">Discord</b-nav-item>
                        <b-nav-item href="#">Github</b-nav-item>
                    </b-navbar-nav>
                </b-collapse>
            </div>
        </b-navbar>
    </div>
</template>

<script>
    export default {
        name: 'NavBar'
    }
</script>

<style lang="scss">
.navbar-logo {
    max-height: 55px;
}

.nav-link {
    font-size: 0.9rem;
}

@media (min-width: 1200px) {
    .nav-link {
        font-size: 1rem;
    }
}
</style>