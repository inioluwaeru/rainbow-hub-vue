<script setup>
import Header from './components/Header.vue'
import Body from './components/Body.vue'
import Footer from './components/Footer.vue'
import View from './components/Vie.vue'
import Product from './components/Product.vue' 
import Contact from './components/Contact.vue' 
</script>

<template>
  <transition name="fade">
    <div v-if="toggle">
      <View @close="togglePro"/>
    </div>
  </transition>
    <Header />
    <Body />
    <Product @open="togglePro"/>
    <Contact />
    <Footer />
</template>

<style scoped>
  .fade-enter-active,
        .fade-leave-active {
        transition:  0.2s ease;
        opacity: 1;
        }

        .fade-enter-from,
        .fade-leave-to {
        opacity: 0;
        }
</style>

<script>
export default {
  name: 'App',
  data() {
    return {
      toggle: false
    }
  },
  components: {
    View,
    Header,
    Body,
    Footer
  },
  methods: {
    togglePro() {
      this.toggle = !this.toggle
    },
    t() {
      alert('we')
    }
  }
  }
</script>