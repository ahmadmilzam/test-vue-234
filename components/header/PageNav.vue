<template>
  <nav class="c-pagenav">
    <PageNavItem
      v-for="(link, idx) in links"
      :key="idx"
      :link="link"/>
  </nav>
</template>

<script>
import PageNavItem from '@/components/header/PageNavItem.vue';

export default {
  components: {
    PageNavItem,
  },
  props: {
    links: {
      type: Array,
      required: true,
    },
  },
}
</script>
