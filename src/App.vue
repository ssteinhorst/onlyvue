<template>
  <div>
    <my-header></my-header>
    <div class="headerBox border container-fluid m-0 p-0">
      <div class="navBar row m-1">
        <div class="m-1" id="nav">
          <p class="navLinks m-1">
            <button v-on:click="toggleSearch">Search</button>
            |
            <button v-on:click="toggleEdit">Create</button>
            |
            <button v-on:click="toggleFacilities">Facilites</button>
          </p>
        </div>
      </div>
    </div>
    <my-search v-if="searchEnabled" v-bind:providers="providers"></my-search>
    <my-provider v-if="searchEnabled" v-bind:providers="providers"></my-provider>
    <my-create v-if="createEnabled" v-bind:providers="providers"></my-create>
  <my-facilities v-if="facilitiesEnabled" v-bind:facilities="facilities"></my-facilities>
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
      facilities: data.facilities,
      createEnabled: false,
      searchEnabled: true,
      facilitiesEnabled: false
    };
  },
  methods: {
    created(){
      // Fetch Data
      // this.fetchData();
      console.log("in created");
    },
    toggleEdit() {
      this.createEnabled = this.createEnabled? false:true;
      // if(this.createEnabled) {
      //   this.createEnabled = false
      // } else {
      //   this.createEnabled = true;
      // }
    },
    toggleSearch() {
      this.searchEnabled = this.searchEnabled? false:true;
    },
    toggleFacilities() {
      this.facilitiesEnabled = this.facilitiesEnabled? false:true;

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
