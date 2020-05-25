<template>
  <div class="gallery" id="gallery">
    <div class="gallery-panel"
         v-for="photo in photos"
         :key="photo.id">
      <router-link :to="`/photo/${photo.id}`">
        <img :src="thumbUrl(photo.filename)">
      </router-link>
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
    };
  },
  methods: {
    thumbUrl(filename) {
      console.log(filename);
      return require(`../assets/eng_pics/${filename}`);
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
    object-position: 0% 0%;
    border-radius: 0.75rem;
  }
</style>
