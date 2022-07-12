<template>
  <div class="home">
    <searchCard/>
    <div class="reponse">
      <responseCard/>
      <responseCard/>
      <responseCard/>
      <responseCard/>
      <responseCard/>
      <responseCard/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import searchCard from '@/components/searchCard.vue'
import responseCard from '@/components/responseCard.vue'
let openai = require('openai-api');

export default {
  name: 'Home',
  components: {
    searchCard,
    responseCard
  },
  mounted (){
    const OPENAI_API_KEY = "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";

    openai = new openai(OPENAI_API_KEY);
    (async () => {
  const gptResponse = await openai.classification({
    "examples": [
      ["A happy moment", "Positive"],
      ["I am sad.", "Negative"],
      ["I am feeling awesome", "Positive"]
    ],
    "labels": ["Positive", "Negative", "Neutral"],
    "query": "It is a nice day :)",
    "search_model": "ada",
    "model": "curie"
  });

  console.log(gptResponse.data);
})();
  }
}
</script>

<style scoped>
  .home {
    width: 50%;
  }
  .reponse {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 20px;
  }
</style>