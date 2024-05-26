<template>
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleDrawer"></q-btn>
        <q-toolbar-title>
          <div class="text-h6">Sneakyboyy Motor</div>
        </q-toolbar-title>
        <q-btn flat dense round icon="search" aria-label="Search"></q-btn>
        <q-btn flat dense round icon="notifications" aria-label="Notifications"></q-btn>
        <q-avatar>
          <img src="https://i.vimeocdn.com/portrait/9101361_640x640">
        </q-avatar>
      </q-toolbar>
    </q-header>
  </template>
  
  <script>
  export default {
    methods: {
      toggleDrawer() {
        this.$emit('toggle-drawer');
      }
    }
  }
  </script>
  
  <style scoped>
  </style>
  