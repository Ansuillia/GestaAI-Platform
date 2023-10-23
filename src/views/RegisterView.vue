<template>
  <div
    class="mx-auto flex flex-col rounded-lg px-10 py-5 shadow-xl shadow-slate-950 xs:h-fit xs:w-full lg:w-3/6 lg:self-center"
  >
    <div class="mb-10 flex w-full items-center">
      <h1 class="text-3xl font-bold">Cadastre-se</h1>
    </div>
    <GA-Input
      name="name"
      type="text"
      v-model="newUser.name"
      label="Nome"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
      placeholder="Digite seu nome"
    ></GA-Input>
    <GA-Input
      name="lastname"
      type="text"
      v-model="newUser.lastname"
      label="Sobrenome"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
      placeholder="Digite seu sobrenome"
    ></GA-Input>
    <GA-Input
      name="email"
      type="email"
      v-model="newUser.email"
      label="E-mail"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
      placeholder="Digite seu e-mail"
    ></GA-Input>
    <GA-Input
      name="birthdate"
      type="date"
      v-model="newUser.birthdate"
      label="Data de Nacimento"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
    ></GA-Input>
    <GA-Input
      name="password"
      type="password"
      v-model="newUser.password"
      label="Senha"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
      placeholder="Digite sua senha"
    ></GA-Input>
    <GA-Input
      name="passwordConfirm"
      type="password"
      v-model="newUser.passwordConfirm"
      label="Confirme sua senha"
      inputClasses="w-full"
      divClasses="justify-center"
      labelClasses="text-lg"
      placeholder="Repita sua senha"
    ></GA-Input>

    <button @click="register" class="my-3 w-full rounded bg-slate-500 p-2 text-lg">
      Registrar
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import GAInput from '@/components/InputComponent.vue'

const newUser = ref({
  name: '',
  lastname: '',
  email: '',
  birthdate: '',
  password: '',
  passwordConfirm: ''
})

function register() {
  console.log(newUser.value)
}
</script>
