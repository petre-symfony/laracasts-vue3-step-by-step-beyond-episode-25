<script setup>
  import TeamMembers from "@/components/Teams/TeamMembers.vue";
  import TeamHeader from "@/components/Teams/TeamHeader.vue";
  import TeamFooter from "@/components/Teams/TeamFooter.vue";
  import { useTeamStore } from "@/stores/TeamStores.js";
  import Modal from "@/components/Modal.vue";
  import {ref} from "vue";

  let team = useTeamStore();
  team.fill();

  let showModal = ref(false);
</script>

<template>
  <TeamHeader @add="showModal = true"/>

  <div class="place-self-center flex flex-col gap-y-3">
    <TeamMembers />

  </div>
  <TeamFooter />
  <Modal :show="showModal"/>
</template>
