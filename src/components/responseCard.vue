<template>
  <div class="responseCard">
      <p class="titre">Dior</p>
      <p class="artist">Pop Smook</p>
      <a href="https://www.youtube.com" target="_blank" >Ecouter <img src="../../public/img/circle-play-regular.svg" alt="play"></a>
  </div>
</template>

<script>
export default {
  name: 'responseCard',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .responseCard {
        background-color: #35363a;
        width: 48%;
        height: 15vh;
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;
    }
    p {
        margin: 0;
    }
    a {
        color: #35363a;
        text-decoration: none;
        background-color: #ffdc2b;
        padding: 5px 20px;
        border-radius: 10px;
        margin-top: 10px;
        transition: 0.3s;
        display: flex;
        align-items: center;
    }
    a:hover {
        border-radius: 20px;
    }
    a img {
        width: 20px;
        margin-left: 10px;
    }
</style>
