<template>
  <div>
    <img src="../assets/logo-spotify.png" alt="">
  </div>
</template>

<script>
export default {
  name: 'HeaderAlbums',
  data() {
    return {
            
        }
    },
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
div {
    background-color: #2E3A46;
    height: 10vh;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    padding: 20px;

    img {
        width: 50px;
    }
}
</style>