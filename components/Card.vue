<template>
    <div class="card">
  <div class="card-image">
    <figure class="image is-4by3">
      <img :src="imageurl" alt="image">
    </figure>
  </div>
  <div class="card-content">
    <div class="content">
    <h2>{{title}}</h2>
      {{main}}
      <a href="#">#css</a> <a href="#">#responsive</a><a href="#">#responsive</a>
      <br>
      <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
    </div>
  </div>
</div>
</template>

mounted



<script>



export default {
    props: ['imageurl','title','main']
    
}
</script>
