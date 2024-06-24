
<script setup>
import { useModalStatus } from '@/stores/modal_status'
import { defineProps } from 'vue'





const modal_status = useModalStatus()
const props = defineProps({
  title: String
})
</script>
<template>
     <div>
      <!-- Modal Content -->
      <div class="modal" tabindex="-1" role="dialog" :class="{ 'd-block': modal_status.getModalStatus }">
        <div class="modal-dialog" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title">{{ title }}</h5>
              <button type="button" class="btn-close" @click="modal_status.setModalStatus (false)"></button>
            </div>
            <div class="modal-body">
              <slot></slot>
            </div>
            <div class="modal-footer">
              <button type="button" class="btn btn-secondary" @click="modal_status.setModalStatus(false)">
                Close
              </button>
              <!-- <button type="button" class="btn btn-primary">Save changes</button> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  /* Add your modal button and modal content styles here */
  </style>