<template>
  <div class="container">
    <div class="row">
      <div class="col-md-3 mx-auto shadow-lg p-3 mb-5 bg-white rounded">
        <div align="center">
          <img src="./assets/default.jpg" class="rounded mx-auto d-block" height="150">
          <button class="btn btn-outline-dark mt-4 btn-sm"><i class="fas fa-upload"></i> Select an image</button>
        </div>
      </div>
      <div class="col-md-6 mx-auto align-self-center shadow-lg p-3 mb-5 bg-white rounded">
        <h3 class="text-center">Create Form</h3>
        <form>
          <div class="form-group input-group input-group-sm">
            <input type="text" name="phone-model" placeholder="Phone model" class="form-control">
          </div>
          <div class="row">
            <div class="col input-group input-group-sm">
              <input type="text" name="phone-price" class="form-control" placeholder="Phone price">
            </div>
            <div class="col input-group input-group-sm">
              <input type="number" name="phone-piece" class="form-control" placeholder="Phone piece">
            </div>
          </div>
          <button type="submit" class="btn btn-outline-success mt-3 btn-sm"><i class="fas fa-plus"></i> Create</button>
        </form>
      </div>
    </div>
    <hr>
    <div class="row">
      <div class="col-md-12">
        <h2 class="text-center">List of added phones</h2>
        <div class="progress mt-4">
          <div class="progress-bar bg-warning" role="progressbar" style="width: 10%;" aria-valuenow="0" aria-valuemin="10" aria-valuemax="100">10%</div>
        </div>
        <div class="mt-4">

        </div>
      </div>
    </div>
    <div align="center" class="row item-list">
      <div class="col-md-2 myofset mt-2 mb-1" v-for="index in 10" :key="index">
        <div class="card shadow p-3 mb-5 bg-white rounded" style="width: 13rem;">
          <img src="./assets/default.jpg" class="card-img-top" height="200">
          <div class="card-body">
            <h6 class="card-title">Model</h6>
          </div>
          <ul class="list-group list-group-flush smal_font">
            <li class="list-group-item">Price : 15 <i class="fas fa-lira-sign"></i></li>
            <li class="list-group-item">Piece : 10</li>
            <li class="list-group-item">Total amount : 150 <i class="fas fa-lira-sign"></i></li>
          </ul>
          <div class="card-body">
            <button class="card-link btn btn-warning btn-sm">Edit</button>
            <button class="card-link btn btn-danger btn-sm">Delete</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
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
