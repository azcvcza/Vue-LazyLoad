<template>
  <div id="app">
    <ArticlesList />
    <link href="https://fonts.googleapis.com/css?family=Roboto:100,300" rel="stylesheet">
    
  </div>
</template>

<script>
import ArticlesList from "./components/ArticlesList";

export default {
  name: "App",
  components: {
    ArticlesList
  }
};
</script>

<style>
#app {
  font-family: "Roboto", sans-serif;

  
}
#app .news-api-link {
    display: flex;
    justify-content: center;
    position: fixed;
    bottom: 0;
    right: 0;
    width: 100%;
    background: #fff;
  }
</style>