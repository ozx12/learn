<template>
  <div id="app">
    <app-header />

    <div class="container">
      <h1 class="pt-3 pb-3">Персонажи Marvel</h1>
     
      <app-modal />

      <spinner />

      <div class="row">
        <div v-for="el in characters" class="col-lg-4 col-md-6 col-sm-12">
          <div class="card mb-3" style="max-width: 540px">
            <div class="row g-0">
              <div class="col-md-4">
                <img
                  class="img-fluid rounded-start"
                  :src="el.thumbnail"
                  :alt="el.name"
                />
              </div>
              <div class="col-md-8">
                <div class="card-body">
                  <h5 class="card-title">{{el.name}}</h5>

                  <button
                    type="button"
                    class="btn btn-primary"
                    data-bs-toggle="modal"
                    data-bs-target="#exampleModal"
                  >
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
  name: "App",
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
    };
  },
  methods: {
    fetchCharacters: function () {
      fetch("https://netology-api-marvel.herokuapp.com/characters")
        .then((res) => res.json())
        .then((json) => (this.characters = json));
    },
  },
  computed: {},
  mounted(){
      this.fetchCharacters()
  }
};
</script>

<style>
</style>
