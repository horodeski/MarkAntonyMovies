<script>
export default {
  props: {
    poster: String,
    nome_fsa: String,
    link_filme: {
      type: Object,
    },
  },
  methods: {
    UrlDoFilme(id) {
      return `/filmaco/${id}`;
    },
  },
};
</script>
<template>
  <div id="section3-container" class="container">
    <img class="cardfilmes" :src="poster" />
    <div class="overlay">
      <div class="text">
        <h4 class="nome_filme">{{ nome_fsa }}</h4>
        <router-link :to="UrlDoFilme(link_filme.id)">
          <button class="verMais">VER MAIS</button>
        </router-link>
      </div>
    </div>
  </div>
</template>
