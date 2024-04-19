<template>
    <div>Dialog 示例</div>
    <h2>示例1</h2>
    <Button @click="toggle">toggle</Button>
    <Dialog v-model:visible="x" :closeOnClickoverly="false" 
    :ok="f1" :cancel="f2" :onClickoverly="f3">
    <template v-slot:content>
        <strong>你好</strong>
        <div>hi</div>
    </template>
    <template v-slot:title>
        <strong>加粗的标题</strong>
    </template>
    </Dialog>
    <h2>示例2</h2>
    <Button @click="showDialog"> show </Button>
</template>

<script lang="ts">
import Dialog from "../lib/Dialog.vue";
import Button from "../lib/Button.vue";
import { ref }  from 'vue'
import { openDialog } from "../lib/openDialog.ts";
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
        const f3 = ()=>{}
        const showDialog = () =>{
            openDialog ({
                title:'标题',
                content:'你好'
            })
        }
        return {x,toggle,f1,f2,f3,showDialog}
    },
}
</script>

<style lang="scss">
</style>