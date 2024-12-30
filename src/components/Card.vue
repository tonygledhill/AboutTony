<script setup lang="ts">
import { defineProps, type PropType } from 'vue';

export interface ICard {
     /**
   * The id
   */
   id: number,
     /**
   * The text that will be shown in the label
   */
   title: string,

     /**
   * The description
   */
   description: string
}

const props = defineProps({
    card: {
            type: Object as PropType<ICard>,
            required: true
        }
});
</script>

<template>
    <div class="card">
        <img src="https://placehold.co/600x400" />
        <h1>{{ props.card.title }}</h1>
        <p>{{ props.card.description }}</p>
    </div>

</template>

<style lang="scss" scoped>

.card{
    width: 30%;
    display: flex;
    flex-direction: column;
}
</style>