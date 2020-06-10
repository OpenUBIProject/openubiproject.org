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

        <div class="sidebar-toggle d-lg-none" v-b-toggle.sidebar-right><span class="sidebar-toggle-icon"></span></div>
        <b-sidebar id="sidebar-right" title="OpenUBI" no-header right shadow>
            <template v-slot:default="{ hide }">
                <div>
                    <nav class="mb-3 sidebar-nav">
                        <b-nav vertical>
                            <slot>
                            </slot>
                            <hr />
                            <b-nav-item class="nav-item-first" href="#" @click="hide">Twitter</b-nav-item>
                            <b-nav-item href="#" @click="hide">Facebook</b-nav-item>
                            <b-nav-item href="#" @click="hide">Discord</b-nav-item>
                            <b-nav-item href="#" @click="hide">Github</b-nav-item>
                        </b-nav>
                    </nav>
                </div>
            </template>
        </b-sidebar>
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

.b-sidebar-outer {
    position: fixed;
    z-index: 1000;
    width: 85%;
    max-width: 400px;
    top: 82px;
    height: 100%;
}

.collapsed + .b-sidebar-outer {
    right: -401px;

    transition: linear 100ms;
}

.not-collapsed + .b-sidebar-outer {
    right: 0;

    transition: linear 100ms;
}

#sidebar-right {
    height: 100%;
    display: block !important;

    &:focus {
        outline: none;
    }
}

.sidebar-nav {
    width: 100%;
    position: absolute;

    .nav-item:first-of-type, .nav-item-first {
        margin-top: 10px;
        border-top: solid 1px rgba(0, 0, 0, 0.05);
    }

    .nav-item {
        text-align: left;
        border-bottom: solid 1px rgba(0, 0, 0, 0.05);

        .nav-link {
            font-size: 1.3rem;
            padding-top: 10px;
            padding-bottom: 10px;
        }

        .nav-link.active {
            background-color: hsla(0, 0%, 0%, 0.05);
        }
    }
}

.sidebar-toggle {
    position: fixed;
    z-index: 110;
    top: 14px;
    right: 16px;

    &:focus {
        outline: none;
    }
}

.sidebar-toggle-icon {
    display: inline-block;
    width: 2.5em;
    height: 2.5em;
    vertical-align: middle;
    content: "";
    background-size: 100% 100%;
    background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(255, 255, 255, 0.5)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 7h22M4 15h22M4 23h22'/%3E%3C/svg%3E");
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