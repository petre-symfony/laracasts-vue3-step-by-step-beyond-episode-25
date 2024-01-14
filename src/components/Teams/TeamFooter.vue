<script setup>
  import { useTeamStore } from "@/stores/TeamStores.js";

  let team = useTeamStore();
</script>

<template>
  <footer class="mt-12 bg-gray-100 py-4 text-center">
    <h5 class="font-semibold text-lg">{{ team.name }} - {{ team.spots }} Member Team</h5>

    <div id="hello">
      <h1>Hello Here</h1>
    </div>
  </footer>
</template>