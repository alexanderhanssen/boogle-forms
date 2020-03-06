<template>
  <div class="home">
    <input v-model="formTitle" placeholder="Form title" />
    <br />

    <TextQuestionEditor
      v-for="textQuestion in textQuestions"
      :key="textQuestion.id"
    ></TextQuestionEditor>

    <button v-on:click="addTextQuestion">New question</button>

    <br />
    <button v-on:click="saveForm"></button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import TextQuestionEditor from "../components/TextQuestionEditor.vue";

@Component({
  components: {
    TextQuestionEditor
  }
})
export default class QuestionCreator extends Vue {
  private textQuestions: TextQuestionEditor[] = [];
  @Prop() formTitle!: string;

  public addTextQuestion() {
    this.textQuestions.push(new TextQuestionEditor());
  }

  public saveForm() {
    console.log(this.textQuestions);
  }
}
</script>
