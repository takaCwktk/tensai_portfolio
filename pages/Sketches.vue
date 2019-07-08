<template>
    <div>
        <CardList :category="'sketches'" :posts="posts" />
    </div>
</template>

<script>
import CardList from '~/components/Card.List.vue'

export default {
  components: {
    CardList
  },
  async asyncData (context) {
    const { data } = await context.app.$axios.get(`https://api.storyblok.com/v1/cdn/stories`, {
      params: {
        token: 'Z3wB1rsLPBLMjjRBlEgAcgtt',
        starts_with: 'sketches',
        cv: "CURRENT_TIMESTAMP"
      }
    })

    return {
      posts: data.stories,
    }
  },
}
</script>