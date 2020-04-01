<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>

    <div>
        <p v-for="d in data" v-bind:key="d.id">
          <span>{{d.key}}</span>
          {{d.text}}
        </p>
    </div>
    <!--
    <div v-if="check">
      <p> Check True</p>
    </div>
    <div v-else>
      <p> Check False</p>
    </div>
    -->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,

  },
  data(){
     return {
       check: true,
       data: {0:{text: "hola1"},1:{text: "hola2"},2:{text: "hola3"}}
     }
  }

}
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
