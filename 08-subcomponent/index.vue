<template>
  <div class="wrapper">
    <p>{{ fullName }}</p>
    <p>
      Edit full name:<br />
      <input v-model="fullName">
    </p>
    <FullNameEditor />
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
  }
}
</script>

<style scoped>
</style>
