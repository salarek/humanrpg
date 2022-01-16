<template>
  <div class="login" :class="'switch-' + mode">
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

    <div v-if="mode == 'registration'">
      <p>Rejestracja</p>
      <div class="mb-3 row">
        <label for="staticName" class="col-sm-2 col-form-label">Nazwa</label>
        <div class="col-sm-10">
          <input type="text" class="form-control" id="staticName" />
        </div>
      </div>
      <div class="mb-3 row">
        <label for="staticEmail" class="col-sm-2 col-form-label">Email</label>
        <div class="col-sm-10">
          <input type="text" class="form-control" id="staticEmail" />
        </div>
      </div>

      <div class="mb-3 row">
        <label for="inputPassword" class="col-sm-2 col-form-label"
          >Password</label
        >
        <div class="col-sm-9">
          <input :type="passwordMode" class="form-control" id="inputPassword" />
        </div>
        <div class="col-sm-1">
          <button
            type="button"
            class="btn btn-danger"
            @click="changePasswordMode(passwordMode)"
          >
            <svg
              v-if="passwordMode == 'password'"
              style="width: 24px; height: 24px"
              viewBox="0 0 24 24"
            >
              <path
                fill="currentColor"
                d="M12,9A3,3 0 0,1 15,12A3,3 0 0,1 12,15A3,3 0 0,1 9,12A3,3 0 0,1 12,9M12,4.5C17,4.5 21.27,7.61 23,12C21.27,16.39 17,19.5 12,19.5C7,19.5 2.73,16.39 1,12C2.73,7.61 7,4.5 12,4.5M3.18,12C4.83,15.36 8.24,17.5 12,17.5C15.76,17.5 19.17,15.36 20.82,12C19.17,8.64 15.76,6.5 12,6.5C8.24,6.5 4.83,8.64 3.18,12Z"
              />
            </svg>
            <svg
              v-if="passwordMode == 'text'"
              style="width: 24px; height: 24px"
              viewBox="0 0 24 24"
            >
              <path
                fill="currentColor"
                d="M2,5.27L3.28,4L20,20.72L18.73,22L15.65,18.92C14.5,19.3 13.28,19.5 12,19.5C7,19.5 2.73,16.39 1,12C1.69,10.24 2.79,8.69 4.19,7.46L2,5.27M12,9A3,3 0 0,1 15,12C15,12.35 14.94,12.69 14.83,13L11,9.17C11.31,9.06 11.65,9 12,9M12,4.5C17,4.5 21.27,7.61 23,12C22.18,14.08 20.79,15.88 19,17.19L17.58,15.76C18.94,14.82 20.06,13.54 20.82,12C19.17,8.64 15.76,6.5 12,6.5C10.91,6.5 9.84,6.68 8.84,7L7.3,5.47C8.74,4.85 10.33,4.5 12,4.5M3.18,12C4.83,15.36 8.24,17.5 12,17.5C12.69,17.5 13.37,17.43 14,17.29L11.72,15C10.29,14.85 9.15,13.71 9,12.28L5.6,8.87C4.61,9.72 3.78,10.78 3.18,12Z"
              />
            </svg>
          </button>
        </div>
      </div>
      <div class="col-auto">
        <button
          type="submit"
          class="btn btn-primary mb-3 m-2"
          @click="mode = 'login'"
        >
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M19,7V11H5.83L9.41,7.41L8,6L2,12L8,18L9.41,16.58L5.83,13H21V7H19Z"
            />
          </svg>
        </button>
        <button
          type="submit"
          class="btn btn-primary mb-3 m-2"
          @click="mode = 'registration'"
        >
          Zarejestruj konto
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "login",
  data() {
    return {
      mode: "login",
      passwordMode: "password",
    };
  },
  methods: {
    changePasswordMode(mode) {
      switch (mode) {
        case "password":
          this.passwordMode = "text";
          break;
        case "text":
          this.passwordMode = "password";
          break;
      }
    },
  },
};
</script>
<style lang="scss" scoped>
@import "@/scss/variables";
.login {
  contain: content;
  position: relative;
  padding: 5%;
  color: white;

  width: 100%;
  background-color: $secondary;

  transition: all 0.5s ease;
}

.switch-registration {
  transform: scale(1);
  width: 80%;
}

.login:before {
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
.login:after {
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
