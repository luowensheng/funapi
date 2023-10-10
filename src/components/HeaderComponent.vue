<template>
    <header>
      <img src="logo.svg" alt="logo">
      <div id="spacer"></div>
      <div class="right-item">
        <div>API</div>
        <div>About</div>
        <div>FAQ</div>
      </div>
    </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  components: {
  }
}
</script>

<style scoped>
.right-item {
  display: flex;
  flex-direction: row;
  gap: 20px;
  padding: 10px;
  color: black;
  font-size: large; 
}
.right-item > * {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}

#spacer {
  flex-grow: 1;
}

header {
  display: flex;
  box-shadow: 0 20px 0px 0px rgb(162, 159, 159) !important;
  padding-bottom: 10px !important;

}

img {
  height: 100%;
}
</style>