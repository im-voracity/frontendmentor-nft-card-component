<template>
  <nft-card></nft-card>
</template>

<script>
import NftCard from "@/components/NftCard";

export default {
  name: 'App',
  components: {
    NftCard
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
}

html {
  background-color: hsla(217, 54%, 11%, 1);
  height: 100vh;
  width: 100vw;
}

body {
  height: 100%;
  width: 100%;
}

#app {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
