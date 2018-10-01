<template>
    <div class="about">
        <button @click="log">GET REQUEST</button>
        <Lottie :options="defaultOptions" :height="400" :width="400" @animCreated="handleAnimation"></Lottie>
    </div>
</template>


<script lang="ts">
import animationData from "../assets/animation/splashy_loader.json";
import Lottie from "../../node_modules/vue-lottie/src/lottie.vue";
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {
    Lottie
  }
})
export default class About extends Vue {
    defaultOptions = { animationData };
    anim: any;

    handleAnimation(anim: any) {
        this.anim = anim;
    }

    log(){
        // DO GET REQUEST
        const axios = require('axios');

        axios.get('http://localhost:50993/api/journey')
  .then(functio (response) {
    // handle success
    console.log(response);
  })
  .catch(functio (error) {
    // handle error
    console.log(error);
  })
  .then(functio () {
    // always executed
  });

    }
}
</script>
