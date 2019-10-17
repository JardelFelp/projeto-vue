<template>
  <div class="hello">
    <h1>Carrinho</h1>
    <button v-on:click="removerItemCarrinho()">Remover Item</button>
    {{ qtdItens }}
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  props: {
    qtdItens: {
      type: Number,
      default: 0
    },
  },

  mounted() {
    console.log(this.removerItemCarrinho);
  },

  methods: {
    removerItemCarrinho() {
      this.$parent.removerItemCarrinho();
    }
  }

  // Similar ao state do react
  // data() {} ou data: function() {}
  // data: function() {
  //   return {
  //     numeroUm: '',
  //     numeroDois: ''
  //   }
  // },

  // computed: {
  //   soma() {
  //     return Number(this.numeroUm) + Number(this.numeroDois);
  //   }
  // }

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
