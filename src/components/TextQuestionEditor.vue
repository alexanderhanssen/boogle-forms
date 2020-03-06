<template>
  <div class="question-wrapper">
    <!-- <input :value="title" placeholder="Title" /> -->
    <!-- <textarea v-model="question" placeholder="Spørsmål"></textarea> -->
    <textarea :value="question" placeholder="Your question"></textarea>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({})
export default class TextQuestionEditor extends Vue {
  @Prop() title!: string;
  @Prop({ default: "" }) question!: string;
  @Prop() required!: boolean;
  @Prop() id!: string;
}
</script>
