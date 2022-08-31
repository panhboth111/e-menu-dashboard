<template>
  <div class="d-flex justify-center">
    <v-card>
      <v-container>
        <v-card-title>
          <v-btn icon class="mr-12" nuxt link to="/users"
            ><v-icon>mdi-arrow-left</v-icon></v-btn
          >
          Create User</v-card-title
        >
        <v-form>
          <v-text-field
            type="text"
            label="username"
            name="username"
            outlined
            dense
          ></v-text-field>
          <v-text-field
            type="text"
            label="fullname"
            name="name"
            outlined
            dense
          ></v-text-field>
          <v-text-field
            type="password"
            label="password"
            name="password"
            outlined
            dense
          ></v-text-field>
          <v-text-field
            type="password"
            label="Confirm password"
            name="password"
            outlined
            dense
          ></v-text-field>
          <v-select :items="roles" outlined label="Role"></v-select>
          <v-btn color="primary" block dark>SUBMIT</v-btn>
        </v-form>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    roles: ["Admin", "User"],
  }),
};
</script>

<style scoped>
.v-text-field {
  width: 400px;
}
</style>
