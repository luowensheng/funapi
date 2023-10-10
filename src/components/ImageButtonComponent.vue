<template>
    <button @mouseover="isHovering = true" 
            @mouseout="isHovering = false"  
            :class="getClass()" 
            class="button default-button">

            {{textContent}}
    </button>
</template>
<script>
export default {
  name: 'ImageButtonComponent',
  props: [
    "textContent",
    "src",
    "dark"
  ],
  data() {
    return {isHovering: false}
  },
  methods: {
    getClass(){
        if (!this.isHovering){
            if (this.dark){
                 return 'dark'
            } else {
                return 'light'
        }
        } else {
            if (this.dark){
                return 'light'
            } else {
                return 'dark'
            }
        }


    }
  },
  components: {
  }
}
</script>

<style scoped>
.button {
    background-color: white;
}
.light {
    background-color: white;
    color: black;
}

.dark {
    background-color: black;
    color: white
}
</style>