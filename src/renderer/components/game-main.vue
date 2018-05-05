<template>
  <div class="body">
    <b-navbar class="nav-red" toggleable>
      <b-navbar-toggle target="nav_dropdown_collapse"></b-navbar-toggle>
      <b-collapse is-nav id="nav_dropdown_collapse">
        <b-navbar-nav>
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#" @click="loginOut">登出</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <b-container>
      <b-row class="mt-5">
        <b-col sm="6"><b-jumbotron class="nav-red btn-click"><h1 class="text-center">電腦對戰</h1></b-jumbotron>
        </b-col>
        <b-col sm="6"><b-jumbotron class="nav-red btn-click"><h1 class="text-center">玩家對戰</h1></b-jumbotron>
      </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
  export default {
    name: "game-main",
    data () {
      return {
        signedIn: true
      }
    },
    methods: {
      loginOut() {
        let vm = this
        vm.signedIn = false
        vm.$emit('updateLogin', vm.signedIn)
      }
    }
  }
</script>
<style scoped>
  .nav-red {
    background-color: #FF6773;
    border-color: #FF6773;
    color: #F0F8FF;
  }
  .btn-click{
    transition: .2s ease;
  }
  .btn-click:active {
    background-color: #9D3F47;
    border-color: #9D3F47;
  }
  .body {
    height: 100%;
    width: 100%;
    position: fixed;
    background-color: #303133;
    color: #F0F8FF;
  }
</style>