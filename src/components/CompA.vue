<script lang="ts" setup>
  import { ref } from 'vue'

  defineOptions({
    name: 'CompA',
  })

  const foo = ref('bar')

  defineSlots<{
    default: {
      foo: string,
      buz: number
    }
  }>()
</script>

<template>
  <div>
    <slot v-bind="{ foo }" />
    <!-- ^^^ Property 'slot' does not exist on type 'Pick<IntrinsicElements, "div">'. -->
  </div>
</template>

<style lang="scss" scoped>

</style>
