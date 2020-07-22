<template>
  <div class="wrapper">
    <p>
      First name:<br />
      <input v-model="firstName">
    </p>
    <p>
      Last name:<br />
      <input v-model="lastName">
    </p>
  </div>
</template>

<script>
export default {
  name: 'FullNameEditor',
  data () {
    const [firstName, lastName] = this.fullName.split(' ')
    return {
      firstName,
      lastName
    }
  },
  props: {
    fullName: {
      type: String,
      required: false,
      default: 'John Doe'
    }
  }
}
</script>

<style scoped>
  .wrapper {
    border: 5px solid red;
    padding: 1em;
  }
</style>
