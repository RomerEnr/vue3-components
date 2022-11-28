<script>
import BaseHeader from "@/components/BaseHeader.vue"
import BaseFooter from "@/components/BaseFooter.vue"
import bus from "@/event-bus"

export default {
  name: "App",
  mounted() {
    bus.$on("send-social", this.onSocial)
    console.log(bus);
  },
  components: {
    BaseHeader,
    BaseFooter
  },
  methods: {
    onSocial(data) {
      console.log("He recibido: ", data);
    }
  }
}
</script>

<template>
  <div>
    <BaseHeader text="Docker" />
    <BaseFooter />
  </div>
</template>

<style>

</style>