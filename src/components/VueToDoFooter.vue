<template>
  <div class="footer">
    <h3>{{ date }}</h3>
  </div>
</template>

<script>
export default {
  name: 'vuetodo-footer',
  data () {
    return {
      date: new Date().toLocaleString()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer{
  font-size: 2vw;

}
</style>
