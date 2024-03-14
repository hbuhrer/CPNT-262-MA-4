<template>
  <div id="app">
    <ComponentDos />
    <ComponentUno />
  </div>
</template>

<script>
import ComponentUno from './components/ComponentUno.vue';
import ComponentDos from './components/ComponentDos.vue';

export default {
  name: 'App',
  components: {
    ComponentUno,
    ComponentDos
  },
};
</script>