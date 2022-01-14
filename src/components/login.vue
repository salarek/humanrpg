<template>
  <div class="login">
    <div v-if="mode == 'login'">
      <div class="mb-3 row">
        <p>Logowanie</p>
        <label for="staticEmail" class="col-sm-2 col-form-label">Email</label>
        <div class="col-sm-10">
          <input type="text" class="form-control" id="staticEmail" />
        </div>
      </div>
      <div class="mb-3 row">
        <label for="inputPassword" class="col-sm-2 col-form-label"
          >Password</label
        >
        <div class="col-sm-10">
          <input type="password" class="form-control" id="inputPassword" />
        </div>
      </div>
    </div>

    <div v-if="mode == 'registration'">
      <div class="mb-3 row">
        <p>Rejestracja</p>
        <label for="staticEmail" class="col-sm-2 col-form-label">Email</label>
        <div class="col-sm-10">
          <input type="text" class="form-control" id="staticEmail" />
        </div>
      </div>
      <div class="mb-3 row">
        <label for="inputPassword" class="col-sm-2 col-form-label"
          >Password</label
        >
        <div class="col-sm-10">
          <input type="password" class="form-control" id="inputPassword" />
        </div>
      </div>
    </div>
    <div class="col-auto">
      <button
        type="submit"
        class="btn btn-primary mb-3 m-2"
        @click="mode = 'login'"
      >
        Zaloguj sie
      </button>
      <button
        type="submit"
        class="btn btn-primary mb-3 m-2"
        @click="mode = 'registration'"
      >
        Rejestracja
      </button>
    </div>
  </div>
</template>
<script>
export default {
  name: "login",
  data() {
    return {
      mode: "login",
    };
  },
};
</script>
<style lang="scss" scoped>
.login {
  position: relative;
  padding: 4%;
  width: 100%;
  height: 100%;
  background-color: white;
  border-radius: 24px;
}
</style>
