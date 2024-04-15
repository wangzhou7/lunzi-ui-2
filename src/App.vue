<template>
  <router-view />
</template>

<script lang="ts">
import { ref, provide } from 'vue'

export default {
  name: 'App',
  setup() {
   const visible = ref(true)
   provide('menuvisible', visible)// set
  }
}
</script>
