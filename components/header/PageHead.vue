<template>
  <header class="c-pagehead">
    <PageNav :links="links"/>
  </header>
</template>

<script>
import PageNav from '@/components/header/PageNav';

export default {
  components: {
    PageNav,
  },
  props: {
    links: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss">
@import "~assets/scss/variables";

$pagehead-height: 60px;
$pagehead-bgcolor: #34495e;

$pagenav-link-color: #fff;

.c-pagehead {
  display: block;
  padding: 0;
  margin: 0;
  height: rem-calc($pagehead-height);
  background-color: $pagehead-bgcolor;
  box-shadow: 0px 1px 2px rgba(#000, .2);
}

.c-pagenav {
  display: flex;
  padding: 0;
  margin: 0;
}

.c-pagenav__link {
  display: inline-flex;
  height: rem-calc($pagehead-height);
  line-height: rem-calc($pagehead-height);
  padding-left: rem-calc($global-spacing-unit);
  padding-right: rem-calc($global-spacing-unit);
  text-decoration: none;
  outline: none;
  background-color: $pagehead-bgcolor;
  color: #fff;

  &,
  &:hover,
  &:active,
  &:focus {
    color: $pagenav-link-color;
  }

  &:hover,
  &.is-active {
    background-color: #2c3e50;
  }

  &:hover {
    transition: background-color .3s ease-out;
  }
}
</style>
