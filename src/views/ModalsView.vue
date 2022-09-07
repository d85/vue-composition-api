<template>
  <div class="modals">
    <h1>Modals</h1>
    <div>
      <label>Show dark modals?</label>
      <input
        v-model="showDarkModals"
        type="checkbox"
      >
    </div>
    <button @click="showModal = true">Show modal</button>
    <component
      v-model="showModal"
      :is="showDarkModals ? ModalDark : Modal"
      title="My modal title (via prop)"
    >
      <template #title>My new title</template>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum a eligendi corporis eum beatae quis saepe qui,
        neque doloremque et ad error delectus blanditiis dolores rem? Qui harum debitis in.</p>
    </component>
  </div>
</template>

<script setup>
/*
  imports
*/

import { ref } from 'vue'
import Modal from '@/components/Modal.vue'
import ModalDark from '@/components/ModalDark.vue'

/*
  modals
*/

const showDarkModals = ref(false)
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