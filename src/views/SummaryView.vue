<template>
  <SecondaryLayout st="总结报告" :si="si" v-model="key" pt="总结报告" :cr="curLabel">
    <ContentLoader base="summary" sub="index" />
  </SecondaryLayout>
</template>

<script setup>
import { ref, computed, watch } from 'vue'
import { useRoute } from 'vue-router'
import SecondaryLayout from '@/components/SecondaryLayout.vue'
import ContentLoader from '@/components/ContentLoader.vue'

const route = useRoute()
const si = [
  {key:'summary',label:'总结报告',path:'/summary'}
]
const key = ref('summary')
const curLabel = computed(() => '总结报告')
watch(() => route.query.section, (v) => { key.value = v || 'summary' })
</script>
