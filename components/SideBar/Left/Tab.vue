<script setup lang="ts">
const {defaultTransition} = useTailwindConfig()

const props = defineProps({
  active: {
    type: Boolean,
    default: false
  }
})

const textClasses = computed(() => props.active ? 'font-semibold' : 'text-normal')
</script>

<template>
  <nuxt-link to="#" class="flex items-center p-3 w-min hover:bg-gray-200 rounded-full">
    <div class="w-6 h-6 text-dark hover:bg-red-200" :class="defaultTransition">
      <slot name="icon"></slot>
    </div>

    <div class="ml-4 text-xl" :class="textClasses">
      <slot name="name"></slot>
    </div>
  </nuxt-link>
</template>

<style scoped>

</style>