<template>
  <div class="home">
    <header class="header-bar">
      <div style="padding: 12px" class="bg-primary text-white">Human RPG</div>
    </header>
    <div class="main-view">
      <div class="left-page">
        <div class="greetings-container">
          <div>chuj</div>
        </div>
      </div>
      <div class="right-page"><login /></div>
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
  height: 80%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.left-page {
  padding: 2%;
  min-width: 300px;
  width: 50%;
}
.right-page {
  position: relative;
  padding: 2%;
  min-width: 300px;
  width: 50%;
}
.greetings-container {
  font-size: 1rem;
  min-width: 300px;
  min-height: 300px;
  padding: 5%;
  position: relative;
  width: 100%;
  height: 100%;
  color: white;
  background-color: $secondary;
}
.greetings-container:before {
  content: "";
  width: 100%;
  height: 0;
  position: absolute;
  top: 0;
  left: 0;
  border-bottom: 19px solid $secondary;
  border-left: 19px solid #48d399;
  border-right: 19px solid #48d399;
}
.greetings-container:after {
  content: "";
  width: 100%;
  height: 0;
  position: absolute;
  bottom: 0;
  left: 0;
  border-top: 19px solid $secondary;
  border-left: 19px solid #48d399;
  border-right: 19px solid #48d399;
}
</style>
