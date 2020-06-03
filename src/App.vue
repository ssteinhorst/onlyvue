<template>
  <div>
    <my-header></my-header>
    <my-search v-bind:providers="providers"></my-search>
    <my-provider v-bind:providers="providers"></my-provider>
    <my-create v-bind:providers="providers"></my-create>
  </div>
</template>

<script>

import header from './components/header';
import provider from './components/provider';
import search from './components/search';
import create from './components/create';
import providers from './assets/data.json';

export default {
  name: 'App',
  components: {
    'my-header': header,
    'my-search': search,
    'my-provider': provider,
    'my-create': create
  },
  data: function() {
    return {
      providers: providers.providers,
      baseUrl: process.env.VUE_APP_BASE_URL,
    };
  },
  methods: {
    created(){
      // Fetch Data
      // this.fetchData();
      console.log("in created");
    }
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
