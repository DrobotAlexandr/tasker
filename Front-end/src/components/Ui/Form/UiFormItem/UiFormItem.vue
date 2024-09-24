<template>
  <div class="UiFormItem">
    <div v-if="title" class="UiFormItem__title" v-html="title"></div>
    <div class="UiFormItem__input">
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';

import './UiFormItem.css';

export default defineComponent({
  name: 'UiFormItem',
  props: ['title']
});
</script>
