<template>
  <ol>
    <li>{{ msg }}</li>
  </ol>
      
</template>

<script>
export default {
  name: 'defaultDescription',
  props: {
    msg: String
  },
  data() {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
