<template>
  <div class="wrapper">
    Full name:
    <input
      v-bind:value="fullName"
      v-on:click="fullName = 'John Doe'"
    >
  </div>
</template>

<script>
export default {
  data () {
    return {
      fullName: 'Riki Fridrich'
    }
  }
}
</script>

<style scoped>
</style>
