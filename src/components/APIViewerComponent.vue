<template>
    <div class="wrapper flex-row overflow-hidden">
        <div class="flex-column api-container flex-align-center">

            <div class="header flex-row ">
                <span class="method flex-justify-center">{{ this.api.method }}</span>
                <div class="url spacer flex-center">{{ this.api.url }}</div>
                <button class="default-button">Send</button>
            </div>

            <div class="body fill-width overflow-hidden">
                
                <div class="styled-input invisible-scrollbar fill-width" contenteditable="true" spellcheck="false">
                    <!-- {
                        "type": "selfie",
                        "description": "28 year old indonesian woman",
                        "image_count": 2
                    } -->
                </div>

            </div>

            <div class="json-output fill-width invisible-scrollbar overflow-hidden">
                <!-- <div class="styled-input " contenteditable="true">
                    {
                        "success": true,
                        "error": "",
                        "data": [
                            "https://oaidalleapiprodscus.blob.core.windows.net/private/org-RCXEhqb0qYRghbH3wmSBQiKQ/user-XiIyexuZpvKazt7LrwMnQ3Tj/img-0YGOkHMWExYetf82O7xP19Cl.png?st=2023-10-09T00%3A40%3A47Z&se=2023-10-09T02%3A40%3A47Z&sp=r&sv=2021-08-06&sr=b&rscd=inline&rsct=image/png&skoid=6aaadede-4fb3-4698-a8f6-684d7786b067&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2023-10-08T17%3A09%3A39Z&ske=2023-10-09T17%3A09%3A39Z&sks=b&skv=2021-08-06&sig=WSJ40MNh2N0LG5NHLyFk7wPMdh9MwAEAiHr1aX0aBxY%3D",
                            "https://oaidalleapiprodscus.blob.core.windows.net/private/org-RCXEhqb0qYRghbH3wmSBQiKQ/user-XiIyexuZpvKazt7LrwMnQ3Tj/img-vS40UbCPQQVRr18TB2YdyM45.png?st=2023-10-09T00%3A40%3A48Z&se=2023-10-09T02%3A40%3A48Z&sp=r&sv=2021-08-06&sr=b&rscd=inline&rsct=image/png&skoid=6aaadede-4fb3-4698-a8f6-684d7786b067&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2023-10-08T17%3A09%3A39Z&ske=2023-10-09T17%3A09%3A39Z&sks=b&skv=2021-08-06&sig=3MQ/iPDtjz4MP1Z9h9wN2Cq7ah%2BuslU41ZyBFIrtfb8%3D"
                        ]
                    }
                </div> -->
            </div>

        </div>

        <div class="output-viewer">

        </div>
    </div>
</template>

<script>

export default {
  name: 'APIViewerComponent',
  props: [
    "api"
    //   "url", "method", "outputType", "params", "type",
  ],
  components: {
  }
}
</script>

<style scoped>



.wrapper {
    height: 100%;
    width: 100%;
  /* border: 1px solid red; */

}
.method {
    padding: 10px;
}
button {
    background-color: blue;
    color: white;
    border-radius: var(--default-border-radius);
    width: 100px;
    padding: none !important;
}
.output-viewer {
    background-color: blueviolet;
    flex-grow: 1;
}

.header {
    width: 100%;
    gap: 10px;
    height: wrap;
    /* background-color: aqua; */
}
.url {
    /* background-color: beige; */
}

.styled-input {
    /* min-width: 100% !important; */
    height: 100%;
    margin: 0%;
    padding: 0%;
}

.body {
    background-color: red;
    height: 60%;
    margin: 0;
    padding: 0%a;
}
.api-container {
    /* background-color: bisque; */
    width: 50%;
    height: 100%;
    text-align: left;
    /* border: 1px solid red; */
    overflow: none;
    padding: none;

}

.json-output {
    overflow: hidden;
    max-width: 100%;
    text-overflow: clip;
    /* display: none; */
}
pre {
    overflow: scroll;
}
</style>