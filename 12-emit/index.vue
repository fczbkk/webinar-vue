<template>
  <div class="wrapper">
    <p>{{ fullName }}</p>
    <p>
      Edit full name:<br />
      <input v-model="fullName">
    </p>
    <FullNameEditor
      v-bind:fullName="fullName"
      v-on:fullNameUpdated="updateFullName"
    />
  </div>
</template>

<script>
import FullNameEditor from './FullNameEditor.vue'

export default {
  components: { FullNameEditor },
  data () {
    return {
      fullName: 'Riki Fridrich'
    }
  },
  methods: {
    updateFullName (newValue) {
      this.fullName = newValue
    }
  }
}
</script>

<style scoped>
</style>
