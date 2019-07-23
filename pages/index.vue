<template>
  <div>
    <CardList :category="'3Dworks'" :posts="posts.filter((post) => post.content.component === '3dwork').slice(0,3)" />
    <CardList :category="'Sketches'" :posts="posts.filter((post) => post.content.component === 'sketch').slice(0,3)" />
    <CardList :category="'PhotoDiaries'" :posts="posts.filter((post) => post.content.component === 'photodiary').slice(0,3)" />
  </div>

</template>

<script>
import Logo from '~/components/Logo.vue'
import CardList from '~/components/Card.List.vue'
export default {
  components: {
    Logo,
    CardList
  },
  async asyncData (context) {
    const { data } = await context.app.$axios.get(`https://api.storyblok.com/v1/cdn/stories`, {
      params: {
        token: 'Ssm4K0OYn8WM6jQEe09Wygtt',
        cv: ""
      }
    })

    return {
      posts: data.stories,
    }
  },
}
</script>
