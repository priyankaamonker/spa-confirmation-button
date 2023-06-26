<script setup>
import vueConfirmationButton from './components/vue-confirmation-button.vue';

const demo = {
  data: {
      customMessages: [
        'Delete User',
        'Are you sure?',
        'Ok!'
      ],
  },
  methods: {
    deleteUser() {
      alert("deleted");
    },
  },
  components: {
    'vue-confirmation-button': vueConfirmationButton,
  },
};
</script>
<template>
    <div class="confirmation__button">
        <vue-confirmation-button
          :messages="demo.customMessages"
          v-on:confirmation-success="demo.deleteUser()">
        </vue-confirmation-button>
    </div>
</template>
