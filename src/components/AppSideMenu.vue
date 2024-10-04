<template>
  <v-navigation-drawer >
    <v-list item-props :items="links" />
  </v-navigation-drawer>
</template>

<script lang="ts" setup>
defineProps({
  drawer: Boolean
})
const links = ref([
  {
    title: "Home",
    prependIcon: "mdi-view-dashboard-outline",
    link: true,
    to: "/",
  },
  {
    title: "About",
    prependIcon: "mdi-view-dashboard-outline",
    link: true,
    to: "/about",
  }
])
</script>