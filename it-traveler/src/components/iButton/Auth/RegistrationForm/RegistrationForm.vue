<script setup>
  import Iinput from '../../Iinput/Iinput.vue';
  import iButton from '../../iButton/iButton.vue';
  import { reactive, toRaw } from 'vue';

  const emit = defineEmits(['submit']);

  const userData = reactive({
    name: '',
    email: '',
    password: ''
  })
</script>

<template>
    <form @submit.prevent="emit('submit', toRaw(userData))" class="max-w-[500px] v-full bg-white rounded-2xl p-10" >
        <Iinput class="mb-4" label="Повне ім'я" placeholder="" v-model="userData.name"/>
        <Iinput class="mb-4" label="Електронна пошта" type="email" placeholder="email@gmail.com" v-model="userData.email"/>
        <Iinput class="mb-4" label="Пароль" type="password" placeholder="" v-model="userData.password"/>
        <iButton type="submit" class="mt-10 w-full">Ствоити акаунт</iButton>
    </form>
</template>

