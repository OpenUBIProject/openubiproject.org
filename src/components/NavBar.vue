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
            </div>
        </b-navbar>
    </div>
</template>

<script>
    export default {
        name: 'NavBar'
    }
</script>