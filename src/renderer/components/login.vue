<template>
    <div class="body darkTheme">
        <div class="main-block container">
            <h1 class="text-center mt-4">登入</h1>
            <b-row>
                <b-col sm="8" offset="2" class="mt-4">
                    <b-btn class="btn-red" style=" width:100%;">使用 google 登入</b-btn>
                </b-col>
            </b-row>
            <b-row class="mt-4">
                <b-col sm="12" class="text-center">- or -</b-col>
            </b-row>
            <b-row>
                <b-col sm="8" offset="2" class="mt-4 mb-4">
                    <b-form-input class="darkTheme" placeholder="請輸入帳號"></b-form-input>
                </b-col>
            </b-row>
            <b-row>
                <b-col sm="8" offset="2" class="mb-4">
                    <b-form-input class="darkTheme" placeholder="請輸入密碼"></b-form-input>
                </b-col>
            </b-row>
            <b-row>
                <b-col sm="8" offset="2">
                    <b-btn class="mb-4 btn-red" style=" width:100%;">登入</b-btn>
                </b-col>
            </b-row>

            <b-row>
                <b-col sm="8" offset="2" class="mb-4">
                    <b-btn style="width: 100%;">忘記密碼</b-btn>
                </b-col>
            </b-row>
        </div>
    </div>
</template>

<script>
  export default {
    name: "login"
  }
</script>

<style scoped>
  * {
        position: relative;
  }
  .body {
      height: 100%;
      width: 100%;
      position: fixed;
  }
  .main-block {
      position: absolute;
      height: 30rem;
      width: 20rem;
      background-color: rgba(27,27,27,0.5);
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
  }
  .btn-red {
      background-color: #FF6773;
      border-color: #FF6773;
  }
  .darkTheme {
      background-color: #303133;
      color: #F0F8FF;
    }
</style>