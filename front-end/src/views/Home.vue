<template>
<div>
  <MyFleet v-if="user" />
  <HomePage v-else />
</div>
</template>

<script>
import HomePage from '@/components/HomePage.vue'
import MyFleet from '@/components/MyFleet.vue'
export default {
  name: 'home',
  components: {
    HomePage,
    MyFleet
  },
  computed: {
    user() {
      return this.$root.$data.user;
    }
  }
}
</script>
