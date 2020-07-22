<template>
  <div class="wrapper">
    <p>{{ fullName }}</p>
    <p>
      Edit full name:<br />
      <input v-model="fullName">
    </p>
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
