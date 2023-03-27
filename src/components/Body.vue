<template>
    <div>
        <Nav />
        <Page />
    </div>
</template>

<script>
import Nav from '../components/body-components/Navbar.vue'
import Page from '../components/body-components/Page.vue'

export default {
  name: 'App',
  components: {
      Nav,
      Page,
  }
}
</script>