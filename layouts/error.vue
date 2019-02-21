<template>
  <div class="c-error">
    <h1
      v-if="error.statusCode === 404"
      class="c-error__title">Halaman Tidak Ditemukan :(</h1>
    <h1
      v-else
      class="c-error__title">Oops! An error occurred</h1>
    <div class="c-error__text">
      Mohon maaf sekali, halaman yang anda tuju tidak dapat kami temukan.<br>
      Coba kembali dalam beberapa saat, atau anda bisa klik tombol di bawah ini<br>
      untuk kembali ke halaman depan.
    </div>
    <div class="c-error__action">
      <a
        href="/"
        class="c-btn">Ke Halaman Depan</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      required: true,
    }
  },
  layout: 'blank' // you can set a custom layout for the error page
}
</script>

<style lang="scss">
@import "~assets/scss/variables";

.c-error {
  display: flex;
  height: 100vh;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
  text-align: center;
}

.c-error__title {
  font-weight: 700;
  font-size: rem-calc(28);
  margin-bottom: rem-calc($global-spacing-unit);
}

.c-error__text {
  color: #999;
  font-size: rem-calc(14);
  margin-bottom: rem-calc($global-spacing-unit);
}
</style>
