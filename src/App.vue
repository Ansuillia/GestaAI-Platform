<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header >
    <nav class="w-full flex bg-slate-900 h-16 text-slate-200 items-center p-10 sticky shadow-md shadow-slate-700">
      <div id="header-logo" class="flex mr-5 shrink">
        <h1 class="text-3xl">Gest.AI</h1>
      </div>
      <div id="header-links" class="flex flex-1 justify-center gap-x-6 grow">
        <RouterLink class="hover:text-xl transition ease-in-out hover:scale-110" to="/">Home</RouterLink>
        <RouterLink class="hover:text-xl transition ease-in-out hover:scale-110" to="/blog">Blog</RouterLink>
        <RouterLink class="hover:text-xl transition ease-in-out hover:scale-110" to="/about">Quem Somos</RouterLink>
      </div>
      <div id="header-login" class="flex shrink gap-x-2 justify-end">
        <RouterLink to="/login">Entrar</RouterLink>
        <RouterLink to="/register">Cadastrar</RouterLink>
      </div>
    </nav>
  </header>
  <main class="flex w-full h-screen bg-slate-800 p-10 text-slate-200">
    <RouterView />
  </main>
  <footer class="w-full flex bg-slate-900 h-16 text-slate-200 items-center p-10">
    <div class="flex flex-1 justify-center">
      <span class="text-center">Powered by: Anderson Martins | &copy; 2023</span>
    </div>
  </footer>
</template>

<style scoped></style>
