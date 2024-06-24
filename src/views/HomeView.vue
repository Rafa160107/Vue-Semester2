
<script setup>
// import TheWelcome from '../components/TheWelcome.vue'
// import NavItem from '@/components/NavItem.vue'
import { onMounted } from 'vue'
import modal_store from '../components/modal_store.vue'
import { useModalStatus } from '@/stores/modal_status'

const modal_status = useModalStatus()

onMounted(() => {
  // Ensure that modal is closed initially
  modal_status.setModalStatus(false)
})

const showModal = () => {
  modal_status.setModalStatus(true)
}
</script>

<template>
  <div>
    <button @click="showModal" class="btn btn-success">Show Modal</button>
    <modal_store title="Judul Modal">ini isinya modal!</modal_store>
  </div>
</template>