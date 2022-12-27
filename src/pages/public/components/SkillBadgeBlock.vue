<template>
  <va-card-block class="flex row">
    <va-badge v-for="(item, i) in arr" :key="i" class="column mr-4">
      <va-button :color="color" size="small">{{ item }}</va-button>
    </va-badge>
  </va-card-block>
</template>

<script>
  export default {
    name: 'SkillBadgeBlock',
    props: {
      arr: Array,
      color: String,
    },
  }
</script>

<style scoped></style>
