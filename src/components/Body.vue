<template>
    <div>
        <Nav />
        <Page />
        <Product />
        <Contact />
    </div>
</template>

<script>
import Nav from '../components/body-components/Navbar.vue'
import Page from '../components/body-components/Page.vue'
import Product from '../components/body-components/Product.vue'
import Contact from '../components/body-components/Contact.vue'

export default {
  name: 'App',
  components: {
      Nav,
      Page,
      Product,
     Contact
  }
}
</script>