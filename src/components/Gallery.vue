<template>
<div class="container" id="gallery">
  <h3 class="text-center">Pictures of us</h3>
  <div class="gallery">
    <div class="gallery-panel"
         v-for="photo in photos"
         :key="photo.id" v-bind:class="{'gallerycollapse collapse':(photo.id > 7)}">
      <router-link :to="`/photo/${photo.id}`">
        <img :src="thumbUrl(photo.filename)">
      </router-link>
    </div>
  </div>

  <div class="accordion text-center" id="accordionExample">
        <h2 class="mb-0">
        <button v-show="!accordionToggle" v-on:click="toggleCollapse" class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target=".gallerycollapse" aria-expanded="false" aria-controls="collapseTwo">
          See more pictures
        </button>
        <button v-show="accordionToggle" v-on:click="toggleCollapse" class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target=".gallerycollapse" aria-expanded="false" aria-controls="collapseTwo" href="#gallery">
          <a href="#gallery">See less pictures</a>
        </button>
        </h2>
      </div>
</div>
</template>

<script>
import photos from '@/photos.json';
export default {
  name: 'Gallery',
  data() {
    return {
      photos,
      accordionToggle: false,
    };
  },
  methods: {
    thumbUrl(filename) {
      return require(`../assets/eng_pics/${filename}`);
    },
    toggleCollapse() {
      this.accordionToggle = !this.accordionToggle;
    },
  },
};
</script>

<style>
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(6rem, 1fr));
    grid-gap: 0.5rem;
    max-width: 80rem;
    margin: 1rem auto;
    padding: 0 5%;
  }
  .gallery-panel img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: 50% 0%;
    border-radius: 0.75rem;
  }
</style>
