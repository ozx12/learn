<template>
    <div id="app">

        <app-header/>

        <div class="container">
            <h1 class="pt-3 pb-3">Персонажи Marvel</h1>

            <app-modal/>

            <spinner/>

            <div class="row">
                    <div class="col-lg-4 col-md-6 col-sm-12">

                <div class="card mb-3" style="max-width: 540px;">
                    <div class="row g-0">
                        <div class="col-md-4">
                            <img class="img-fluid rounded-start"
                                src="http://i.annihil.us/u/prod/marvel/i/mg/3/50/526548a343e4b.jpg" alt="Человек-паук">
                        </div>
                        <div class="col-md-8">
                            <div class="card-body">
                                <h5 class="card-title">Человек-паук</h5>

                                <button type="button" class="btn btn-primary" data-bs-toggle="modal"
                                    data-bs-target="#exampleModal">
                                    Подробнее
                                </button>
                            </div>
                        </div>
                    </div>
                </div>




            </div>
            </div>
        </div>

    </div>
</template>

<script>
    import Spinner from "./components/Spinner";
    import AppModal from "./components/AppModal";
    import AppHeader from "./components/AppHeader";

    export default {
        name: 'App',
        components: {
            AppHeader,
            AppModal,
            Spinner,
        },
        data() {
            return {
                loading: false,
                characters: [],
                characterIndex: 0,
            }
        },
        methods: {},
        computed: {},
    }
</script>

<style>

</style>
