<template>
  <div>
    <NavBar />
    <ListNumber />

    <button @click="goBack">Go Back</button>
    <button @click="goForward">Go Forward</button>
  </div>
</template>
  
<script>
  import { useRouter } from 'vue-router'
  import NavBar from '@/components/NavBar.vue'
  import ListNumber from '@/components/ListNumber.vue'

  export default {
    name: 'HomeView',
    components: {
      NavBar,
      ListNumber,
    },
    setup() {
      const router = useRouter()

      const goBack = () => {
        if (router._value?.path !== '/') {
          console.log(router);

        }
      }

      const goForward = () => {
        router.forward()
      }

      return {
        goBack,
        goForward
      }
    }
  }
</script>
  
<style scoped>
</style>
  