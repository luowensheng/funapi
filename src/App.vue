<template>
  <link rel="preload" href="Mona-Sans.woff2" as="font" type="font/woff2" crossorigin>

  <Header id="header"></Header>
   <section id="container">
    <SideBar id="sidebar"></SideBar>
    <Main></Main>
   </section>

</template>

<script>
import SideBar from './components/SideBarComponent.vue'
import Main from './components/MainComponent.vue'
import Header from './components/HeaderComponent.vue'
import "./assets/global.css"

export default {
  name: 'App',
  components: {
    SideBar,
    Main,
    Header
  }
}
</script>

<style>

#sidebar {
  height: 100%;
  width: 250px;
}

#container {
  width: 100%;
  height: 100%;
  background-color: rgb(252, 252, 252);
  display: flex;
  flex-direction: row;
}
#header {
  height: var(--header-height);
}
html, body {
  padding: 0%;
  margin: 0%;
}
body {
  background-color: white;
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  width: 100%;
  /* border: 1px solid lightgray; */
  /* border-radius: 9px; */
  max-width: 1200px;
  height: 100%;
  padding-left: 20px;
  overflow-y: hidden;
  padding-right: 20px;
}
</style>
