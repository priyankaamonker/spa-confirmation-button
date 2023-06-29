<script>
import vueConfirmationButton from './components/vue-confirmation-button.vue';

export default {
  components: {
    vueConfirmationButton
  },
  data: () => ({
    customMessages: [
      'Delete',
      'Are you sure?',
      'Ok!'
    ],
    }
),
  methods: {
    deleteUser() {
      console.log("deleteUser");
    },
    resetButton() {
      this.$refs.confirmationButton.reset();
      console.log("resetButton");
     //this.$refs.resetButton.class = "test";
    },
  },
}
</script>
<template>
    <div>
        <vue-confirmation-button
          :messages="customMessages"
          ref="confirmationButton"
          v-on:confirmation-success="deleteUser()" 
          >
        </vue-confirmation-button>
        <button @click="resetButton()" ref="resetButton" class="reset_button">
            Reset
        </button>
    </div>
</template>
