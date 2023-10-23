<template>
  <div
    class="mx-auto flex flex-col rounded-lg px-10 py-5 shadow-xl shadow-slate-950 xs:h-fit xs:w-full lg:w-3/6 lg:self-center"
  >
    <div class="mb-10 flex w-full items-center">
      <h1 class="text-3xl font-bold">Faça seu login</h1>
    </div>
    <GA-Input
      name="username"
      type="text"
      v-model="user.username"
      label="Usuario"
      inputClasses="w-full"
      labelClasses="text-lg"
      placeholder="Digite seu usuário"
    ></GA-Input>

    <GA-Input
      name="password"
      type="password"
      v-model="user.password"
      label="Senha"
      inputClasses="w-full"
      labelClasses="text-lg"
      placeholder="Digite sua senha"
    ></GA-Input>

    <button
      class="my-3 w-full rounded border border-slate-500 p-2 text-lg hover:bg-slate-700"
      @click="login"
    >
      Entrar
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import GAInput from '@/components/InputComponent.vue'

const user = ref({ username: '', password: '' })

function login() {
  console.log(user.value)
}
</script>
