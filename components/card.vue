<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-4by3">
        <img class="artist-img" :src="artist.img" alt="Placeholder image" />
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <figure class="image is-48x48">
            <img
              src="https://bulma.io/images/placeholders/96x96.png"
              alt="Placeholder image"
            />
          </figure>
        </div>
        <div class="media-content">
          <p class="title is-4">{{ artist.name }}</p>
          <p class="subtitle is-6">{{ artist.handle }}</p>
        </div>
      </div>

      <div class="content">
        {{ artist.bio }}<a>@bulmaio</a>. <a href="#">#css</a>
        <a href="#">#responsive</a>
        <br />
        <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["artist"]
};
</script>

<style scoped>
.card {
  width: 300px;
  margin: 1em;
}

.artist-img {
  background-size: cover;
  background-position: center;
}
</style>
