<template>
    <div class="navMenu">

        <nav class="navbar navbar-expand-lg bg-light">
            <div class="container-fluid">
                <router-link to="/home" class="navbar-brand">PatoFlix</router-link>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                    aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <router-link to="/home" class="nav-link active">Home</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link to="/about" class="nav-link active">About</router-link>
                        </li>
                    </ul>
                    <form class="d-flex" role="search">
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item">
                                <router-link to="/" class="nav-link active" @click="exitSystem()">Sair</router-link>
                            </li>
                        </ul>
                    </form>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'navMenu',
    methods: {
        exitSystem(){
            localStorage.setItem('loged', false);
            this.$router.push('/')
        }
    },

}
</script>

<style>

</style>