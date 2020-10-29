<template>
  <div class="row">
    <div class="col-md-3 mx-auto shadow-lg p-3 mb-5 bg-white rounded">
      <div align="center">
        <img :src="phone.selectedImage == null ? '/src/assets/default.jpg' : phone.selectedImage" class="rounded mx-auto d-block" height="150">
        <input ref="file" type="file" style="display: none;" @change="onChange($event)">
        <button class="btn btn-outline-dark mt-4 btn-sm" type="button" @click="$refs.file.click()"><i class="fas fa-upload"></i> Select an image</button>
      </div>
    </div>
    <div class="col-md-6 mx-auto align-self-center shadow-lg p-3 mb-5 bg-white rounded">
      <h3 class="text-center">Create Form</h3>
      <form>
        <div class="form-group input-group input-group-sm">
          <input type="text" name="phone-model" v-model="phone.model" placeholder="Phone model" class="form-control">
        </div>
        <div class="row">
          <div class="col input-group input-group-sm">
            <input type="number" name="phone-price" class="form-control" v-model="phone.price" placeholder="Phone price">

          </div>
          <div class="col input-group input-group-sm">
            <input type="number" name="phone-piece" class="form-control" v-model="phone.piece" placeholder="Phone piece">
          </div>
        </div>
        <button @click="createPhone()" type="button" class="btn btn-outline-success mt-3 btn-sm"><i class="fas fa-plus"></i> Create</button>
      </form>
    </div>
  </div>
</template>

<script>
import {eventBus} from "@/main";

export default {
  data: function() {
    return{
      phone: {
        model: null,
        price: null,
        piece: null,
        totalPrice: null,
        selectedImage: null,
      }
    }
  },
  methods: {
    onChange(e) {
      const file = e.target.files[0];
      this.phone.selectedImage = URL.createObjectURL(file);
    },
    createPhone() {
      this.phone.totalPrice = this.phone.price * this.phone.piece;
      eventBus.$emit("pushPhone", this.phone);
      this.phone = {
        model: null,
        price: null,
        piece: null,
        totalPrice: null,
        selectedImage: null,
      }
    }
  }
}
</script>

<style scoped>

</style>
