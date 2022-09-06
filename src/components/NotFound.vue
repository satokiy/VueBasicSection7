<template>
  <div>
    404 not found page.
    <button @click="goToHome">return Home</button>
  </div>
</template>

<script>
export default {
  methods: {
    goToHome() {
      this.$router.push('/')
    }
  }

}
</script>

<style>

</style>