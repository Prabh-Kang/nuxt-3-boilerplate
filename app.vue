<script setup>
const {data, pending} = useFetch('/api/hello');
</script>

<template>
  <MyEditor />
</template>
