<script lang="ts" setup>
import { capitalize } from '~/utils/str'

// composable
const { t } = useLang()

// compiler macro
definePageMeta({
  layout: 'page',
})
useHead(() => ({
  title: capitalize(t('pages.speakers.title')),
  meta: [
    {
      name: 'description',
      content: t('pages.speakers.description'),
    },
  ],
}))
</script>

<template>
  <PageContentRenderer
    path="/page/speakers"
    :page-title="$t('pages.speakers.title')"
  />
</template>
