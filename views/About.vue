<template>
  <div class="about">
    <h1>This is an about page</h1>
    <HelloWorld msg="Welcome in About"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'About',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
.about {
  border: 1px solid red;
  padding: 30px;
}
</style>