<template>
  <div>Button 示例 </div>
  <h2>示例1</h2>
  <div>
    <Button @click="onClick">hello</Button>
    <Button theme="button">hello</Button>
    <Button theme="text">hello</Button>
    <Button theme="link">hello</Button>
  </div>
  <h2>示例2</h2>
  <div>
    <Button level="main">Main button</Button>
    <Button>Normal button</Button>
    <Button level="danger">Danger button</Button>
  </div>
  <div>
    <Button theme="text" level="main">Main text button</Button>
    <Button theme="text">Normal Text button</Button>
    <Button theme="text" level="danger">Danger text button</Button>
  </div>
  <div>
    <Button theme="link" level="main">Main link button</Button>
    <Button theme="link">Normal link button</Button>
    <Button theme="link" level="danger">Danger link button</Button>
  </div>
  <h2>示例3</h2>
  <div>
    <Button size="big">Big</Button>
    <Button>Normal</Button>
    <Button size="small">Small</Button>
  </div>
  <div>
    <Button theme="text" size="big">Big</Button>
    <Button theme="text">Normal</Button>
    <Button theme="text" size="small">Small</Button>
  </div>
  <div>
    <Button theme="link" size="big">Big</Button>
    <Button theme="link">Normal</Button>
    <Button theme="link" size="small">Small</Button>
  </div>

  <h2>示例4</h2>
  <div>
    <Button disabled> Disable button </Button>
    <Button theme="text" disabled>Disable text button</Button>
    <Button theme="link" disabled>Disable link button</Button>
  </div>
  <h2>示例5</h2>
  <div>
    <Button loading> Loading </Button>
    <Button> Loaded </Button>
  </div>
</template>


<script lang="ts">
import Button from '../lib/Button.vue';
export default {
  components: { Button },
  setup() {
    const onClick = () => {
      console.log('hi')
    }
    return { onClick }
  }
}
</script>

<style lang="scss"></style>