<template>
  <v-app>
    <AppSideMenu :drawer="drawer" />
    <div>
      <AppHeader />
      <v-main>
        <router-view />
      </v-main>
      <AppFooter />
    </div>
  </v-app>
</template>

<script lang="ts" setup>
  const drawer = ref(true)
</script>
