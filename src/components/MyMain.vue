<template>
  
  <main>
    <div class="container">
      <h4>--> Content Goes Here </h4>
    </div>
    <ShopRow />
  </main>

</template>

<script>

import ShopRow from './ShopRow.vue'

export default {
  name : 'MyMain',

  components : {
    ShopRow
  }
}
</script>

<style lang="scss">

  main{
    color: white;
    padding-top: 10px;
    background-color: #1c1c1c;
    .container{
      padding: 50px 0;
    }
  }

</style>