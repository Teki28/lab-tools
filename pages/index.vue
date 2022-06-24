<template>
  <div>
    <h1>Home page</h1>
    <ul>
      <li>
        <nuxt-link :to="{name:'index'}">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'tool1'}">Tool1</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'tool2' }">Tool2</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name:'tool3' }">Tool3</nuxt-link>
      </li>

    </ul>
  </div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>

<style>
</style>
