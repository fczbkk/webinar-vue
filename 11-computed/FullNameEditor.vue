<template>
  <div class="wrapper">
    <p>{{ joinedName }}</p>
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
  },
  watch: {
    fullName () {
      const [firstName, lastName] = this.fullName.split(' ')
      this.firstName = firstName
      this.lastName = lastName
    }
  },
  computed: {
    joinedName () {
      return [this.firstName, this.lastName].filter(Boolean).join(' ')
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
