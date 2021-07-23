<template>
  <div id="app">
    <HeaderComponent />
    <div id="sidebar">
      <h2>Contacts</h2>
      <b-list-group>
        <b-list-group-item>Martina</b-list-group-item>
        <b-list-group-item>Lucia</b-list-group-item>
        <b-list-group-item>Lorenzo</b-list-group-item>
      </b-list-group>
    </div>
    <div id="container">
      <div id="header">
        <ChatComponent msg="Welcome to Your Vue.js App" />
      </div>
      <div id="footer" class="container">
        <CreateMessage />
      </div>
    </div>
  </div>
</template>

<script>
import ChatComponent from "./components/ChatComponent.vue";
import CreateMessage from "./components/CreateMessageComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
export default {
  name: "App",
  components: {
    ChatComponent,
    CreateMessage,
    HeaderComponent,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: rgb(201, 233, 200) !important;
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 100vh;
  width: 100%;
  box-sizing: border-box;
}
#sidebar{
  background-color: white!important;;
  width: 20%;
  min-height: 90vh;
  float: left;
  border: 1px solid black;
  box-sizing: border-box;
}
#container {
  width: 80%;
  float: right;
  min-height: 90vh;
  box-sizing: border-box;
}
#header {
  padding-bottom: 60px;
  height: 100%;
}
#footer {
  position: absolute;
  bottom: 0;
  height: 60px;
  width: 80%;
}
</style>
