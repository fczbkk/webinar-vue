<template>
  <div class="wrapper">
    <p>{{ fullName }}</p>
    <p>
      Edit full name:<br />
      <input
        ref="fullNameInput"
        v-bind:value="fullName"
        v-on:input="updateFullName"
      >
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      fullName: 'Riki Fridrich'
    }
  },
  methods: {
    updateFullName () {
      this.fullName = this.$refs.fullNameInput.value
    }
  }
}
</script>

<style scoped>
</style>
