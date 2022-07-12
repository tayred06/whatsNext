<template>
  <div class="searchCard">
    <h2>Rechercher</h2>
    <p>Je recheche un / une </p>
    <select name="type" id="type">
        <option disabled selected value="">Choisir une option ...</option>
        <option value="artist">Artiste</option>
        <option value="chanson">Chanson</option>
        <!-- <option value="style">Style</option> -->
    </select>
    <p>comme</p>
    <input type="text" name="search" id="search">
  </div>
</template>

<script>
export default {
  name: 'searchCard',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .searchCard {
        background-color: #35363a;
        width: 100%;
        height: 30vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 25px;
    }
    select, input {
        width: 50%;
        border-radius: 10px;
        border: none;
        outline: none;
        padding: 5px 20px;
    }
    input {
        height: 15px;
    }
    select {
        height: 25px;
    }
</style>
