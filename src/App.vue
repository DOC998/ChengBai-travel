<script setup>
</script>

<template>
  <div class="div">
    <router-view/>
    <tab-bar></tab-bar>
  </div>
</template>

<script setup>

  import TabBar from '@/components/tab-bar/TabBar.vue'
  import { ref } from 'vue'

  const rateValue  = ref(0);

function rateIncrement() {
  rateValue.value++;
}




</script>
<style scoped>

</style>
