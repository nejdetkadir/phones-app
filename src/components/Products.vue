<template>
  <div>
    <h3 class="text-center mt-2 mb-2">List of added phones</h3>
    <div align="center" class="row item-list">
      <Phone v-for="phone in phoneList" :key="phone.model">
        <img :src="phone.selectedImage" class="card-img-top" height="200">
        <div class="card-body">
          <h6 class="card-title">{{ phone.model }}</h6>
        </div>
        <ul class="list-group list-group-flush smal_font">
          <li class="list-group-item">Price : {{ phone.price }} <i class="fas fa-lira-sign"></i></li>
          <li class="list-group-item">Piece : {{ phone.piece }}</li>
          <li class="list-group-item">Total amount : {{ phone.totalPrice }} <i class="fas fa-lira-sign"></i></li>
        </ul>
        <div class="card-body">
          <button class="card-link btn btn-danger btn-sm">Delete</button>
        </div>
      </Phone>
    </div>
  </div>
</template>

<script>
import Phone from "@/components/Phone";
import {eventBus} from "@/main";

export default {
  components: {
    Phone
  },
  data: function() {
    return{
      phoneList: []
    }
  },
  created() {
    eventBus.$on('pushPhone', (data) => {
      this.phoneList.push(data);
    });
  }
}
</script>

<style scoped>

</style>
