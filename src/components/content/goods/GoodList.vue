<template>
  <div class="goods">
    <good-list-item v-for="(item,index) in goods" :goods="item" :key="index"></good-list-item>
  </div>
</template>

<script>
import GoodListItem from "./GoodListItem"
export default {
 name:"GoodList",
 components:{
   GoodListItem
 },
 props:{
    goods:{
      type:Array,
      default(){
        return []
      }
    }
  }
}
</script>

<style scoped>
.goods {
  display: flex;
  flex-wrap: wrap;
  padding-top: 10px;
}
</style>