<script>
import bus from "@/event-bus"

export default {
  name: "BaseFooter",
  data() {
    return {
      socials: {
        facebook: "https://facebook.com",
        twitter: "https://twitter.com",
        instagram: "https://instagram.com"
      }
    }
  },
  methods: {
    sendSocials() {
      bus.$emit("send-social", this.socials)
    }
  }
}
</script>

<template>
  <div>
    <h2>Footer</h2>
    <button @click="sendSocials">Enviar socials</button>
  </div>
</template>

<style>

</style>