<template>
  <div>
    <v-card>
      <v-container fluid class="pt-6">
        <v-row>
          <v-col cols="12" sm="12" md="3" lg="4">
            <v-text-field
              label="search"
              outlined
              dense
              v-model="search"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-data-table :headers="headers" :items="items">
          <template v-slot:item.actions="{ item }">
            <v-btn @click="handleNavigate(item)" icon
              ><v-icon size="20">mdi-eye</v-icon></v-btn
            >
          </template>
          <!-- <template v-slot:[`item.actions`]="{ item }">
            <v-btn nuxt link icon :to="`/${to}/${item.id}`"
              ><v-icon size="20">mdi-eye</v-icon></v-btn
            >
          </template> -->
        </v-data-table>
        <!-- <v-row class="px-2">
          <v-col cols="12" sm="12" md="3" lg="4">
            <v-text-field
              label="search"
              outlined
              dense
              v-model="search"
            ></v-text-field>
          </v-col>
          <v-spacer></v-spacer>
          <v-btn color="primary" dark nuxt link :to="`/${to}/create`"
            >Create</v-btn
          >
        </v-row>
        <v-data-table
          :headers="headers"
          :items="items"
          :items-per-page="5"
          class="elevation-0"
          :search="search"
        >
          <template v-slot:item.actions="{ item }">
            <v-btn nuxt link icon :to="`/${to}/${item.id}`"
              ><v-icon size="20">mdi-eye</v-icon></v-btn
            >
          </template>
        </v-data-table> -->
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    search: "",
  }),
  props: {
    headers: Array,
    items: Array,
    to: String,
  },
  methods: {
    handleNavigate(item) {
      this.$router.push(`/${this.to}/${item.id}`);
    },
  },
};
</script>

<style></style>
