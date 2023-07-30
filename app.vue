<template>
  <div>
    <NuxtLayout>
      <Navbar />
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<script>
import Navbar from '~/components/__common/Navbar/Navbar.vue'
export default {
  components: {
    Navbar
  }
}
</script>
