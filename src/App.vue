<script setup lang="ts">
import Todos from './components/Todos.vue'

import { Authenticator } from '@aws-amplify/ui-vue'
import '@aws-amplify/ui-vue/styles.css'

</script>

<template>
  <authenticator>
    <template v-slot="{ user, signOut }">
      <main>
        <h1>{{ user?.signInDetails?.loginId }}'s Todos</h1>
        <Todos />
        <button @click="signOut">Sign Out</button>
      </main>
    </template>
  </authenticator>


</template>
