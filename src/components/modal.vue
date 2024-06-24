
<template>
  <div>
    <!-- Modal Button -->
    <button type="button" class="btn btn-primary" @click="showModal = true">
      Open Modal
    </button>

    <!-- Modal Content -->
    <div class="modal" tabindex="-1" role="dialog" :class="{ 'd-block': showModal }">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">Modal title</h5>
            <button type="button" class="btn-close" @click="showModal = false"></button>
          </div>
          <div class="modal-body">
            <p>Modal content goes here...</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" @click="showModal = false">
              Close
            </button>
            <button type="button" class="btn btn-primary">Save changes</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ShowModal from '@/views/ShowModal.vue';
import { ref } from 'vue';

const showModal = ref(false);
</script>