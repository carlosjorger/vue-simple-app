
<template>
  <div class="toToList">
    <input v-model="tempToDo"/>
    <button v-on:click="addToDo">Add toDo</button>
    <ul>
      <vue-to-do v-for="toDo in toDos" :key="toDo.id" v-bind:toDo="toDo">
      </vue-to-do>
    </ul>
  </div>
</template>

<script>
import VueToDo from './VueToDo.vue'
export default {
  name: 'VueToDoList',
  data () {
    return {
      count: 0,
      tempToDo: 'cosa por hacer',
      toDos: []
    }
  },
  components: {VueToDo},
  methods: {
    addToDo: function () {
      this.count++
      this.toDos.push({
        'id': this.count,
        'name': this.tempToDo
      })
    }
  }
}
</script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  ul{
    max-width: 40vw;
    font-size: 1.5vw;

  }

</style>
