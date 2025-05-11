<script setup lang="ts">
const route = useRoute()
const breadcrumb = route.fullPath.split('/')
// const breadcrumb_div = useTemplateRef('breadcrumb_div')
breadcrumb[0] = 'Home'
</script>

<template>
    <h2 ref="breadcrumb_div">
      <span v-for="(item, index) in breadcrumb" :key="index">
        <span v-if="index !== 0" class="separator"> >> </span>
          <nuxt-link :to="`/${breadcrumb.slice(1, index + 1).join('/')}`">
            {{ item }}
          </nuxt-link>
      </span>
    </h2>
</template>

<style scoped>

h2{
  margin: 0; 
  word-spacing: 10px;
  font-size: medium;
  font-weight: 400;
  /* font-family: 'Alata'; */
}
</style>