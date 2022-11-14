<template>
    <div class="toDo-card">
      <header>
            <h2>{{toDo.name}}</h2>
      </header>
      <div class="content">
            <p>{{toDo.description}}</p>
        </div>
    </div>
</template>
<script>
export default {
  name: 'VueToDo',
  props: ['toDo']
}
</script>
<style scoped>
  .toDo-card {
    display: grid;
    grid-template-rows:max-content 15vh;
    border-style: solid;
    max-width: 40vw;
  }
  header>h2{
    margin: 0;
    padding: 8px;
  }
  .content>p{
    padding: 8px;
  }
</style>
