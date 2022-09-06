<template>
  <div class="modals">
    <h1>Modals</h1>
    <button @click="showModal = true">Show modal</button>
    <Modal
      v-model="showModal"
      title="My modal title (via prop)"
    >
      <template #title>My new title</template>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum a eligendi corporis eum beatae quis saepe qui, neque doloremque et ad error delectus blanditiis dolores rem? Qui harum debitis in.</p>
    </Modal>
  </div>
</template>

<script setup>
/*
  imports
*/

import { ref } from 'vue'
import Modal from '@/components/Modal.vue'

/*
  modals
*/

const showModal = ref(false)

</script>

<!--
<script>
import Modal from '@/components/Modal.vue'

export default {
  components: {
    Modal
  }
}
</script>
-->