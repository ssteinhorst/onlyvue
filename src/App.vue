<template>
  <div>
    <my-header></my-header>
    <my-search v-bind:providers="providers"></my-search>
    <my-provider v-bind:providers="providers"></my-provider>
    <my-create v-bind:providers="providers"></my-create>
  <my-facilities v-bind:facilities="facilities"></my-facilities>
  </div>
</template>

<script>

import header from './components/header';
import provider from './components/provider';
import search from './components/search';
import create from './components/create';
import data from './assets/data.json';
import facilities from './components/facilities';

export default {
  name: 'App',
  components: {
    'my-header': header,
    'my-search': search,
    'my-provider': provider,
    'my-create': create,
    'my-facilities': facilities
  },
  data: function() {
    return {
      providers: data.providers,
      facilities: data.facilities
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
