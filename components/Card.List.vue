<template>
<div>
    <h1>{{category}}</h1>  
  <div class="container">
    <div class="columns is-multiline is-variable is-4" >

   <div class="column is-one-third-desktop">
    <Card :title="'aaaaa'" :imageurl="'https://pbs.twimg.com/media/D9QDO_qUcAEsDok.jpg'" 
    :main="'テキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキスト'"/>
   </div>

   <div class="column is-one-third-desktop">
     <Card :title="'bbbbb'" :imageurl="'https://pbs.twimg.com/media/D9P-UR5UEAEUZiB.png'" 
     :main="'テキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキスト'"/>
     </div>
  
   <div class="column is-one-third-desktop">
    <Card :title="'cccccc'" :imageurl="'https://pbs.twimg.com/media/D9QDO_qUcAEsDok.jpg'"
    :main="'テキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキストテキスト'" />
   </div>
   
        </div>
    </div>
</div>

</template>
<script>
import Logo from '~/components/Logo.vue'
import Card from '~/components/Card.vue'

export default {
    props: ['category'],
  components: {
    Logo,
    Card
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
