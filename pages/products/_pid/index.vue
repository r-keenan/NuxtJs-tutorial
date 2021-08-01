<template>
  <h1>A single product, with ID: {{ $route.params.pid }}</h1>
</template>

<script>
export default {
  validate(data) {
    return /^\d+$/.test(data.params.pid);
  }
};
</script>
