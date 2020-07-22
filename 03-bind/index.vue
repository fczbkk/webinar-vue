<template>
  <div class="wrapper">
    Full name:
    <input v-bind:value="fullName">
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
