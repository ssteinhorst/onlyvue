<template>
  <div>
    <my-header></my-header>
    <my-search></my-search>
    <my-provider></my-provider>
  </div>
</template>

<script>

import header from './components/header';
import provider from './components/provider';
import search from './components/search';

export default {
  name: 'App',
  components: {
    'my-header': header,
    'my-search': search,
    'my-provider': provider
  },
  data: function() {
    return {
        
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 60px;
}
</style>
