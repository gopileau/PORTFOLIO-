<template>
  <div>
  <!--MENU-->
  <div class="header-container">
    <header>
      <div class="logo">
        <a href="#">
        <img src="..//assets/tortu.png" alt="" height="40" width="40">
        </a>
      </div>
      <nav id="nav">
        <ul>
            <li :class="{ 'actif': itemMenuActif === 'surmoi' }">
              <a @click="definirItemMenuActif('surmoi')" href="#surmoi">À PROPOS DE MOI</a>
            </li>
            <li :class="{ 'actif': itemMenuActif === 'skills' }">
              <a @click="definirItemMenuActif('skills')" href="#skills">COMPETENCES</a>
            </li>
            <li :class="{ 'actif': itemMenuActif === 'cv' }">
              <a @click="definirItemMenuActif('cv')" href="#cv">CV</a>
            </li>
            <li :class="{ 'actif': itemMenuActif === 'contact' }">
              <a @click="definirItemMenuActif('contact')" href="#contact">CONTACT</a>
            </li>
          </ul>
      </nav>
        <img src="..//assets/menu.png" class="img0" alt="" height="42" width="42">
    </header>
  </div>
  <!--ACCUEILLE-->
  <section id="accueille" class="accueille">
    <div>
    <div class="contenu-banner">
      <div class="contenedor-img">
        <img src="..//assets/profilepic.png" alt="">
      </div>
      <h1>Laura Gonzalez</h1>
      <h2>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum quibusdam
         vitae vero tenetur molestias iusto. Provident, animi amet?</h2>
      <div class="contenu-section">
      <h2>Mes créations</h2>
      <div class="galerie">
        <div class="proyect">
        <img src="..//assets/cv1.png" alt="" width="120px" height="120px">
        <ModalContent :revele="revele" :toggleModale="toggleModale"
                  :reveleModale2="reveleModale2" :toggleModale2="toggleModale2"
                  :reveleModale3="reveleModale3" :toggleModale3="toggleModale3" />
      <div v-on:click="toggleModale" class="btn btn-success">
        <div class="overlay">
          <h3>HTML&CSS</h3>
          <p>CV</p>
        </div> 
      </div>
    </div>
      <div class="proyect">
        <ModalContent :reveleModale2="reveleModale2" :toggleModale2="toggleModale2">
        </ModalContent>
      <div v-on:click="toggleModale2" class="btn btn-success">
        <img src="..//assets/comment.png" alt="" width="120px" height="120px">
        <div class="overlay">
          <h3>JAVASCRIPT</h3>
          <p>Espace Commentaire</p>
        </div> 
      </div>
      </div>
      <div class="proyect">
        <ModalContent :reveleModale3="reveleModale3" :toggleModale3="toggleModale3">
        </ModalContent>
      <div v-on:click="toggleModale3" class="btn btn-success">
        <img src="..//assets/cahier.png" alt="" width="120px" height="120px">
        <div class="overlay">
          <h3>PDF</h3>
          <p>Cahier des charges</p>
        </div> 
      </div>
    </div>
    </div>
    </div>
    </div>
    <footer>
    <FooterComponent/>
    </footer>
    <router-view />
    </div>
  </section>
  <!--À PROPOS DE MOI-->
  <section id="surmoi" class="surmoi">
    <div>
    <div class="contenu-section">
      <h2>À propos de moi</h2>
      <p><span>Bonjour, Je suis Laura Gonzalez</span>Lorem ipsum dolor sit amet consectetur adipisicing elit.
         Ab ex aspernatur nihil consectetur placeat mollitia doloremque, odit iste eveniet eius incidunt tenetur? 
         Dolorum distinctio sint unde. Ex accusantium fugiat ea.</p>
    </div>
    <div class="fila">
      <!--COORDONNÉES-->
      <div class="col">
        <h3>Coordonnèes</h3>
        <ul>
          <li>
            <strong>date de naisssance</strong>
            19/11/1999
          </li>
          <li>
            <strong>Portable</strong>
            2244-33-33345
          </li>
          <li>
            <strong>Email</strong>
            vanessagonza@gmail
          </li>
          <li>
            <strong>website</strong>
            www.exemple.com
          </li>
          <li>
            <strong>étudiante</strong>
            developpeur web/langues etrangeres
          </li>
          <li>
            <strong>adress</strong>
            94 rue courcelles,france 
          </li>
        </ul>
        </div>
        <!--Centres d'interet-->
        <div class="col">
          <h3>Centre d'intérêt</h3>
          <div class="contenedor-intereses">
            <div class="interes">
              <img src="..//assets/langues.png" alt="" height="42" width="42">
              <span>Langues</span>
            </div>
            <div class="interes">
              <img src="..//assets/cam.png" alt="" height="42" width="42">
              <span>Photographie</span>
            </div>
            <div class="interes">
              <img src="..//assets/music.png" alt="" height="42" width="42">
              <span>Musique</span>
            </div>
            <div class="interes">
              <img src="..//assets/vol.png" alt="" height="42" width="42">
              <span>Voyages</span>
            </div>
            <div class="interes">
              <img src="..//assets/sport.png" alt="" height="42" width="42">
              <span>Sports</span>
            </div>
          </div>
        </div>
    </div>
    <button>
        Telecharger CV <img src="..//assets/telecharger.png" alt="" height="42" width="42">
        <span class="overlay"></span>
      </button>
      <footer>
    <FooterComponent />
    </footer>
    </div>
  </section>
  <!--COMPETENCES-->
  <section class="skills" id="skills">
    <div>
    <div class="contenu-section">
      <h2>Compétences</h2>
      <div class="fila">
        <!--Technical Skill-->
        <div class="col">
          <h3>Compétences technologiques</h3>
          <div class="skill">
            <span>Javascript</span>
            <div class="barra-skill">
              <div class="progrès javascript">
                <span>75%</span>
              </div>
            </div>
          </div>
          <div class="skill">
            <span>HTML & CSS</span>
            <div class="barra-skill">
              <div class="progrès htmlcss">
                <span>89%</span>
              </div>
            </div>
          </div>
        </div>
        <div class="col">
          <h3>Compétences professionnelles</h3>
          <div class="skill">
            <span>Communication</span>
            <div class="barra-skill">
              <div class="progrès comunication">
                <span>80%</span>
              </div>
            </div>
          </div>
          <div class="skill">
            <span>Travail en groupe</span>
            <div class="barra-skill">
              <div class="progrès travail">
                <span>89%</span>
              </div>
            </div>
          </div>
          <div class="skill">
            <span>Creativité</span>
            <div class="barra-skill">
              <div class="progrès creativité">
                <span>90%</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer>
    <FooterComponent />
    </footer>
    </div>
  </section>
  <!--CV-->
  <section id="cv" class="cv">
    <div>
    <div class="contenu-section">
      <h2>CV</h2>
      <div class="fila">
        <div class="col gauche">
          <h3>Études</h3>
          <div class="item gau">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus,
               ab tempore distinctio excepturi amet blanditiis! Labore voluptatibus tempora voluptates facilis.</p>
               <div class="conectori">
                <div class="circuloi"></div>
               </div>
          </div>
          <div class="item gau">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus,
               ab tempore distinctio excepturi amet blanditiis! Labore voluptatibus tempora voluptates facilis.</p>
               <div class="conectori">
                <div class="circuloi"></div>
               </div>
          </div>
          <div class="item gau">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus.</p>
               <div class="conectori">
                <div class="circuloi"></div>
               </div>
          </div>
        </div>
        <div class="col droite">
          <h3>Éxperience professionnelle</h3>
          <div class="item dro">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus,
               ab tempore distinctio excepturi amet blanditiis! Labore voluptatibus tempora voluptates facilis.</p>
               <div class="conectord">
                <div class="circulod"></div>
               </div>
          </div>
          <div class="item dro">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus,
               ab tempore distinctio excepturi amet blanditiis! Labore voluptatibus tempora voluptates facilis.</p>
               <div class="conectord">
                <div class="circulod"></div>
               </div>
          </div>
          <div class="item dro">
            <h4>Lincence Langues Étrangères Appliquées</h4>
            <span class="maison">Université de Reims</span>
            <span class="date">2021-2022</span>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque dolore voluptatibus.</p>
               <div class="conectord">
                <div class="circulod"></div>
               </div>
          </div>
        </div>
      </div>
    </div>
    <footer>
    <FooterComponent />
    </footer>
    </div>
  </section>
  <!--CONTACT-->
  <section id="contact" class="contact">
    <div>
    <div class="contenu-section">
      <h2>CONTACT</h2>
      <div class="fila">
        <!--Formulaire-->
        <div class="col">
          <input type="text" placeholder="Prenom">
          <input type="text" placeholder="Telephone">
          <input type="text" placeholder="addresse mail">
          <input type="text" placeholder="sujet">
          <textarea name="" id="" cold="30" rows="10" placeholder="Mesaje"></textarea>
          <button>
            Envoyer message <img src="..//assets/fly.png"  alt="" width="10px" height="10px">
            <span class="overlay"></span>
          </button>
        </div>
        <!--Carte-->
        <div class="col">
          <img src="..//assets/google.png" class="img1" alt="">
          <div class="info">
            <ul>
              <li>
                <img src="..//assets/loc.png"  class="img2" alt="" width="20px" height="20px">
                        Reims, 51100, france 
              </li>
              <li>
                <img src="..//assets/tel.png"  class="img2" alt="" width="20px" height="20px">
              Telephone: 9210-372408493
              </li>
              <li>
                <img src="..//assets/correo.png" class="img2" alt="" width="20px" height="20px">
                E-mail:        peto@cara.com
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <footer>
    <FooterComponent />
    </footer>
    </div>
  </section>
  </div>
</template>

// MainCard.vue
<script>
import ModalContent from '@/components/ModalContent.vue';
import FooterComponent from '@/components/Footer.vue';

// ...

export default {
  name: 'MainCard',
  data() {
    return {
      revele: false,
      reveleModale2: false,
      reveleModale3: false,
      itemMenuActif: 'surmoi', // Ajoutez cet état s'il n'est pas déjà défini
    };
  },
  components: {
    ModalContent,
    FooterComponent,
  },
  methods: {
    toggleModale() {
      this.revele = !this.revele;
    },
    toggleModale2() {
      this.reveleModale2 = !this.reveleModale2;
    },
    toggleModale3() {
      this.reveleModale3 = !this.reveleModale3;
    },
    definirItemMenuActif(item) {
      this.itemMenuActif = item;
    },
  },
};

</script>





<style scoped>
template{
    scroll-behavior: smooth;
}
.header-container{
  background-color: rgb(0,0,128,0.7);
  position: fixed;
  width: 100%;
  top:0;
  left: 0;
  z-index:99;
}
.header-container header{
  max-width: 1100px;
  margin:auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
}
.header-container header ul{
  display: flex;
  list-style: none;
}
.header-container header nav ul li a {
  text-align: none;
  color: #babab8;
  margin: 0 15px;
  transition: .5s;
  text-decoration: none;
}
.header-container header nav ul li a:hover{
  color: #000053;
}
img.img0 {
  padding: 5px 10px;
  border-radius: 50%;
  cursor: pointer;
  display: inline-block; 
}
.accueille{
  background-image: url(..//assets/fondo.png);
  color:#fff;
  background-size: cover;
  position: relative;
  height: 100vh;
  overflow: hidden;
  align-items: center;
  display:flex;
  justify-content: center;
  flex:1;
  padding: 80px;
}
.accueille .contenu-banner{
  position: relative;
  bottom: 0;
  padding: 20px;
  background-color: rgb(0,0,128,0.7);
  width: 50%;
  margin: auto;
  text-align: center;
  font-size: 10px;
  border-radius: 40px;
  transition:left 0.5s ease;
}
.accueille .contenu-banner img{
   margin-top: 40px;
   border:3px solid #000053;
   display: block;
   width: 20%;
   margin:auto;
}
.accueille .contenu-banner h1{
  margin-top: 40px;
  font-size: 42px;
  font-family: 'Righteous';
  color:#000053;
}
.accueille .contenu-banner h2{
  font-size: 15px;
  font-weight: normal;
}
.accueille .contenu-section h2{
  font-size: 30px;
  font-family: 'Righteous';
  color:#000053;
}
.galerie{
  display:flex;
justify-content: space-between;
}
.accueille .galerie .proyect {
  position:relative;
  max-width: 340px;
  height: fit-content;
  margin:10px;
  cursor:pointer;
}
.accueille .galerie .proyect img{
  width: 100%;
  display:block;
}
.accueille .galerie .proyect .overlay{
  position: absolute;
  top: 0;
  width: 110%;
  height: 100%;
  text-align: center;
  background:rgb(0,0,128,0.7);
  display:flex;
  flex-direction: column;
  justify-content: center;
  transition: 1s;
  font-size: 10px;
  color:#fff;
  letter-spacing: 3px;
  opacity: 0;
}
.accueille .galerie .proyect .overlay h3{
  margin-bottom: 20px;
  transition: 1s;
}
.accueille .galerie .proyect .overlay:hover{
  opacity: 1;
}
.accueille .contenu-banner .galerie img:hover{
  background-color: #000053;
}
.surmoi{
  background-color: #babab8;
  color: #000053;
  padding: 50px 20px;
}
.surmoi .contenu-section{
  max-width: 1100px;
  margin: auto;
}
.surmoi h2{
  font-size: 48px;
  font-family: 'Righteous';
  text-align: center;
  padding: 20px 0;
}
.surmoi .contenu-section p{
  font:18px;
  line-height: 22px;
  margin-bottom: 20px;
  text-align: left;
}
.surmoi .contenu-section p span{
  color:#000053;
  font-weight: bold;
}
.surmoi .fila{
  display: flex;
}
.surmoi .fila .col{
  width: 50%;
}
.surmoi .fila .col h3{
  font-size: 28px;
  font-family: 'Righteous';
  margin-bottom:25px;
}
.surmoi .fila .col ul{
  list-style: none;
}
.surmoi .fila .col ul li{
  margin:12px 0;
  text-align: left;
}
.surmoi .fila .col ul li strong{
  display: inline-block;
  color:#fff;
  width: 130px;
}
.surmoi .fila .col .contenedor-intereses{
  display:flex;
  flex-wrap: wrap;
}
.surmoi .fila .col .contenedor-intereses .interes {
  width: 100px;
  height:100px;
  background-color: rgb(0,0,128,0.7);
  color:#fff;
  margin: 0 15px 15px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transition: .3s;
}
.surmoi .fila .col .contenedor-intereses .interes:hover{
  background-color: #fff;
  color:#000053;
}
.surmoi .fila .col .contenedor-intereses .interes a{
  font-size: 30px;
  margin-bottom: 10px;
}
.surmoi button{
  cursor: pointer;
  background-color: transparent;
  border:2px solid #fff;
  width: fit-content;
  display: block;
  margin: 20px auto;
  padding: 10px 22px;
  font-size: 16px;
  color: #fff;
  position: relative;
  z-index:10;
}
.surmoi button .overlay{
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background-color: #000053;
  z-index: -1;
  transition: 1s;
}
.surmoi button:hover .overlay{
  width: 100%;
}
/*SCTION S K I L L S*/
.skills{
  background-color: #e5e5e1;
  color: #000053;
  padding: 50px 20px;
}
.skills .contenu-section{
  max-width: 1100px;
  margin: auto;
}
.skills h2{
  font-size: 48px;
  font-family: 'Righteous';
  text-align: center;
  padding: 20px 0;
}
.skills .fila{
  display: flex;
}
.skills .fila .col{
  width: 50%;
  padding: 0 20px;
}
.skills .fila .col h3{
  font-size: 28px;
  font-family: 'Righteous';
  margin-bottom:25px;
}
.skills .skill > span{
  font-weight: bold;
  display: block;
  margin-bottom: 10px;
  color:#000053;
}
.skills .skill .barra-skill{
  height: 8px;
  width: 80%;
  background-color: #babab8;
  position: relative;
  margin-bottom: 30px;
}
.skills .skill .progrès{
  background-color: #000053;
  position: absolute;
  top: 0;
  left: 0;
  height: 8px;
}
.skills .skill .barra-skill span{
  position:absolute;
  height: 40px;
  width: 40px;
  background-color: #000053;
  color:#fff;
  border-radius: 50px;
  line-height: 40px;
  text-align: center;
  top: -17px;
  right: -15px;
  font-size: 14px;
}
.skills .skill .javascript{
  width: 0%;
  animation: 2s javascript forwards;
}
@keyframes javascript {
  0%{width: 0%;}
  100%{width: 75%;}
}
.skills .skill .htmlcss{
  width: 0%;
  animation: 2s htmlcss forwards;
}
@keyframes htmlcss {
  0%{width: 0%;}
  100%{width: 89%;}
}
.skills .skill .comunication{
  width: 0%;
  animation: 2s comunication forwards;
}
@keyframes comunication {
  0%{width: 0%;}
  100%{width: 80%;}
}
.skills .skill .travail{
  width: 0%;
  animation: 2s travail forwards;
}
@keyframes travail {
  0%{width: 0%;}
  100%{width: 89%;}
}
.skills .skill .creativité{
  width: 0%;
  animation: 2s creativité forwards;
}
@keyframes creativité {
  0%{width: 0%;}
  100%{width: 90%;}
}
/*SECTION CV*/
.cv{
  background-color: #babab8;
  color: #000053;
  padding: 50px 20px;
}
.cv .contenu-section{
  max-width: 1100px;
  margin: auto;
}
.cv h2{
  font-size: 48px;
  font-family: 'Righteous';
  text-align: center;
  padding: 20px 0;
}
.cv .fila{
  display: flex;
  justify-content: space-between;
}
.cv .fila .col{
  width: 49%;
  padding: 0 20px;
}
.cv .fila .col h3{
  font-size: 28px;
  font-family: 'Righteous';
  margin-bottom:25px;
}
.cv .fila .gauche{
  border-right: 2px solid #000053;
}
.cv .fila .droite{
  border-left: 2px solid #000053;
}
.cv .fila .item{
  padding: 25px;
  margin-bottom: 30px;
  background-color: #e5e5e1;
  position: relative;
}
.cv .fila .item h4{
  font-size: 20px;
  margin-bottom: 10px;
}
.cv .fila .item .maison{
  color:#77b5fe;
  font-size: 22px;
  font-weight: bold;
  display: block;
}
.cv .fila .item .date{
  display: block;
  color: #fff;
  margin-bottom: 10px;
}
.cv .fila .item p{
  line-height: 24px;
}
.cv .fila .gau{
  border-right: 2px solid #fff;
  margin-right: 20px;
}
.cv .fila .dro{
  border-left: 2px solid #fff;
  margin-left: 20px;
}
.cv .fila .item .conectori{
  height: 2px;
  background-color: #000053;
  width: 47px;
  position:absolute;
  top: 50%;
  right: -47px;
  z-index: 5;
}
.cv .fila .item .conectori .circuloi{
  display: block;
  height: 10px;
  width: 10px;
  border-radius:50%;
  background-color: #000053;
  float: right;
  position:relative;
  bottom: 4px;
}
.cv .fila .item .conectord{
  height: 2px;
  background-color: #000053;
  width: 47px;
  position:absolute;
  top: 50%;
  left: -47px;
  z-index: 5;
}
.cv .fila .item .conectori .circulod{
  display: block;
  height: 10px;
  width: 10px;
  border-radius:50%;
  background-color: #000053;
  float: left;
  position:relative;
  bottom: 4px;
}
.contact{
  background-color: #e5e5e5;
  color: #000053;
  padding: 50px 0;
}
.contact .contenu-section{
  max-width: 1100px;
  margin: auto;
}
.contact h2 {
  font-size: 48px;
  font-family: 'Righteous';
  text-align: center;
  padding: 10px 0;
}
.contact .fila {
  display: flex;
  justify-content: space-between;
}
.contact .col{
  width: 40%;
  padding: 20px;
  position: relative;
}
.contact .col input, .contact .col textarea{
  display: block;
  width: 100%;
  padding: 18px;
  border: none;
  margin-bottom: 20px;
  background-color: #000053;
  color:#fff;
  font-size: 18px;
}
.contact button{
  cursor: pointer;
  background-color: transparent;
  border:2px solid #000053;
  width: fit-content;
  display: block;
  margin: 20px auto;
  padding: 10px 22px;
  font-size: 16px;
  color: #000053;
  position: relative;
  z-index:10;
}
.contact button .overlay{
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background-color: #babab8;
  z-index: -1;
  transition: 1s;
}
.contact button:hover .overlay{
  width: 100%;
}
.contact .col img .img1{
  width:100%
}
.contact .col .info{
  position: absolute;
  top:40%;
  background-color: #000053;
  color:#babab8;
  padding: 20px;
  max-width: 350px;
  left: 50%;
  transform: translate(-50%, -50%);
}
.contact .col .info ul {
  list-style: none;
}
.contact .col .info ul li{
  margin-bottom: 20px;
}
.contact .col .info ul li img.img2 {  
  display:inline-block;
  margin-right: 20px;
}
#nav ul li:hover {
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
}

#nav ul li.actif a {
  text-decoration: underline;
}
</style>