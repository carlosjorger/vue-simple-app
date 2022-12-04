
<template>
  <div class="toToList">
    <input v-model="tempToDoName"/>
    <input v-model="tempToDoDescription"/>

    <button v-on:click="addToDo">Add toDo</button>
    <div class="toDo-cardList">
      <vue-to-do
        v-for="toDo in toDos"
        :key="toDo.id"
        v-bind:toDo="toDo">
      </vue-to-do>
    </div>
  </div>
</template>

<script>
import VueToDo from './VueToDo.vue'
export default {
  name: 'VueToDoList',
  data () {
    return {
      count: 0,
      tempToDoName: 'cosa por hacer',
      tempToDoDescription: 'una cosa que no he hecho todavia',
      toDos: []
    }
  },
  components: {VueToDo},
  methods: {
    addToDo: function () {
      this.count++
      this.toDos.push({
        'id': this.count,
        'name': this.tempToDoName,
        'description': this.tempToDoDescription
      })
    }
  }
}
</script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .toDo-cardList{
    display: grid;
    grid-template-columns: auto auto auto auto;
    grid-gap: 1vw;
  }

</style>
