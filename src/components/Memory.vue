<script setup>
const tableauImg = ["/public/images/Paw-Patrol-Logo.png", "chase.png", ever]
function createTab(largeur, hauteur, tableauImg) {

for (let x = 0;x<hauteur;x++){
  for (let y = 0; y< largeur; y++){
    createCard(tableauImg[largeur+hauteur])
  }
}
}

function createCard(image) {
  document.createElement('img', image)
}
</script>

<template>
  <main>
    <h2>Memory game grid</h2>
    <ul>
      <li v-for="(image, imageIndex) in tableauImg" :key="imageIndex">
        <div>
        <img :src="image">
      </div>
      </li>
    </ul>
    
  </main>
</template>

<style scoped>


</style>
