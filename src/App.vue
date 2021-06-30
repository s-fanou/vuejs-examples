<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <h1>{{ msg }}</h1>

    <drop-down-menu @command-change="dropDownHandler"></drop-down-menu>
  </div>
</template>

<script>
import DropDownMenu from "./components/DropDownMenu.vue";

export default {
  name: "app",
  components: { DropDownMenu },
  data() {
    return {
      msg: "Sot-drop down menu with event emit",
    };
  },
  methods: {
    dropDownHandler(selectedCommand) {
      switch (selectedCommand) {
        case "logout":
          //this.logOutHandler();
          alert("logout command chosen");
          break;
        case "other":
          alert("Other command chosen");
          break;
        default:
          alert("Error!");
      }
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
