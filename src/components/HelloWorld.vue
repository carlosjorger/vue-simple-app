<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <vue-to-do-list></vue-to-do-list>
    <vue-to-do-footer></vue-to-do-footer>
  </div>
</template>

<script>
import VueToDoFooter from './VueToDoFooter.vue'
import VueToDoList from './VueToDoList.vue'

export default {
  name: 'HelloWorld',
  components: {
    VueToDoFooter,
    VueToDoList
  },
  data () {
    return {
      msg: 'Welcome to VueToDo app'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}
h3{
  text-align: left;
}
</style>
