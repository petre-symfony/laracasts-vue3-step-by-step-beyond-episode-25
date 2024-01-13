<script setup>
  import TeamMembers from "@/components/Teams/TeamMembers.vue";
  import TeamHeader from "@/components/Teams/TeamHeader.vue";
  import team from "@/team.json";
</script>

<template>
  <TeamHeader :team="team" />

  <div class="place-self-center flex flex-col gap-y-3">
    <TeamMembers :team="team" />
    <p class="text-right text-gray-600 italic" v-show="team.members.length === team.spots">
      There are no remaining team spots. Upgrade to add more.
    </p>
  </div>
  <footer class="mt-12 bg-gray-100 py-4 text-center">
    <h5 class="font-semibold text-lg">{{ team.name }} - {{ team.spots }} Member Team</h5>
  </footer>
</template>
