<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :qtdItens="qtdItens" />

    <!-- v-on:click ou @click -->
    <button
      v-on:click="adicionarAoCarrinho()"
    >Adicionar item ao Carrinho</button>
  </div>
</template>

<script>
// @ is an alias to /src

// https://br.vuejs.org/v2/guide/events.html
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'home',

  components: {
    HelloWorld,
  },

  data() {
    return {
      itens: []
    }
  },

  computed: {
    qtdItens() {
      return this.itens.length;
    }
  },

  methods: {
    adicionarAoCarrinho() {
      this.itens.push({
        name: 'Mouse',
        valor: 500
      });
    },

    removerItemCarrinho() {
      this.itens.pop();
    }
  }
};
</script>
