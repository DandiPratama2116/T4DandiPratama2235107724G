<template>
  <div>
    <child-component @message-to-parent1="displayMessage1" @message-to-parent2="displayMessage2"></child-component>
    <p>Message 1 from Child: {{ message1 }}</p>
    <p>Message 2 from Child: {{ message2 }}</p>
    <sibling-component :siblingMessage2="message2"></sibling-component>
    <slot></slot>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
import SiblingComponent from './SiblingComponent.vue';

export default {
  components: {
    ChildComponent,
    SiblingComponent
  },
  data() {
    return {
      message1: '',
      message2: ''
    }
  },
  methods: {
    displayMessage1(msg) {
      this.message1 = msg;
    },
    displayMessage2(msg) {
      this.message2 = msg;
    }
  }
}
</script>
