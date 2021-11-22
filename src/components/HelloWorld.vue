<template>
  <h1>HelloWorld</h1>
  <ul id="tableau">
    <li v-show="toggle" v-for="item in items" :key="item.name">
      {{ item.name }}
    </li>
  </ul>
  <button @click="toggle = false">Masquer</button>
  <button @click="toggle = true">Afficher</button>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data: function () {
    return {
      toggle: true,
      items: [
        { name: "Melvyn REBECA" },
        { name: "Thibault SOWA" },
        { name: "Leo ALVES" },
        { name: "Timothée TEMIL" },
        { name: "Laetita RINALDI" },
        { name: "Fatma MARZOUKI" },
      ],
    };
  },
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
  margin-top: 1%;
}
a {
  color: #42b983;
}
</style>
