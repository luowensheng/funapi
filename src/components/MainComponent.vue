<template>
  <section class="main-container flex-center fill-height">
    <main class="flex-column invisible-scrollbar">
      
      <section class="component flex-column hero">
        <span>Rapidly generate <span class="fun">fun</span> APIs<br/>for your next <span class="fun">fun</span> projects.</span>
        <p>An approchable, performant and versatile framework for building web user interfaces</p>
        <div class="main-button-container flex-row flex-center">
          <ImageButtonComponent 
                v-bind:key="index" 
                v-for="(button, index) in buttons"  
                :text-content="button.textContent" 
                :src="button.src" 
                :dark="index==0"
                />
        </div>
      </section>

      <section class="component">
        <APIViewerComponent :api="mainApi"/>
      </section>

      <section class="component" v-bind:key="index" v-for="(api, index) in apis">
          <APIViewerComponent :api="api"/>  
      </section>
    </main>
  </section>

</template>
<script>
import ImageButtonComponent from "./ImageButtonComponent.vue"
import APIViewerComponent from "./APIViewerComponent.vue"
export default {
  name: 'MainComponent',
  data(){
    return {
      buttons: [
        {textContent: "Get Started", src: ""},
        {textContent: "Language", src: ""},
        {textContent: "Vision", src: ""}
      ],
      mainApi: {
        url: "/api/v1/generate/people",
            method:"GET",
            outputType: "text",
            params: {
              type: "url",
            }      },
      apis: [
        {
            url: "/api/v1/generate/people",
            method:"POST",
            outputType: "text",
            params: {
              type: "url",
            }
        },
        {
            url: "/api/v1/generate/people",
            method:"GET",
            outputType: "text",
            params: {
              type: "url",
            }
        },
        {
            url: "/api/v1/generate/people",
            method:"GET",
            outputType: "text",
            params: {
              type: "url",
            }
        },        {
            url: "/api/v1/generate/people",
            method:"GET",
            outputType: "text",
            params: {
              type: "url",
            }
        }
      ]
    }
  },
  components: {
    ImageButtonComponent,
    APIViewerComponent
  }
}
</script>

<style scoped>

.fun {
  content: "fun";
  display: inline-block;
  font-style: italic;
  transform: rotate(-15deg);
  translate: 6px -6px;
}
.component {
  --parent-height: calc(100vh - var(--header-height));
  --first-component-height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.component:nth-of-type(1) {
  min-height: var(--first-component-height);
}
.component:nth-of-type(1)>span {
  font-size: 2.5rem;
  font-weight: 700;
}
.component:nth-of-type(1)>p {
  font-size: 1.2rem;
}
.component {
  /* background-color: brown; */
  min-height: calc((var(--parent-height) - var(--first-component-height) - 30px));
  /* border: 1px solid red; */
}

.hero {
}
/* section section {
  border: 1px solid red;
} */
.main-container {
  flex-grow: 1;
}

.main-button-container {
  gap: 15px;
}

main {
  /* background-color: rgb(241, 250, 255); */
  height: 100%;
  width: 90%;
  overflow-y: auto;

}
</style>