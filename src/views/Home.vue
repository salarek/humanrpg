<template>
  <div class="home">
    <header class="header-bar">
      <div style="padding: 12px" class="bg-primary text-white">Human RPG</div>
    </header>
    <div class="main-view">
      <div class="greetings-container">hello</div>
      <div class="login-form"><login /></div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import login from "@/components/login.vue";

export default {
  name: "Home",
  components: { login },
};
</script>
<style lang="scss" scoped>
@import "@/scss/variables";
.home {
  position: absolute;
  background-color: $primary;
  width: 100vw;
  height: 100vh;
  justify-content: center;
}
.header-bar {
  background-color: $secondary;
  width: 100%;
  height: 10vh;
  display: flex;
  flex-direction: row;
}
.main-view {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.greetings-container {
  padding: 2%;
  min-width: 300px;
  width: 50%;
}
.login-form {
  position: relative;
  padding: 2%;
  min-width: 300px;
  width: 50%;
}
</style>
