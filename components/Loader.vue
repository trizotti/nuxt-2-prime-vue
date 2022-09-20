<template>
    <ProgressSpinner :style="{ width, height }" stroke-width="8" />
  </template>
  
  <script>
  export default {
    name: "Loader",
    props: {
      size: {
        type: String,
        default: "sm",
        validator(value) {
          return ["sm", "md", "lg"].includes(value);
        },
      },
    },
    data() {
      return {
        width: "20px",
        height: "20px",
      };
    },
    beforeMount() {
      switch (this.size) {
        case "md":
          this.width = "30px";
          this.height = "30px";
          break;
        case "lg":
          this.width = "40px";
          this.height = "40px";
          break;
        default:
          this.width = "20px";
          this.height = "20px";
          break;
      }
    },
  };
  </script>
  