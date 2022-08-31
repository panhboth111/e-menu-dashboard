<template>
  <div><DataTable :headers="headers" :items="items" :to="'categories'" /></div>
</template>

<script>
import DataTable from "@/components/reusables/DataTable.vue";
export default {
  components: {
    DataTable,
  },
  data: () => ({
    items: [
      { id: "1", name: "Appetizer", status: "Enable", action: "" },
      { id: "2", name: "Seafood", status: "Enable", action: "" },
      { id: "3", name: "Asian", status: "Enable", action: "" },
      { id: "4", name: "European", status: "Enable", action: "" },
      { id: "5", name: "Fast Food", status: "Enable", action: "" },
    ],
    headers: [
      { text: "No.", value: "id" },
      { text: "Category Name", value: "name" },

      { text: "Status", value: "status" },
      { text: "Actions", value: "actions" },
    ],
  }),
};
</script>

<style></style>
