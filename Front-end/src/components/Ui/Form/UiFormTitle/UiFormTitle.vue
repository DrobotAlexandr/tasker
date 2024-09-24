<template>
  <div class="UiFormTitle">
    <div class="UiFormTitle__title">
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';

import './UiFormTitle.css';

export default defineComponent({
  name: 'UiFormTitle'
});
</script>
