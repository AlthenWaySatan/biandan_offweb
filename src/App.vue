<template>
  <component :is="currentView" />
</template>
<script>
import Home from './pages/home.vue'
import Questions from './pages/question.vue'
import UserAgreement from './pages/userAgreement.vue'
import PrivacyStatement from './pages/PrivacyStatement.vue'

const routes = {
  '/': Home,
  '/questions': Questions,
  '/userAgreement': UserAgreement,
  '/privacyStatement': PrivacyStatement,
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || Home
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
    })
  }
}
</script>
