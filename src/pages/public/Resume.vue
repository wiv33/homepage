<template>
  <div class="row">
    <div class="flex flex xs12">
      <va-card-content stripe stripe-color="blue" class="flex">
        <va-card-block style="align-items: center">
          <va-image
            ratio="1"
            style="border-radius: 50%; width: 20%"
            class="flex md6 lg4"
            src="../../../public/40161102.jpg"
          />
        </va-card-block>
      </va-card-content>
      <va-card-content stripe stripe-color="blue">
        <va-card-block style="align-items: center">
          <va-card-title>
            안녕하세요. 각 사람의 장점으로 더 나은 소프트웨어를 만들어가는 개발자 고필성입니다.
          </va-card-title>
        </va-card-block>

        <!--        &lt;!&ndash;        <va-card-title> 안녕하세요! 개발을 좋아하는 고필성입니다.</va-card-title>&ndash;&gt;-->
        <!--        <va-card-content>-->
        <!--          <va-card-block style="align-items: center">-->
        <!--            <va-button-->
        <!--              class="app-navbar-center__github-button"-->
        <!--              href="mailto:qwer3@kakako.com"-->
        <!--              color="warning"-->
        <!--              target="_blank"-->
        <!--              icon="github"-->
        <!--            >-->
        <!--              qwer3@kakako.com-->
        <!--            </va-button>-->
        <!--            <va-button-->
        <!--              href="https://github.com/wiv33"-->
        <!--              color="#000000"-->
        <!--              class="app-navbar-center__github-button"-->
        <!--              icon="github"-->
        <!--              target="_blank"-->
        <!--            >-->
        <!--              {{ t("navbar.repository") }}-->
        <!--            </va-button>-->
        <!--          </va-card-block>-->
        <!--          <br />-->
        <!--        </va-card-content>-->
      </va-card-content>
    </div>
  </div>

  <div class="flex xs12">
    <va-card no-padding-h style="overflow-x: auto" class="timelines__horizontal-long">
      <va-card-title>{{ t('timelines.horizontalCards') }}</va-card-title>
      <va-card-content>
        <va-timeline align-top style="min-width: 600px" class="timelines__horizontal-long__timeline">
          <va-timeline-item active>
            <template #before>
              <div class="title va-text-center" :style="{ color: colors.primary }">
                {{ t('timelines.firstDate') }}
              </div>
            </template>
            <template #after>
              <va-card stripe stripe-color="warning" class="mb-0">
                <va-card-title>{{ t('timelines.titleDateFirst') }}</va-card-title>
                <va-card-content>{{ t('timelines.contentFirst') }}</va-card-content>
              </va-card>
            </template>
          </va-timeline-item>
          <va-timeline-item active>
            <template #before>
              <div class="title va-text-center" :style="{ color: colors.primary }">
                {{ t('timelines.secondDate') }}
              </div>
            </template>
            <template #after>
              <va-card stripe stripe-color="info" class="mb-0">
                <va-card-title>{{ t('timelines.titleDateSecond') }}</va-card-title>
                <va-card-content>{{ t('timelines.contentSecond') }}</va-card-content>
              </va-card>
            </template>
          </va-timeline-item>
        </va-timeline>
      </va-card-content>
    </va-card>
  </div>

  <div class="timelines">
    <div class="row">
      <div class="flex xs12">
        <va-card no-padding-h style="overflow-x: auto"></va-card>
      </div>

      <div class="flex xs12">
        <va-card no-padding-h style="overflow-x: auto" class="timelines__horizontal-long"></va-card>
      </div>

      <div class="flex xs12">
        <va-card no-padding-v>
          <va-card-title>{{ t('timelines.verticalLabel') }}</va-card-title>
          <va-card-content>
            <va-timeline vertical>
              <va-timeline-item active>
                <template #before>
                  <span class="title va-timeline-item__text" :style="{ color: colors.primary }">
                    {{ t('timelines.company.NHN.date') }}
                  </span>
                  <SkillBadge company="NHN" />
                </template>
                <template #after>
                  <va-card stripe stripe-color="" class="mb-0">
                    <va-card-title>{{ t('timelines.company.NHN.title') }}</va-card-title>
                    <va-card-content>{{ t('timelines.company.NHN.content') }}</va-card-content>
                  </va-card>
                </template>
              </va-timeline-item>
            </va-timeline>
          </va-card-content>
        </va-card>
      </div>

      <div class="flex xs12">
        <va-card no-padding-v>
          <va-card-title>{{ t('timelines.verticalCentered') }}</va-card-title>
          <va-card-content>
            <va-timeline vertical centered style="min-width: 300px">
              <va-timeline-item color="danger" active>
                <template #before>
                  <span class="title title--danger va-timeline-item__text" :style="{ color: colors.danger }">
                    {{ t('timelines.company.JOINS.date') }}
                  </span>
                  <SkillBadge company="JOINS" />
                </template>
                <template #after>
                  <va-card stripe stripe-color="warning" class="mb-0">
                    <va-card-title>{{ t('timelines.company.JOINS.title') }}</va-card-title>
                    <va-card-content>{{ t('timelines.company.JOINS.content') }}</va-card-content>
                  </va-card>
                </template>
              </va-timeline-item>
            </va-timeline>
          </va-card-content>
        </va-card>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Resume',
  }
</script>
<script setup>
  /**
   * HIDDEN FROM THE ADMIN! SEE src/components/sidebar/NavigationRoutes.ts AND src/pages/admin/ui/route.ts TO REVEAL.
   */
  import { useI18n } from 'vue-i18n'
  import { useColors } from 'vuestic-ui'
  import SkillBadge from './components/SkillBadge.vue'

  const { t } = useI18n()
  const { colors } = useColors()
</script>

<style lang="scss">
  :root {
    font-size: xx-large;
  }
</style>
