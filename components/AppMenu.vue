<template>
  <nav>
    <AppLogo />
    <ul>
      <li><nuxt-link exact to="/">Home</nuxt-link></li>
      <li><nuxt-link to="/restaurants">Restaurants</nuxt-link></li>
      <li><nuxt-link to="/about">About</nuxt-link></li>
    </ul>
    <div class="smallnum" v-if="cartCount > 0">{{ cartCount }}</div>
    <nuxt-link to="/cart">Cart</nuxt-link>
  </nav>
</template>

<script>
import { mapGetters } from "vuex";

import AppLogo from "@/components/AppLogo.vue";

export default {
  components: {
    AppLogo,
  },
  computed: {
    ...mapGetters(["cartCount"]),
  },
};
</script>

<style lang="scss" scoped></style>
