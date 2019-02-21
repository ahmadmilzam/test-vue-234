<template>
  <div id="app-container">
    <PageHead :links="links"/>
    <div class="o-box">
      <nuxt/>
    </div>
  </div>
</template>

<script>
import PageHead from '~/components/header/PageHead';

export default {
  components: {
    PageHead,
  },
  data() {
    return {
      links: [
        {
          name: 'home',
          path: '/',
          label: 'Home'
        },
        {
          name: 'posts',
          path: '/posts',
          label: 'Posts'
        },
        {
          name: 'about',
          path: '/about',
          label: 'About Us'
        },
        {
          name: 'login',
          path: '/admin/auth',
          label: 'Login'
        },
      ],
    }
  },
}
</script>
