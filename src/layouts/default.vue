<template>
  <v-app>
    <AppSideMenu :drawer="drawer" @update:drawer="updateDrawer" />
    <div>
      <AppHeader @changeState="toggleDrawer" />
      <v-main>
        <router-view />
      </v-main>
      <AppFooter />
    </div>
  </v-app>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const drawer = ref(true);

onMounted(() => {
  window.innerWidth >= 1024 ? drawer.value = true : drawer.value = false;
})

function updateDrawer(value: boolean) {
  drawer.value = value;
}

function toggleDrawer() {
  drawer.value = !drawer.value;
}
</script>
