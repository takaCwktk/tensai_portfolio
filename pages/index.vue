<template>
  <div>
    <CardList :category="'3Dworks'"/>
    <CardList :category="'Sketches'"/>
    <CardList :category="'PhotoDiary'"/>
  </div>

</template>

<script>
import Logo from '~/components/Logo.vue'
import CardList from '~/components/Card.List.vue'


export default {
  components: {
    Logo,
    CardList
  }
}
</script>
