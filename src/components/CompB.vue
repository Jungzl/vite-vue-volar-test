<script lang="ts" setup>
  import CompA from './CompA.vue'; // using `unplugin-vue-components` and comment this line will throw error below

  defineOptions({
    name: 'CompB',
  })
</script>

<template>
  <CompA>
    <!-- ^^^ Property 'CompA' does not exist on type 'Pick<IntrinsicElements, "template"> & Pick<IntrinsicElements, "div">'. -->
    <template #default="{ foo, buz }">
      <div>
        {{ foo }}{{ buz }}
      </div>
    </template>
  </CompA>
</template>

<style lang="scss" scoped></style>
