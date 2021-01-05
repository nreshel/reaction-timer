<template>
  <p>Reaction Time: {{score}} ms</p>
  <p>{{response}}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      response: null
    }
  },
  mounted() {
    if(this.score < 250) {
      this.response = "Ninja Reflexes"
    } else if(this.score < 400) {
      this.response = "Rapid Reflexes"
    } else {
      this.response = "Snail Reflexes"
    }
  }
}
</script>

<style scoped>

</style>