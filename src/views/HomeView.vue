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
  </div>
</template>

<script>
export default {};
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
    padding: 16px;
    z-index: 1;
    color: #fff;

    h3 {
      margin-bottom: 16px;
    }
  }
}
</style>
