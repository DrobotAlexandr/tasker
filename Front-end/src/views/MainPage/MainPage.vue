<template>
  <div class="MainPage">

    <RegistrationForm/>

  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';
import RegistrationForm from "@/components/Passport/RegistrationForm/RegistrationForm.vue";

export default defineComponent({
  name: 'MainPage',
  components: {RegistrationForm}
});
</script>
