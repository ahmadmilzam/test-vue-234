<template>
  <div class="c-panel">
    <div class="c-panel__head">
      <div class="c-panel__title">
        <slot name="title"/>
      </div>
    </div>
    <div class="c-panel__body">
      <slot/>
    </div>
  </div>
</template>

<style lang="scss">
@import "~assets/scss/variables";

$panel-title-font-size: 18px !default;

.c-panel {
  position: relative;

  display: block;
  margin-bottom: rem-calc($global-spacing-unit--small);

  background-color: $color-white;
  box-shadow: 0 2px 1px rgba($color-black, .2);
  border-radius: $global-border-radius;
  border: 1px solid $color-sand--dark;
}

.c-panel__head {
  position: relative;
  padding: rem-calc($global-spacing-unit--small $global-spacing-unit);
  background-color: $color-sand--light;
  border-bottom: 1px solid $color-sand--dark;
}

.c-panel__title {
  cursor: pointer;
  display: block;
  height: auto; // reset height that has been set on another rules
  padding: 0; // reset padding that has been set on another rules
  margin: 0; // reset margin that has been set on another rules

  line-height: 1.4;
  font-weight: bold;
  font-size: rem-calc($panel-title-font-size);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.c-panel__body {
  padding: rem-calc($global-spacing-unit);

  > :last-child {
    margin-bottom: 0;
  }
}

</style>
