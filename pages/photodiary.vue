<template>
    <div>
        <CardList :category="'photodiaries'" :posts="posts" />
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
        starts_with: 'photodiaries',
        cv: "CURRENT_TIMESTAMP"
      }
    })

    return {
      posts: data.stories,
    }
  },
}
</script>