<template>
    <div class="container">
        <div>
            <Loader />
            <ProgressSpinner :style="{ width, height }" stroke-width="8" />
        </div>
    </div>
</template>

<script>
import Loader from "../components/Loader.vue"

export default {
    data() {
        return {
        text: null
        }
    },
    methods: {
        greet() {
            this.$toast.add({severity: 'info', summary: 'Hello '  + this.text});
        }
    }
}
</script>

<style>
.container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

@keyframes p-progress-spinner-color {
    100%,
    0% {
      stroke: blue;
    }
    40% {
      stroke: blue;
    }
    66% {
      stroke: blue;
    }
    80%,
    90% {
      stroke: blue;
    }
  }
</style>
