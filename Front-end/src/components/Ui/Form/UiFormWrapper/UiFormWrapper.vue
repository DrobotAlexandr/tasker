<template>
  <form @submit.prevent="submitForm" class="UiFormWrapper">
    <slot></slot>
  </form>
</template>

<script lang="ts">
import { defineComponent, defineEmits } from 'vue';

import './UiFormWrapper.css';

export default defineComponent({
  setup(_, { emit }) {

    const submitForm = () => {
      emit('sendForm');
    };

    return {
      submitForm
    };
  }
});
</script>
