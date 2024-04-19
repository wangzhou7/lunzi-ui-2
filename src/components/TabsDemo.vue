<template>
    <div>
        Tabs 示例
        <h2>示例1</h2>
        <Tabs>
            <Tab title="导航1">内容1</Tab>
            <Tab title="导航2">内容2</Tab>
        </Tabs>
    </div>
</template>
<script lang="ts">
import Tabs from '../lib/Tabs.vue';
import tab from '../lib/tab.vue';
export default {
    components:{
        Tabs,
        tab
    }
    
}
</script>


<style lang="scss">
</style>
