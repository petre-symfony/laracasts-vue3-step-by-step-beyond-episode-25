<script setup>

</script>

<template>
  <div class="modal-mask">
    <div class="modal-container">
      <header>Header Text</header>

      <div>Main Text</div>

      <footer>footer</footer>
    </div>
  </div>
</template>

<style>
  .modal-mask {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, .6);
    display: grid;
    place-items: center;
  }
  .modal-container {
    background: white;
    padding: 1rem;
  }
</style>