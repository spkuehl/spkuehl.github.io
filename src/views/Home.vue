<template>
  <div>
    <Heading />
    <Navbar />
    <Gallery />
    <Venue />
  </div>
</template>

<script>
import Heading from '@/components/Heading.vue';
import Navbar from '@/components/Navbar.vue';
import Gallery from '@/components/Gallery.vue';
import Venue from '@/components/Venue.vue';
export default {
  name: 'home',
  components: {
    Heading,
    Navbar,
    Gallery,
    Venue,
  },
};
</script>
