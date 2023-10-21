<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav
    class="sticky top-0 z-10 flex h-16 w-full items-center bg-slate-900 p-10 text-slate-200 shadow-md shadow-slate-700 lg:container lg:mx-auto"
  >
    <div id="header-logo" class="mr-5 flex shrink">
      <h1 class="text-3xl">Gest.AI</h1>
    </div>
    <div id="header-links" class="flex flex-1 grow justify-center gap-x-6">
      <RouterLink class="" to="/">Home</RouterLink>
      <RouterLink class="" to="/blog">Blog</RouterLink>
      <RouterLink class="" to="/about">Quem Somos</RouterLink>
    </div>
    <div id="header-login" class="flex shrink justify-end gap-x-2">
      <RouterLink to="/login">Entrar</RouterLink>
      <RouterLink to="/register">Cadastrar</RouterLink>
    </div>
  </nav>

  <main class="flex min-h-screen bg-slate-800 p-10 text-slate-200 lg:container lg:mx-auto">
    <RouterView />
  </main>

  <footer
    class="flex h-16 w-full items-center bg-slate-900 p-10 text-slate-200 lg:container lg:mx-auto"
  >
    <div class="flex flex-1 justify-center">
      <span class="text-center xs:text-xs">Powered by: Anderson Martins | &copy; 2023</span>
    </div>
  </footer>
</template>

<style scoped></style>
