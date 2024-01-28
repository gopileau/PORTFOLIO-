<template>
    <div>
      <!-- Modale 1 -->
      <div class="bloc-modal" v-if="revele && !reveleModale2 && !reveleModale3">
        <div class="overlay" v-on:click="toggleModale"></div>
        <div class="modale card">
            <a href="https://github.com/gopileau/cv" alt="" target="_blank">
            <p>voir PROJET</p></a>
            <p>date de réalisation:28/11/2023</p>
          <div v-on:click="toggleModale" class="btn-modale btn btn-danger">X</div>
          <img src="..//assets/h.png" alt="" width="200px" height="200px">
          <img src="..//assets/t.png" alt="" width="200px" height="200px">
        </div>
      </div>
  
      <!-- Modale 2 -->
      <div class="bloc-modal" v-if="reveleModale2">
        <div class="overlay" v-on:click="toggleModale2"></div>
        <div class="modale card">
          <div v-on:click="toggleModale2" class="btn-modale2 btn btn-danger">X</div>
          <a href="https://github.com/gopileau/devoir-" target="_blank">
            <p>voir PROJET</p></a>
            <p>date de réalisation:12/01/2024</p>
          <img src="..//assets/ja.png" alt="" width="200px" height="200px">
          <img src="..//assets/comment.png" alt="" width="200px" height="200px">
        </div>
        </div>
      </div>

      <!--Modale 3 -->
      <div class="bloc-modal" v-if="reveleModale3">
        <div class="overlay" v-on:click="toggleModale3"></div>
        <div class="modale card">
          <div v-on:click="toggleModale3" class="btn-modale3 btn btn-danger">X</div>
          <a href="https://drive.google.com/file/d/1q4Dbm2KTjMoryzHEKBBqjz-o742OWoO0/view?usp=drive_link" target="_blank">
            <p>voir PROJET</p></a>
            <p>date de réalisation:16/12/2023</p>
          <img src="..//assets/cahier.png" alt="" width="200px" height="200px">
          <img src="..//assets/ca.png" alt="" width="200px" height="200px">
        </div>
      </div>
  </template>
  
  <script>
  export default {
    name: 'ModalContent',
    props: ['revele','reveleModale2','reveleModale3','toggleModale', 'toggleModale2', 'toggleModale3']
  };
  </script>
  
  

<style scoped>
.bloc-modal{
    position:fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}
.overlay {
    position:fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
}
.modale{
    background: #000058;
    color:#fff;
    padding: 50px;
    position: fixed;
    top: 20%;
}
.btn-modale{
    background: #bababa;
    width: 15px;
    position: absolute;
    top: 10px;
    right: 10px;
    cursor:pointer;
 }
 .btn-modale2{
    background: #bababa;
    width: 15px;
    position: absolute;
    top: 10px;
    right: 10px;
    cursor:pointer;
 }
 .btn-modale3{
    background: #bababa;
    width: 15px;
    position: absolute;
    top: 10px;
    right: 10px;
    cursor:pointer;
 }
img{
    margin-right: 10px;
}
p{
    color:#fff;
}

</style>