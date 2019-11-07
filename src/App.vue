<template>
  <nb-container>
    <AppHeader title="Shutsen" @toggle="onToggle"/>
    <AppSidebar v-if="showSidebar"/>
    <AppContent/>
  </nb-container>
</template>

<script>
import AppHeader from './layout/AppHeader'
import AppSidebar from './layout/AppSidebar'
import AppContent from './layout/AppContent'

export default {
  components: { AppHeader, AppSidebar, AppContent },
  data () {
    return {
      showSidebar: false
    }
  },
  methods: {
    onToggle() {
      this.showSidebar = !this.showSidebar
    }
  }
}
</script>
