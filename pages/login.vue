<template>
  <div class="">
    <v-row class="construct-page">
      <v-col cols="12" sm="12" md="4" lg="4" xl="4" class="gray left">
        <div class="form">
          <v-form>
            <div
              class="text-center headline font-weight-bold mb-6 primary--text"
            >
              Welcome back
            </div>
            <v-text-field
              label="username"
              type="text"
              name="username"
              outlined
              dense
            ></v-text-field>
            <v-text-field
              label="password"
              type="password"
              name="password"
              outlined
              dense
            ></v-text-field>
            <v-btn block color="primary" nuxt link to="/" dark>LOGIN</v-btn>
          </v-form>
        </div>
      </v-col>
      <v-col cols="12" sm="12" md="8" lg="8" xl="8" class="right"> </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  layout: "login",
};
</script>

<style>
.construct-page {
  height: 100vh;
}
.form {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
.right {
  background: url("/pvk.jpeg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
