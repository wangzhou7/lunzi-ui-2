<script lang="ts">
import { ref, provide } from 'vue'

export default {
  name: 'App',
  setup() {
    const width = document.documentElement.clientWidth
    const visible = ref(width <= 500 ? false : true)
    provide('menuvisible', visible)// set
  }
}
</script>




<template>
  <router-view />
</template>
