<template>
  <div><DataTable :headers="headers" :items="items" :to="'users'" /></div>
</template>

<script>
import DataTable from "@/components/reusables/DataTable.vue";
export default {
  components: {
    DataTable,
  },
  data: () => ({
    items: [
      {
        id: "1",
        name: "Neak Panhboth",
        email: "panhboth14@gmail.com",
        role: "Super Admin",
        status: "Enable",
        action: "",
      },
      {
        id: "2",
        name: "John Cena",
        email: "johncena@gmail.com",
        role: "Admin",
        status: "Enable",
        action: "",
      },
      {
        id: "3",
        name: "John Doe",
        email: "johndoe@gmail.com",
        role: "User",
        status: "Enable",
        action: "",
      },
    ],
    headers: [
      { text: "No.", value: "id" },
      { text: "Fullname", value: "name" },
      { text: "Email", value: "email" },
      { text: "Role", value: "role" },
      { text: "Status", value: "status" },
      { text: "Actions", value: "actions" },
    ],
  }),
};
</script>

<style></style>
