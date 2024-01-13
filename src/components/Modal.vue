<script setup>
  defineProps({
    show: Boolean
  })
</script>

<template>
  <div v-if="show" class="modal-mask">
    <div class="modal-container">
      <header>
        <slot name="header">default header</slot>
      </header>

      <div>default body</div>

      <footer>
        <slot name="footer">
          <button @click="$emit('close')">Default Close</button>
        </slot>
      </footer>
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
    width: 80vw;

    max-width: 500px;
  }
</style>