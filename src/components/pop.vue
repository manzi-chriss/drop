<template>
    <div>
      <button @click="togglePopup">Open Popup</button>
      <div v-if="showPopup" class="popup">
        <div class="popup-content">
          <button @click="closePopup">Close Popup</button>
          <!-- Your popup content goes here -->
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showPopup: false
      };
    },
    methods: {
      togglePopup() {
        this.showPopup = !this.showPopup;
      },
      closePopup() {
        this.showPopup = false;
      }
    }
  };
  </script>
  
  <style>
  .popup {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 20px;
    border: 1px solid #ccc;
  }
  
  .popup-content {
    text-align: center;
  }
  
  /* Style as needed */
  </style>
  