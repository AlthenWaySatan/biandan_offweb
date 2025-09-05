<template>
  <component :is="currentView" />
</template>
<script>
import Home from './pages/home.vue'
import Questions from './pages/question.vue'
import UserAgreement from './pages/userAgreement.vue'
import PrivacyStatement from './pages/PrivacyStatement.vue'
import HaveacupAgentPrivacyStatement from './htmlPages/HaveacupAgentPrivacyStatement.vue'
import HaveacupUserAgreement from './htmlPages/HaveacupUserAgreement.vue'
import XiangjiUserAgreement from './htmlPages/XiangjiUserAgreement.vue'

const routes = {
  '/': Home,
  '/questions': Questions,
  '/userAgreement': UserAgreement,
  '/privacyStatement': PrivacyStatement,
  '/haveacup_userAgreement': HaveacupUserAgreement,
  '/haveacup_agent_privacyStatement': HaveacupAgentPrivacyStatement,
  '/xiangji_userAgreement': XiangjiUserAgreement,
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
