<script setup>
  defineProps({
    show: Boolean
  })
</script>

<template>
  <transition name="modal">
    <div v-if="show" class="modal-mask">
      <div class="modal-container">
        <slot></slot>

        <footer class="modal-footer">
          <slot name="footer">
            <button @click="$emit('close')">Close</button>
          </slot>
        </footer>
      </div>
    </div>
  </transition>
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
    border-radius: 7px;

    max-width: 500px;
  }
  .modal-footer {
    border-top: 1px solid #ddd;
    margin-top: 1rem;
    padding-top: 0.5rem;
    font-size: .8rem;
  }
  .modal-footer button {
    background: #ddd;
    padding: 0.25rem .75rem;
    border-radius: 20px;
  }
  .modal-footer button:hover {
    background: #c8c8cb;
  }
  .mudal-enter-active {
    /*@apply duration-300; */
    transition: opacity .3s;
  }
  .modal-enter-from {
    opacity: 0;
  }
  .modal-enter-to {
    opacity: 100;
  }
</style>