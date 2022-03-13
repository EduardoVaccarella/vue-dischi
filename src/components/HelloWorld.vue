<template>
  <div class="main">
    <ul>
      <li v-for="(album,i) in albums[0]" :key="i">
          
        <img :src="album.poster" alt="">
          
        <h2>
          {{ album.title }}
        </h2>
        
        <div>
          {{ album.author }}
          {{ album.year }}
        </div>
        
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      albums: []
    }
  },
    mounted() {
          this.$axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
                this.albums.push(res.data.response)
          })
    }
}
</script>

<style scoped lang="scss">
ul {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 40px;
  padding: 90px 400px;
  background-color: #1E2D3B;

  li {
    width: 15%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 20px;
    background-color: #2E3A46;

    img {
      max-width: 100%;
      overflow: hidden;
    }

    h2 {
      padding: 10px;
      color: white;
    }

    div {
      margin-top: 5px;
      color: grey;
    }
  }
}
</style>
