
<template>

  <div>

    <MyHeader />
    <MyMain />
    <MyFooter />

  </div>

</template>

<script>

import MyHeader from "./components/MyHeader.vue";
import MyMain from "./components/MyMain.vue";
import MyFooter from "./components/MyFooter.vue";


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
}
}
</script>

<style lang="scss">
   
   @import './assets/style/vars';
   @import './assets/style/global';
   @import './assets/style/utils';

   @import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');



</style>
