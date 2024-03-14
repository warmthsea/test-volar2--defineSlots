<script lang="ts" setup>
defineSlots<{
  default: (props: { msg: string }) => any
  event: (props: {
    row: string
    index: number
  }) => any
}>()
</script>

<template>
  <div>
    test D
    <slot msg="111" />
    <slot name="event" row="111" :index="1" />
  </div>
</template>
