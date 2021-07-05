<template>
  <div class="container p-2">
    <div class="p-5 bg-blue-100 border-l-4 border-blue-400 text-blue-500 text-sm font-bold">
      {{ titulo }}
    </div>
  </div>
</template>
<script>
  export default {
    name: 'Card',
    props: {
      titulo: { type: String, default: ''}
    }
  }
</script>
