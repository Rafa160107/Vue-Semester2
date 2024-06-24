<script setup>
import modal_store from '../components/modal_store.vue'
import { useModalStatus } from '@/stores/modal_status'
const modal_status = useModalStatus();
const showModal=()=>{
  modal_status.setModalStatus(true)
}
</script>
<template>
    <div>
        <button @click="showModal" class="btn btn-success">Show Modal</button>
        <modal_store title="modal coba">ini isinya modal</modal_store>


    </div>
</template>
