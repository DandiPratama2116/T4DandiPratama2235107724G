<template>
  <div>
    <button @click="sendMessage1">Send Message 1 to Child</button>
    <button @click="sendMessage2">Send Message 2 to Child</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendMessage1() {
      this.$emit('message-to-child1', 'Message 1 from GrandChild');
    },
    sendMessage2() {
      this.$emit('message-to-child2', 'Message 2 from GrandChild');
    }
  }
}
</script>
