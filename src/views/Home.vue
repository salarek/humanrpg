<template>
  <div class="home">
    <header class="header-bar">
      <button type="button" class="btn btn-light">Light</button>
    </header>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {},
};
</script>
<style lang="scss" scoped>
.home {
  background-color: rgba($color: #67fff7, $alpha: 1);
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.header-bar {
  background-color: #7e7e7e;
  width: 100%;
  height: 10vh;
}
</style>
