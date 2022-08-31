<template>
  <div><DataTable :headers="headers" :items="items" :to="'menu'" /></div>
</template>

<script>
import DataTable from "@/components/reusables/DataTable.vue";
export default {
  components: {
    DataTable,
  },
  data: () => ({
    items: [
      { id: "1", name: "Fried Rice", status: "Enable", action: "" },
      { id: "2", name: "Crab Salad", status: "Enable", action: "" },
      { id: "3", name: "Club Sandwich", status: "Enable", action: "" },
      { id: "4", name: "Katsu bowl", status: "Enable", action: "" },
      { id: "5", name: "French Fries", status: "Enable", action: "" },
    ],
    headers: [
      { text: "No.", value: "id" },
      { text: "Food Name", value: "name" },

      { text: "Status", value: "status" },
      { text: "Actions", value: "actions" },
    ],
  }),
};
</script>

<style></style>
