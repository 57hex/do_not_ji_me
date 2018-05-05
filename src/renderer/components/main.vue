<template>
  <div>
    <loginPage @updateLogin="getSignInStatus" v-if="login !== true"></loginPage>
    <div v-if="login !== false">
      <game_main @updateLogin="getSignInStatus"></game_main>
    </div>
  </div>
</template>

<script>
  import loginPage from './login'
  import game_main from './game-main'
  export default {
    name: "main",
    components: { loginPage, game_main },
    data() {
      return {
        res: '',
        login: false,
      }
    },
    computed: {},
    methods: {
      getSignInStatus (status) {
        let vm = this
        vm.login = status
      },
      signOut () {
        let vm = this
        vm.login = false
      }
    }
  }
</script>

<style scoped>

</style>