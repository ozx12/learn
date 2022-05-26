<template>
       <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">Марвел</a>

            <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">

                <form class="d-flex justify-content-end" role="search">
                    <input class="form-control me-2" type="search" placeholder="Поиск" aria-label="Search">
                    <button class="btn btn-primary" type="submit">Все</button>
                </form>
            </div>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "AppHeader",
        data() {
            return {
            }
        },
    }
</script>

<style scoped>

</style>
