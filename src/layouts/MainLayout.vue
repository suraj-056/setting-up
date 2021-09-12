<template>
  <q-layout view="lHr lpR fFf">

    <q-header  class="bg-white text-black">
      <q-toolbar>
      

        <q-toolbar-title class="text-bold">
          
          Switter
        </q-toolbar-title>

       
      </q-toolbar>
    </q-header>

    <q-drawer  show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <!-- drawer content -->
     <q-icon class="q-pa-lg" name="fas fa-dove" size="lg" color="primary" />


      <q-list >
      <q-item clickable v-ripple class="q-pa-md" to="/" exact>
        <q-item-section avatar>
          <q-icon size="md" name="home" />
        </q-item-section>

        <q-item-section><strong>Home</strong></q-item-section>
      </q-item>
      <q-item clickable v-ripple class="q-pa-md" to="/about" exact>
        <q-item-section avatar>
          <q-icon size="md" name="help" />
        </q-item-section>

        <q-item-section><strong>about</strong></q-item-section>
      </q-item>
      </q-list>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <!-- drawer content -->



       <q-input rounded outlined placeholder="Search Switter" class="q-pa-lg">
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>


      <q-list>
      <q-item clickable v-ripple>
        <q-item-section>
          <q-item-label class="text-bold">Single line item</q-item-label>
          <q-item-label caption lines="2">Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
         <q-icon size="1rem" name="fas fa-ellipsis-h" />
        </q-item-section>
      </q-item>
      <q-item clickable v-ripple>
        <q-item-section>
          <q-item-label class="text-bold">Single line item</q-item-label>
          <q-item-label caption lines="2">Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
         <q-icon size="1rem" name="fas fa-ellipsis-h" />
        </q-item-section>
      </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>