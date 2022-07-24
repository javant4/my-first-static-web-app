<template>
  <div>{{ message }}</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "",
    };
  },
  async mounted() {
    const { text } = await await fetch("/api/message");
    this.message = text;
  },
};
</script>
