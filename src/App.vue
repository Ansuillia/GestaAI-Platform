<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav class="flex sticky top-0 z-10 w-full lg:container lg:mx-auto bg-slate-900 h-16 text-slate-200 items-center p-10 shadow-md shadow-slate-700">
    <div id="header-logo" class="flex mr-5 shrink">
      <h1 class="text-3xl">Gest.AI</h1>
    </div>
    <div id="header-links" class="flex flex-1 justify-center gap-x-6 grow">
      <RouterLink class="" to="/">Home</RouterLink>
      <RouterLink class="" to="/blog">Blog</RouterLink>
      <RouterLink class="" to="/about">Quem Somos</RouterLink>
    </div>
    <div id="header-login" class="flex shrink gap-x-2 justify-end">
      <RouterLink to="/login">Entrar</RouterLink>
      <RouterLink to="/register">Cadastrar</RouterLink>
    </div>
  </nav>

  <main class="flex lg:container lg:mx-auto bg-slate-800  min-h-screen p-10 text-slate-200">
    <RouterView />
  </main>

  <footer class="w-full flex lg:container lg:mx-auto bg-slate-900 h-16 text-slate-200 items-center p-10">
    <div class="flex flex-1 justify-center">
      <span class="text-center xs:text-xs">Powered by: Anderson Martins | &copy; 2023</span>
    </div>
  </footer>
</template>

<style scoped></style>
