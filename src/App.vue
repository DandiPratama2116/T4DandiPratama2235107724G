<template>
  <div id="app">
    <parent-component>
      <template #default>
        <p>This is content from the parent component slot.</p>
      </template>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3ff04b;
  margin-top: 60px;
}
</style>
