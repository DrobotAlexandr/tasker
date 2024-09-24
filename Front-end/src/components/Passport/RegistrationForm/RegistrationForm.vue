<template>
  <div class="RegistrationForm">
    <UiFormWrapper @send-form="submitForm">
      <UiFormTitle>Регистрация</UiFormTitle>

      <UiFormItem title="Имя">
        <input v-model="name" type="text" class="form-control">
      </UiFormItem>
      <UiFormItem title="E-mail">
        <input v-model="email" type="email" class="form-control">
      </UiFormItem>
      <UiFormItem title="Пароль">
        <input v-model="password" type="password" class="form-control">
      </UiFormItem>
      <UiFormItem title="Повторите ввод пароля">
        <input v-model="confirmPassword" type="password" class="form-control">
      </UiFormItem>

      <UiFormItem>
        <UiFormButton type="submit">Регистрация</UiFormButton>
      </UiFormItem>
    </UiFormWrapper>
  </div>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';

import './RegistrationForm.css';
import UiFormTitle from "@/components/Ui/Form/UiFormTitle/UiFormTitle.vue";
import UiFormItem from "@/components/Ui/Form/UiFormItem/UiFormItem.vue";
import UiFormButton from "@/components/Ui/Form/UiFormButton/UiFormButton.vue";
import UiFormWrapper from "@/components/Ui/Form/UiFormWrapper/UiFormWrapper.vue";

export default defineComponent({
  components: {UiFormWrapper, UiFormButton, UiFormItem, UiFormTitle},
  setup() {
    const name = ref('');
    const email = ref('');
    const password = ref('');
    const confirmPassword = ref('');

    const submitForm = () => {
      alert(name.value);
    };

    return {
      submitForm,
      name,
      email,
      password,
      confirmPassword
    };
  }
});
</script>
