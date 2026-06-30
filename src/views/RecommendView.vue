<template>
  <SecondaryLayout st="申报书" :si="si" v-model="key" pt="申报书" cr="申报书">
    <ContentLoader base="recommend" />
  </SecondaryLayout>
</template>

<script setup>
import { ref } from 'vue'
import SecondaryLayout from '@/components/SecondaryLayout.vue'
import ContentLoader from '@/components/ContentLoader.vue'

const si = [{key:'recommend',label:'申报书',path:'/recommend'}]
const key = ref('recommend')
</script>

<style lang="scss" scoped>
</style>
