<template>
  <div class="home">
    <div class="card">
      <router-link to="/movie/tt0409591">
        <img
          src="https://posterspy.com/wp-content/uploads/2020/04/DuneFINAL-1200x609.jpg"
          alt="feature-img"
        />
        <div class="detail">
          <h3>Dune</h3>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque
            officiis blanditiis inventore.
          </p>
        </div>
      </router-link>
    </div>

    <form @submit.prevent="SearchMovies()" class="search-box">
      <input type="text" placeholder="Search for a movie" v-model="search" />
      <input type="submit" value="Search" />
    </form>

    <div class="movie-lis">Movies</div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const search = ref("");
    const movies = ref([]);

    const SearchMovies = () => {
      if (search.value != "") {
        console.log(search.value);
      }
    };

    return {
      search,
      movies,
      SearchMovies,
    };
  },
};
</script>

<style lang="scss">
.home {
  .card {
    position: relative;
  }

  img {
    display: block;
    width: 100%;
    height: 300px;
    object-fit: cover;
    position: relative;
  }

  .detail {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.6);
    padding: 1rem;
    z-index: 1;
    color: #fff;

    h3 {
      margin-bottom: 1rem;
    }
  }

  .search-box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1rem;

    input {
      display: block;
      border: none;
      outline: none;
      background: none;
      width: 100%;
      padding: 0.8rem;
      border-radius: 8px;
      color: #fff;

      &[type="text"] {
        font-size: 16px;
        border: 1px solid white;
        margin-bottom: 1rem;
        transition: 0.4s;

        &::placeholder {
          color: #f3f3f3;
        }
      }

      &[type="submit"] {
        background-color: #42b883;
        font-size: 20px;
        text-transform: uppercase;
        letter-spacing: 2px;
        transition: 0.4s;

        &:active {
          background-color: #3b8070;
        }
      }
    }
  }
}
</style>
