<template>
  <div id="app">
    <MainCard />
  </div>
</template>

<script>
import MainCard from "@/components/MainCard.vue";

export default {
  name: "App",
  components: {
    MainCard,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>

