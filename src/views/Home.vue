<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Boogle forms" />
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({ components: { HelloWorld } })
export default class Home extends Vue {}
</script>
