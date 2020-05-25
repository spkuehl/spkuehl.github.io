<template>
  <div>
    <Heading />
    <Navbar />
    <Gallery />
  </div>
</template>

<script>
import Heading from '@/components/Heading.vue';
import Navbar from '@/components/Navbar.vue';
import Gallery from '@/components/Gallery.vue';
export default {
  name: 'home',
  components: {
    Heading,
    Navbar,
    Gallery,
  },
};
</script>
