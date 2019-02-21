<template>
  <nuxt-link
    :to="link.path"
    :exact="isHome(link)"
    class="c-pagenav__link"
    active-class="is-active">{{ link.label }}</nuxt-link>
</template>

<script>
export default {
  props: {
    link: {
      type: Object,
      required: true,
    },
  },
  methods: {
    isHome(link) {
      return link.path === '/';
    },
  },
}
</script>
