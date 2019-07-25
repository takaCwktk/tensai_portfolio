<template>
    <div>
        <CardList :category="'3Dworks'" :posts="posts" />
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
        token: 'Am9M3mQT9L2ftXwZwyRD7Att',
        starts_with: '3dworks',
        cv: ""
      }
    })

    return {
      posts: data.stories,
    }
  },
}
</script>