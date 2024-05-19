<template>
    <div>
      <p>Message 2 from Parent: {{ siblingMessage2 }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['siblingMessage2']
  }
  </script>
  