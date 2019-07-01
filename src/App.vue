<template>
  <div id="app">
    <Menu :edit="canEdit"/>
    <button type="button" @click="edit">Show Buttons</button>
  </div>
</template>

<script>
import Menu from "./components/Menu";

export default {
  name: "App",
  components: {
    Menu
  },
  data() {
    return {
      canEdit: false
    };
  },
  methods: {
    edit() {
      this.canEdit = !this.canEdit;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
