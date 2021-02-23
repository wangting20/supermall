<template>
  <div class="goods">
      <goods-list-item v-for="(item,key) in goods" :goods-item="item" :key="key" />
  </div>
</template>
 
<script>
import GoodsListItem from "./GoodsListItem"
export default {
    name:'GoodList',
    components:{
        GoodsListItem
    },
    props:{
        goods:{
            type:Array,
            default() {
                return []
            }
        }
    }
}
</script>

<style scoped>
    .goods {
        display:flex;
        flex-wrap: wrap;
        justify-content: space-around;

        padding: 2px;
    }



</style>