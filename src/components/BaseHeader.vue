<script>
export default {
  name: "BaseHeader",
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      title: "Titulo: " + this.text
    }
  }
}
</script>

<template>
  <div>
    <h2> {{ title }} </h2>
  </div>
</template>

<style>

</style>