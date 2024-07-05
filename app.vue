<script setup>
const {data, pending} = useFetch('/api/hello');
</script>

<template>
  <div>
    <h3 v-if="pending">Loading data...</h3>
    <h3 v-else>Data is fetched: {{ data }}</h3>
  </div>
</template>
