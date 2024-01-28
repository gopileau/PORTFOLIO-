<template>
<footer>
    <div class="social-icons">
    <a href="https://github.com/dashboard" target="_blank"><img src="..//assets/github.png" alt="GitHub" width="30px" height="30px"></a>
    <a href="https://es.linkedin.com/" target="_blank"><img src="..//assets/linke.png" alt="LinkedIn" width="30px" height="30px"></a>
    <a href="https://www.facebook.com/" target="_blank"><img src="..//assets/facebook.png" alt="GitHub" width="30px" height="30px"></a>
    <a href="https://www.instagram.com/" target="_blank"><img src="..//assets/instagram.png" alt="LinkedIn" width="30px" height="30px"></a>
    </div>
    <p class="last-update">Dernière mise à jour : 24 janvier 2024</p>
    </footer>
</template>
<script>
export default {
  name: 'FooterComponent'
};
</script>

<style scoped>
footer {
color: #000058;
width: 100%;
padding-top: 40px;
}

.social-icons img {
  margin: 0 10px;
  border-radius: 50%;
  border: 2px solid #000058; 
}

</style>