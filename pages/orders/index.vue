<template>
  <div>
    <DataTable :headers="headers" :items="items" :to="'orders'" />
  </div>
</template>

<script>
import DataTable from "@/components/reusables/DataTable.vue";
export default {
  data: () => ({
    items: [
      {
        id: "1",
        table: "A4",
        time: "6:00 PM",
        status: "Pending",
        actions: "",
      },
      {
        id: "3",
        table: "C1",
        time: "6:15 PM",
        status: "Cooking",
        actions: "",
      },
      {
        id: "2",
        table: "B3",
        time: "6:13 PM",
        status: "Cooking",
        actions: "",
      },

      {
        id: "4",
        table: "A1",
        time: "7:35 PM",
        status: "Served",
        actions: "",
      },
    ],
    headers: [
      { text: "No.", value: "id" },
      { text: "Table", value: "table" },
      { text: "Time", value: "time" },
      { text: "Status", value: "status" },
      { text: "Actions", value: "actions" },
    ],
  }),
  components: {
    DataTable,
  },
};
</script>

<style></style>
