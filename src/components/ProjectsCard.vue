<template>
    <div class="main-container">
      <div class="project-card" v-for="(items, index) in projectData.projectsArray" v-bind:key="items">
        <h2>{{ projectData.projectsArray[index].Title }}</h2>
        <img :src="projectData.projectsArray[index].image" alt="">
        <p>{{ projectData.projectsArray[index].About }}</p>
        <div class="links">
            <a :href="projectData.projectsArray[index].link1" target="blank"><img src="../assets/github.png" alt=""></a>
            <a :href="projectData.projectsArray[index].link2" ><img src="../assets/linke.png" alt=""></a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import jsonData from "/projects.json"
  export default {
    data() {
      return {
        projectData: jsonData 
      }
    }
  }
  </script>
  
  <style scoped>
    .main-container{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }
    .project-card{
        margin: 5%;
        padding: 10px;
        flex-wrap: 0 0 40%;
        background-color: #fff;
        border-radius: 25px;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    }
    .project-card img{
        height: 10rem;
    }
    .links{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-end;
    }
    .links img{
        height: 1.5rem;
        margin: 5px;
    }
</style>