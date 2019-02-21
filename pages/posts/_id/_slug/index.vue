<template>
  <div class="single-post-page">
    detail post page
  </div>
</template>

<script>
import axios from 'axios'

export default {
  asyncData(context) {
    // to use axios in asyncData or nuxtServerInit
    // context.app.$axios.$[get|post|put]
    // response data no longer wrapped in response object
    // you can directly use data as promise result
    // OLD
    // $axios.get('url/123 ').then(res), use res.data
    // NEW
    // $axios.get('url/123').then(data), use data directly
    console.log('vue asyncData context: ', context);
  }
};
</script>
