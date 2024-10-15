<template>
  <v-navigation-drawer :model-value="drawer" @update:model-value="updateDrawer">
    <v-list item-props :items="links" />
  </v-navigation-drawer>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  drawer: {
    type: Boolean,
    required: true,
  },
});

const emit = defineEmits(['update:drawer']);

function updateDrawer(value) {
  emit('update:drawer', value);
}

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