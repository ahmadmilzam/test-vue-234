<template>
  <div class="c-auth-page">
    <div class="c-auth-page__form">
      <h1 class="u-h4">Welcome Back, Admin!</h1>
      <div class="o-layout u-margin-bottom--tiny">
        <div class="o-layout__item">
          <label
            for="#email"
            class="c-input-label">Email</label>
          <input
            type="text"
            class="c-input">
        </div>
      </div>
      <div class="o-layout u-margin-bottom--tiny">
        <div class="o-layout__item">
          <label
            for="#email"
            class="c-input-label">Password</label>
          <input
            type="password"
            class="c-input">
        </div>
      </div>
      <div class="o-layout u-margin-bottom">
        <div class="o-layout__item u-6of12">
          <button
            type="button"
            class="c-btn c-btn--primary c-btn--block">Login</button>
        </div>
        <div class="o-layout__item u-6of12">
          <button
            type="button"
            class="c-btn c-btn--block">Signup</button>
        </div>
      </div>
      <div class="u-text-right">
        <nuxt-link to="/"><small>Back to homepage</small></nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'blank',
}
</script>

<style lang="scss">
@import "~assets/scss/variables";

.c-auth-page {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}

.c-auth-page__form {
  display: block;
  margin: 0;
  padding: rem-calc($global-spacing-unit);
  width: rem-calc(300);
  max-width: rem-calc(400);
  height: auto;
  border: 1px solid #ddd;
  border-radius: 4px;
  box-shadow: 0px 1px 2px rgba($color-black, .1);
}
</style>
