<template lang='pug'>
  #movieCards
    div.movie-card-container
      h1 Available movies
      div.movie-cards
        div.movie-card(v-for='movie in movies')
          img(src='../../assets/logo.png')
          div.text-container
            h2 {{ movie.name }}
            p {{ movie.desc }}
</template>
<script>
export default {
  name: 'movieCards',
  data () {
    return {
      movies: [
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        },
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        },
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        },
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        },
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        },
        {
          name: 'Skeleton Dance by Silly Symphonies',
          desc: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit'
        }
      ]
    }
  }
}
</script>
<style lang='scss'>
#movieCards {
  width: 100%;
}

.movie-card-container {
  display: flex;
  flex-direction: column;
  margin: 20px00119px;

  .movie-card,
  .movie-cardimg {
    width: 287px;
    height: 192px;
    img {
      position: absolute;
      z-index: 0;
    }
  }

  .movie-cards {
    display: flex;
    flex-wrap: wrap;
  }

  .movie-card {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    margin: 10px10px10px0;

    .text-container {
      color: #fff;
      padding: 3px5px0;
      z-index: 1;
      background: #ff535b92;
      h2 {
        font-weight: bold;
      }
      p {
        font-size: 12px;
      }
    }
  }
}
</style>