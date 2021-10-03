<script lang="ts">
import { defineComponent } from "vue";
import Title from "@components/organisms/Title.vue";
import Card from "@components/organisms/Card.vue";
import teamBuilderIcon from '@assets/icon-team-builder.svg';
import supervisorIcon from '@assets/icon-supervisor.svg';
import karnaIcon from '@assets/icon-karma.svg';
import calculatorIcon from '@assets/icon-calculator.svg';


export default defineComponent({
  name: 'Main',
  components: { Card, Title },
  data() {
    return {
      cards: [
        {
          area: 't',
          color: '#EB5354',
          title: 'team builder',
          text: 'Scans our talent network to create the optimal team for your project',
          imgSrc: teamBuilderIcon,
        },
        {
          area: 'l',
          color: '#4BCFCF',
          title: 'Supervisor',
          text: 'Monitors activity to identify project roadblocks',
          imgSrc: supervisorIcon,
        },
        {
          area: 'r',
          color: '#579BE9',
          title: 'Calculator',
          text: 'Uses data from past projects to provide better delivery estimates',
          imgSrc: karnaIcon,
        },
        {
          area: 'b',
          color: '#FBAD4A',
          title: 'Karma',
          text: 'Regularly evaluates our talent to ensure quality',
          imgSrc: calculatorIcon,
        },

      ],
    }
  },
})
</script>

<template>
  <Title />
  <div class="px-[15vw] h-[65%] grid grid-cols-3 grid-rows-4 grid-schema gap-6">
    <Card
        v-for="card in cards"
        :key="card.title"
        :style="{ '--area': card.area }"
        :bar-color="card.color"
        :title="card.title"
        :text="card.text"
        :img-src="card.imgSrc"
    />
  </div>

</template>

<style scoped>

  .grid-schema {
    grid-template-areas:
    ". t ."
    "l t r"
    "l b r"
    ". b .";
  }
</style>