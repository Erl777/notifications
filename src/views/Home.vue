<template>
  
  <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="cards-container">

   <card />

  </div>
  
</template>

<script>
// @ is an alias to /src
import card from '@/components/card.vue'

export default {
  name: 'Home',
  components: {
    card
  },
  data() {
    return {
      
    }
  }
}
</script>

<style>
  .cards-container{
    padding: 0 15px;
  }
  .card{
    position: relative;
    width: 300px;
    height: 300px;
    border: 1px solid;
    background-color: gold;
    border-radius: 4px 0 0 4px;
    padding: 0 5px 5px 5px;
  }
  
  .title{
    height: 12%;
    border-bottom: 1px solid;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .description{
    position: relative;
    width: 100%;
    height: 88%;
    padding-top: 10px;
    text-align: left;
  }
  .date{
    position: absolute;
    right: 0;
    bottom: 0;
  }
  .actions{
    position: absolute;
    right: -1px;
    top: -1px;
    width: 10%;
    height: calc(100% + 2px) ;
    background-color: green;
    transform: translateX(100%);
    border-radius: 0 4px 4px 0;
    border-top: 1px solid;
    border-right: 1px solid;
    border-bottom: 1px solid;
  }
  .actions span{
    min-height: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    background-color: rgba(0, 0, 0, 0.3);
  }
  .actions span:hover{
    cursor: pointer;
  }
  ul, ol {
    padding-left: 20px;
    margin: 0;
  }
  .description textarea{
    z-index: 2;
    position: absolute;
    border: 0;
    width: 100%;
    height: calc(100% - 10px);
    border-radius: 4px;
    outline: none;
    resize: none;
  }

</style>
