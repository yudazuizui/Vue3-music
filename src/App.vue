<template>
<router-view/> 
  <FooterMusic v-show="$store.state.isFooterMusic"/> -->
<Child/>
</template>
<script  >
import Child from "@/views/Child.vue";
components:{
  Child
}

</script >

<style lang="less">

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.icon{
  width: .5rem;
  height: .5rem;
}
a{
  color: black;
}
</style>
