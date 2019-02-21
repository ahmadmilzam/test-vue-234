<template>
  <div class="c-post-thumbnail">
    <div class="c-post-thumbnail__head">
      <img
        :src="imageUrl"
        class="c-post-thumbnail__img">
    </div>
    <div class="c-post-thumbnail__body">
      <div class="c-post-thumbnail__title">
        {{ truncate(title, 30) }}
      </div>
      <div class="c-post-thumbnail__description">
        {{ truncate(description, 80) }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imageUrl: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
  methods: {
    truncate(string, max, useWordBoundary = false) {
      if (string.length <= max) {
        return string;
      }
      const subString = string.substr(0, max - 1);

      if (useWordBoundary) {
        return `${subString.substr(0, subString.lastIndexOf(' '))}...`;
      }
      return `${subString}...`;
    },
  },
}
</script>

<style lang="scss">
@import "~assets/scss/variables";

.c-post-thumbnail {
  display: block;
  margin: 0;
  padding: rem-calc($global-spacing-unit--micro);
  border: 1px solid #ddd;
  border-radius: 4px;
  box-shadow: 0px 1px 2px rgba(#000, .1);
}

.c-post-thumbnail__head {
  display: block;
  margin: 0;
  padding: rem-calc($global-spacing-unit--tiny);
}

.c-post-thumbnail__img {
  display: block;
  max-width: 100%;
  height: auto;
}

.c-post-thumbnail__body {
  display: block;
  padding: rem-calc($global-spacing-unit--tiny);
}

.c-post-thumbnail__title {
  display: block;
  font-size: rem-calc(16);
  font-weight: 600;
  line-height: 1.3;
  margin-bottom: rem-calc($global-spacing-unit--micro);
  color: $color-black;
}

.c-post-thumbnail__description {
  display: block;
  color: $color-black;
}
</style>
