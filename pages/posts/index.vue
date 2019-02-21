<template>
  <div class="o-layout">
    <div class="o-layout__item">
      <h1>List of Post</h1>

      <div class="o-layout">
        <div
          v-for="n in 4"
          :key="n"
          class="o-layout__item u-3of12">
          <nuxt-link :to="'/posts/1'">
            <PostThumbnail
              image-url="http://placehold.it/320x200"
              title="Some Post Title Here and There"
              description="Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam, repellat! Asperiores, voluptas! Fuga numquam inventore, aut non natus itaque nobis"/>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PostThumbnail from '~/components/posts/Thumbnail';

export default {
  components: {
    PostThumbnail,
  }
}
</script>
