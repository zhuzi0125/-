<template>
  <div id="app">
   <router-view></router-view>
    <FooterGuide v-show="$route.meta.showFooter"></FooterGuide>
  </div>
</template>
<script>
  import {mapActions} from 'vuex'
  import FooterGuide from "./components/FooterGuide/FooterGuide.vue"
  export default{
    mounted () {
      // this.$store.dispatch('getAddress')
      console.log(this.getCategorys());

    },
    methods: {
      ...mapActions(['getCategorys'])
  },
    components:{
      FooterGuide
    }
  }
</script>
<style lang="stylus" rel="stylesheet/stylus">
 body
   margin:0px
 a
   text-decoration none
 li
   list-style none

</style>
