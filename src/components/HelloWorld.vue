<template>
    <div class="texto">
      <img class="imga" src="../../src/components/pic/webdes.png" alt="">
      <h1 class="typing-text" v-html="typedMessage"></h1>
      <p>{{ dot }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        message: "Welcome! I'm Prince, a web designer and developer.<br>Let's bring your vision to life with <br> beautiful and functional websites",
        typedMessage: ""
      };
    },
    mounted() {
      this.typeMessage();
    },
    methods: {
      typeMessage() {
        let index = 0;
        const typingInterval = setInterval(() => {
          this.typedMessage += this.message[index];
          index++;
          if (index === this.message.length) {
            clearInterval(typingInterval);
          }
        }, this.randomDelay()); // Use random delay for typing
      },
      randomDelay() {
        // Generate a random delay between 50ms and 150ms
        return Math.floor(Math.random() * 100) + 50;
      }
    }
  };
  </script>
  
  <style scoped>
  .typing-text {
    color: #FFD700;
    font-size: 20px;
    white-space: nowrap; /* Prevent text from wrapping */
    overflow: hidden; /* Hide overflow */
    direction: rtl; /* Set text direction to right-to-left */
    text-align: left; /* Align text to left */
    animation: typing-animation 3s steps(40, end);
    font-size: 15px;
  }
  
  @keyframes typing-animation {
    from {
      width: 0; /* Start with no width */
    }
  }
  
  .texto {
    margin: auto;
    margin-top: 70px;
    font-family: "Roboto Mono", monospace;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    max-width: 90%; /* Set maximum width */
  }
  
  .imga {
    width: 200px;
  }
  
  @media screen and (max-width: 768px) {
    .imga {
      width: 150px; /* Adjust image size for smaller screens */
    }
  }
  </style>
  