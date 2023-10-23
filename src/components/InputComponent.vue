<template>
  <div :class="`mb-6 flex flex-row items-center ${divClasses}`">
    <div class="w-full">
      <label :for="name" :class="`label-default flex flex-col ${labelClasses}`"
        >{{ label }}
        <input
          :class="`input-default ${inputClasses}`"
          :id="id"
          :name="name"
          :type="type"
          :placeholder="placeholder"
          :value="modelValue"
          @input="$emit('update:modelValue', ($event.target as HTMLInputElement).value)"
        />
      </label>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from 'vue'

interface IInput {
  id?: string
  type: string
  name: string
  label: string
  divClasses?: string
  labelClasses?: string
  inputClasses?: string
  modelValue: any
  placeholder?: string
}

defineProps<IInput>()

defineEmits(['update:modelValue'])
</script>

<style scoped>
.input-default {
  @apply appearance-none rounded border-2 border-gray-200 bg-gray-200 px-4 py-2 leading-tight text-gray-700 focus:border-slate-500 focus:bg-white focus:outline-none;
}

.label-default {
  @apply mb-0 font-bold text-gray-500;
}
</style>
