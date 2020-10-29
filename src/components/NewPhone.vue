<template>
  <div class="row">
    <div class="col-md-3 mx-auto shadow-lg p-3 mb-5 bg-white rounded">
      <div align="center">
        <img src="../assets/default.jpg" class="rounded mx-auto d-block" height="150">
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
</template>

<script>
export default {
}
</script>

<style scoped>

</style>
