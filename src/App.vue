<template lang="pug">
#app 
  component(:is="layout")
    router-view
</template>

<script>
import EmptyLayout from '@/layouts/EmptyLayout'
import MainLayout from '@/layouts/MainLayout'
export default {
  name: 'App',

  data: () => ({  }),
    components: {
      EmptyLayout,
      MainLayout  
      },
      mounted() {     },  methods: {      }, 
   computed:{ 
     layout(){
       return (this.$route.meta.layout || 'empty')+ '-layout'
     }
       }
};
</script>

<style lang="sass">
@import '~materialize-css/dist/css/materialize.min.css'
@import 'assets/index.css'
  
  

</style>