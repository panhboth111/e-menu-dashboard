<template>
  <div class="d-flex justify-center">
    <v-card>
      <v-container>
        <v-card-title>
          Your Profile
          <v-btn icon class="ml-2" @click="edit = !edit"
            ><v-icon>mdi-pencil</v-icon></v-btn
          ></v-card-title
        >
        <v-form>
          <v-text-field
            type="text"
            label="username"
            name="username"
            v-model="user.username"
            outlined
            dense
            :readonly="!edit"
          ></v-text-field>
          <v-text-field
            type="text"
            label="fullname"
            name="name"
            v-model="user.fullname"
            outlined
            dense
            :readonly="!edit"
          ></v-text-field>
          <v-text-field
            type="password"
            label="password"
            name="password"
            v-model="user.password"
            outlined
            dense
            :readonly="!edit"
          ></v-text-field>
          <v-text-field
            type="password"
            label="Confirm password"
            name="password"
            outlined
            dense
            v-if="edit"
          ></v-text-field>

          <v-select :items="roles" outlined label="Role" readonly></v-select>
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
    edit: false,
    user: {
      fullname: "Neak Panhboth",
      username: "pboth69",
      password: "testingpassword",
    },
  }),
};
</script>

<style scoped>
.v-text-field {
  width: 400px;
}
</style>
