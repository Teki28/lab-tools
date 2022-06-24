<template>
  <div>
    <h1 v-if="error.statusCode==404">404 404 404 404 404</h1>
    <h1 v-else>500 500 500 500 500</h1>
  </div>
</template>

<script>
export default {
  props: ['error']
}
</script>

<style>
</style>