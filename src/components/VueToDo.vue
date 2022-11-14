<template>
    <div>
      <li>{{toDo.name}}</li>
    </div>
</template>
<script>
export default {
  name: 'VueToDo',
  props: ['toDo']
}
</script>
<style scoped>
  li{
    color: red;
  }
</style>
