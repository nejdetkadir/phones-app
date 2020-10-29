<template>
  <div class="row">
    <div class="col-md-12">
      <div class="progress mt-4">
        <div class="progress-bar bg-warning" role="progressbar" :style="{ width: progress+'%' }" aria-valuenow="0" aria-valuemin="10" aria-valuemax="100">
          {{ currentPhone }}/10
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {eventBus} from "@/main";

export default {
  data: function() {
    return{
      currentPhone: null,
      progress: null
    }
  },
  created() {
    eventBus.$on('updateProgress', (data) => {
      this.currentPhone = data;
      this.progress = data * 10;
    });
  }
}
</script>

<style scoped>

</style>
