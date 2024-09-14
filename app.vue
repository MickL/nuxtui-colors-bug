<script setup lang="ts">
const isVisible = ref(false);

const columns = [
  {
    key: 'colors'
  }
]
const rows = [
  {
    color: 'yellow',
  },
  {
    color: 'red',
  },
  {
    color: 'green',
  }
]
</script>

<template>
  <UTable :columns :rows>
    <template #colors-data="{row}">
      <div class="space-x-2">
        <UBadge :color="row.color" variant="subtle">Subtle Badge</UBadge>
        <UButton :color="row.color" variant="soft">Soft Button</UButton>
      </div>
    </template>
  </UTable>
</template>
