<template>
  <div class="container">
    <NewPhone></NewPhone>
    <hr>
    <Progress></Progress>
    <hr>
    <Products></Products>



  </div>
</template>

<script>
import NewPhone from "@/components/NewPhone";
import Progress from "@/components/Progress";
import Products from "@/components/Products";

export default {
  components: {
    NewPhone,
    Progress,
    Products
  },
}
</script>

<style>
  .container{
    margin-top: 80px;
  }
  .smal_font{
    font-size: 14px;
  }
  .myofset{
    margin-left: 2.1%;
  }
  .item-list{
    margin-bottom: 150px;
  }
</style>
