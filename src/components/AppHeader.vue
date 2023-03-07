<script>
export default {
    name: 'AppHeader',
    //components
    data() {
        return {

        }
    }

}

</script>

<template>
    <nav class="navbar navbar-expand-lg bg-light">
        <div class="container">
            <a class="navbar-brand" href="#">'Team5 Books'</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
                aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNavDropdown">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link :to="{ name: 'home' }" class="nav-link"
                            :class="this.$route.name === 'home' ? 'active' : ''">Home</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{ name: 'index' }" class="nav-link"
                            :class="this.$route.name === 'index' ? 'active' : ''">Books</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link :to="{ name: 'AboutUs' }" class="nav-link"
                            :class="this.$route.name === 'AboutUs' ? 'active' : ''">About Us</router-link>
                    </li>

                </ul>
            </div>
        </div>
    </nav>
</template>

<style scoped lang="scss"></style>