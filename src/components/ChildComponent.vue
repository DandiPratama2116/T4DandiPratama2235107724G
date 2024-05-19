<template>
  <div>
    <grand-child-component @message-to-child1="handleMessageFromGrandChild1" @message-to-child2="handleMessageFromGrandChild2"></grand-child-component>
    <p>Message 1 from GrandChild: {{ grandChildMessage1 }}</p>
    <p>Message 2 from GrandChild: {{ grandChildMessage2 }}</p>
    <button @click="sendMessageToParent">Send Messages to Parent</button>
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  components: {
    GrandChildComponent
  },
  data() {
    return {
      grandChildMessage1: '',
      grandChildMessage2: ''
    }
  },
  methods: {
    handleMessageFromGrandChild1(message) {
      this.grandChildMessage1 = message;
    },
    handleMessageFromGrandChild2(message) {
      this.grandChildMessage2 = message;
    },
    sendMessageToParent() {
      this.$emit('message-to-parent1', this.grandChildMessage1);
      this.$emit('message-to-parent2', this.grandChildMessage2);
    }
  }
}
</script>
