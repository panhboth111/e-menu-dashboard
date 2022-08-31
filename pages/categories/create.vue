<template>
  <div class="d-flex justify-center">
    <v-card>
      <v-container>
        <v-card-title>
          <v-btn icon class="mr-12" nuxt link to="/users"
            ><v-icon>mdi-arrow-left</v-icon></v-btn
          >
          Create Category</v-card-title
        >
        <v-form>
          <v-text-field
            type="text"
            label="Category Name"
            name="category name"
            outlined
            dense
          ></v-text-field>
          <v-select :items="statuses" outlined label="Status"></v-select>

          <v-btn color="primary" block dark>SUBMIT</v-btn>
        </v-form>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    statuses: ["Active", "Disabled"],
  }),
};
</script>

<style scoped>
.v-text-field {
  width: 400px;
}
</style>
