<template>
  <main>
      <section class="container">
          <div class="row">
              <div v-for="(album, index) in albums" :key="index" class="col-6 col-md-4 col-lg-2">
                  <Album :item="album" />
              </div>
          </div>
      </section>
  </main>
</template>

<script>
import Album from './Album.vue';
import axios from 'axios';

export default {
    name: "Main",
    components: {
        Album
    },
    data: function() {
        return {
            apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
            albums: []
        }
    },
    created: function() {
        axios
            .get(this.apiUrl)
            .then(
                (response) => {
                    this.albums = response.data.response;
                }
            )
            .catch();
    }
}
</script>

<style lang="scss" scoped>
    main {
        background-color: #1E2E3B;
        padding: 50px;
    }

    main > section > div > div {
        margin: 20px 0;
    }
</style>