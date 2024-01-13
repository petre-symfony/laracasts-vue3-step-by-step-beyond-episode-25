<script setup>
  import TeamMembers from "@/components/Teams/TeamMembers.vue";
  import TeamHeader from "@/components/Teams/TeamHeader.vue";
  import TeamFooter from "@/components/Teams/TeamFooter.vue";
  import { useTeamStore } from "@/stores/TeamStores.js";


  let team = useTeamStore();
  team.fill();

  setTimeout(() => {
    team.spots = 10
  }, 2000);
</script>

<template>
  <TeamHeader />

  <div class="place-self-center flex flex-col gap-y-3">
    <TeamMembers />

  </div>
  <TeamFooter />
</template>
