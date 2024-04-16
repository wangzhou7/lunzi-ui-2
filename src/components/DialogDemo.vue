<template>
    <div>Dialog 示例</div>
    <h2>示例1</h2>
    <Button @click="toggle">toggle</Button>
    <Dialog v-model:visible="x" :closeOnClickoverly="false" 
    :ok="f1" :cancel="f2">
    <template v-slot:content>
        <strong>你好</strong>
        <div>hi</div>
    </template>
    <template v-slot:title>
        <strong>加粗的标题</strong>
    </template>
    
    </Dialog>
</template>

<script lang="ts">
import Dialog from "../lib/Dialog.vue";
import Button from "../lib/Button.vue";
import { ref }  from 'vue'
export default {
    components:{
        Dialog,
        Button
    },
    setup() {
        const x = ref(false)
        const toggle = () =>{
            x.value = !x.value
        }
        const f1 = ()=>{
            return false
        }
        const f2 = ()=>{}
        return {x,toggle,f1,f2}
    },
}
</script>

<style lang="scss">
</style>