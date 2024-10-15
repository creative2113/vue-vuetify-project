<template>
  <v-app-bar>
    <v-app-bar-nav-icon v-if="$vuetify.display.mdAndDown" @click="emitChange" />
    <v-app-bar-title>header</v-app-bar-title>
    <template #append>
      <v-btn icon slim>
        <v-avatar color="surface" image="@/assets/avatar_1.jpg" size="32"></v-avatar>
        <v-menu activator="parent">
          <v-list density="compact" nav>
            <v-list-item append-icon="mdi-cog-outline" link to="/setting" title="Settings" />
            <v-list-item append-icon="mdi-logout" link title="Logout" />
          </v-list>
        </v-menu>
      </v-btn>
    </template>
  </v-app-bar>
</template>
<script lang="ts" setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['changeState']);

function emitChange() {
  emit('changeState');
}
</script>