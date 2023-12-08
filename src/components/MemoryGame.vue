<script setup>

const tableauImg = ["marcus.png", "chase.png", "everest.png", "rocky.png", "zuma.png", "stella.png", "ruben.png","ryder.png"]
const imgBack = "backcard.png"
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

function flipCard(image) {
  image.classList.toggle('flipped');
  
}
</script>

<template>
  <main>
    
    <h2>Memory game grid</h2>
    <div class="list">
      <article v-for="(image, imageIndex) in tableauImg" :key="imageIndex" v-on:click="flipCard(image)">
        <img :src="'/images/'+image" :alt="image">
      </article>
    </div>
    
    
  </main>
</template>
<style scoped>
.list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  grid-gap: 10px;
  width: 100%;
  max-width: 510px;
}

article {
  height: 150px;
  background-color: #efefef;
  text-align: center;
  text-transform: capitalize;
  border-radius: 5px;
  cursor: pointer;
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2), 0 10px 10px rgba(0, 0, 0, 0.2);

  /* justify-content: center;
  align-content: center; */
  
}

h3 {
  margin: 0;
}

img {
  width: 120px;
  height: 120px;

}

img.flipped {
  transform: rotateY(180deg);
}
</style>
