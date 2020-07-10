<template>
  <div class="about">

    <form action="">

      <label for="login"> Login</label>
      <input type="text" id="login">
      
      <label for="password"> Password</label>
      <input type="text" id="password">
      
    </form>

  </div>
</template>

<style scoped>
  form{
    max-width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 auto 
  }
  input{
    margin-bottom: 10px;
  }
</style>