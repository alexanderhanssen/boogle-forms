<template>
  <div>Hello {{ name }}</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class TestCompoent extends Vue {
  @Prop() private name!: string;
}
</script>