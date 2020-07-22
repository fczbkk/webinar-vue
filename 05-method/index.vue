<template>
  <div class="wrapper">
    <p>{{ fullName }}</p>
    <p>
      Edit full name:<br />
      <input
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
    updateFullName (event) {
      // eslint-disable-next-line
      console.log('name changed', event.target.value)
    }
  }
}
</script>

<style scoped>
</style>
