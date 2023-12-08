<script setup>
import Memory from './components/MemoryGame.vue';
</script>

<template>
    <header>
      <div class="header">
        <img src="/images/Paw-Patrol-Logo.png" alt="Vue logo" class="logo"/>
        <h1>Your Memory Game</h1>
        <p>Enjoy playing the memory game!</p>
        
      </div>
    </header>
    <main>
      <Memory />
    </main>
    
</template>

<style scoped>
  
/* styles.css (or your preferred stylesheet) */

html,body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  border:none;
}

.header {
  background-color: #3498db;
  color: #fff;
  padding: 20px;
  text-align: center;
  width: 100%; /* Make the header take up the full width */
  display: grid;
  grid-template-columns: 1fr 2fr;
}

.header h1 {
  margin: 0;
  font-size: 2em;
}

.header p {
  margin-top: 5px;
  font-size: 1.2em;
}
.logo {
  height: 10em;
  margin-right: 0.5em;
  vertical-align: middle;
}


</style>
