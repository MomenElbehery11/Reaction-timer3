<template>
    <p>Reaction Time - {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </template>
  
  <script>
  export default {
  props:['score'],
  data(){
      return {
          rank:null
      }
  },
  mounted(){
      if(this.score<650){
      this.rank="Ninja Fingers"
      }else if(this.score<1000){
      this.rank="Rapid Reflexes"
      }else{
      this.rank="Maybe better next time..."
      }
  }
  }
  </script>
  
  <style>
  .rank{
      font-size: 1.4em;
      color: #dbed1b;
      font-weight:bold;
  }
  </style>