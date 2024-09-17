<template>
  <div>
    <NavBar />
    <ListNumber />
  </div>
</template>
  
<script>
  import NavBar from '@/components/NavBar.vue'
  import ListNumber from '@/components/ListNumber.vue'

  export default {
    name: 'HomeView',
    components: {
      NavBar,
      ListNumber,
    }
  }
</script>
  
<style scoped>
</style>
  