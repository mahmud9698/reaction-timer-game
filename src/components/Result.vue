<template>
    <p>Reaction Time: {{ score }} ms</p>
    <p class="rank" v-html="rank"></p>
  </template>
  
  <script>
  export default {
      props: ['score'],
      data() {
          return {
              rank : null
          }
      },
      mounted() {
          if (this.score <= 200) {
              this.rank = "You're Ninja!"
          } else if (this.score <= 400) {
              this.rank = "Almost Ninja!<br><br> Good Rapid reflexes!"
          } else {
              this.rank = "Similar to snail hehe ..."
          }   
      }
  }
  </script>
  
  <style>
      .rank {
          font-size: 1.4em;
          color: lightseagreen;
          font-weight: bold;
      }
  </style>
