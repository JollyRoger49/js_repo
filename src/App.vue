<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <MainPage />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue'
import MainPage from './components/MainPage.vue'

export default {
  name: 'LayoutDefault',

  components: {
    MainPage
  },

  setup () {
    return {
      leftDrawerOpen: ref(true)
    }
  }
}
</script>
