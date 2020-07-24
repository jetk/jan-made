<template>
  <div>
      
  <div class="container"><VueShowdown :markdown="fileContent"></VueShowdown></div>
  </div>
</template>

<script>
import VueShowdown from "vue-showdown";

export default {
  components: VueShowdown,
  data: function() {
    return {
      fileContent: null,
      fileToRender: "./items/kazoot.md",
      rawContent: null
    };
  },
  created: function() {
    //  const fileToRender = `./assets/documentation/general/welcome.md`;
    //  const rawContent = ""; // Read the file content using fileToRender
    // this.fileContent = "### marked(rawContent) should get executed";
    this.getContent();
  },
  methods: {
    getContent() {
      this.fileContent = "rendering ";
      this.$http.get(this.fileToRender).then(
        response => {
          this.fileContent = response.body;
        },
        response => {
          // error callback
          this.fileContent = "An error ocurred";
        }
      );
    }
  }
};
</script>

<style>


</style>
