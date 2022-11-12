<template>
  <div>
    <li v-for="toDo in toDos" :key="toDo.name">
      <p>{{ toDo }}</p>
    </li>
  </div>
</template>

<script>
export default {
  name: 'VueToDoList',
  data () {
    return {
      toDos: [
        {
          name: 'Estudiar ingles'
        },
        {
          name: 'Leer libro pendiente'
        }
      ]
    }
  }
}
</script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}

h3 {
  text-align: left;
}
</style>
