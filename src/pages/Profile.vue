<!-- Profile Page -->
<script setup>
import useAuthUser from "@/composables/UseAuthUser";
const { user } = useAuthUser();
console.log(user.value);
</script>

<template>
  <div class="max-w-lg m-auto">
    <h1 class="text-3xl mb-5">Profile</h1>
    <div v-if="user">
      <div>Email: {{ user.email }}</div>
      <div>{{ user }}</div>
    </div>
  </div>
</template>
