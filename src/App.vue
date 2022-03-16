<template>
  <header>
    <router-link to="/">
      <h1>Movie<span>Vue</span>App</h1>
    </router-link>
  </header>
  <main>
    <router-view />
  </main>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Fira Sans", sans-serif;
  background-color: #131418;

  &::selection {
    background: transparentize(#43b883, 0.5);
  }
}

h1 {
  color: #fff;
  font-size: 28px;

  span {
    color: #42b883;
  }
}

a {
  text-decoration: none;
}

header {
  padding: 10px 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
