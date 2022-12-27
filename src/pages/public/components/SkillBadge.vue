<template>
  <SkillBadgeBlock :arr="getSkill('language')" color="" />
  <SkillBadgeBlock :arr="getSkill('database')" color="#EEE" />
  <SkillBadgeBlock :arr="getSkill('framework')" color="warning" />
  <SkillBadgeBlock :arr="getSkill('devops')" color="success" />
</template>

<script>
  export default {
    name: 'SkillBadge',
    props: {
      company: String,
    },
    methods: {
      getSkill(type) {
        return this.t(
          {
            language: ['timelines', 'skills', this.company, 'language'].join('.'),
            database: ['timelines', 'skills', this.company, 'database'].join('.'),
            devops: ['timelines', 'skills', this.company, 'devops'].join('.'),
            framework: ['timelines', 'skills', this.company, 'framework'].join('.'),
          }[type],
        ).split(',')
      },
    },
  }
</script>

<script setup>
  import { useI18n } from 'vue-i18n'
  import { useColors } from 'vuestic-ui'
  import SkillBadgeBlock from './SkillBadgeBlock.vue'

  const { colors } = useColors()
  const { t } = useI18n()
</script>

<style scoped>
  :root {
    /* Text */
    --va-badge-text-py: 0;
    --va-badge-text-px: 0.2rem;
  }
</style>
