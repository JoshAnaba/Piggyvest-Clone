<template>
  <div class="header-ctn-wrapper">
    <img src="@/assets/images/piggyvest-logo.png" alt="">
    <nav>
      <ul>
        <li>
          <nuxt-link to="/save">Save</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/invest">Invest</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/stories">Stories</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/login">Login</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/register" class="register">Create A Free Account</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
.header-ctn-wrapper {
  height: 80px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  /* position: absolute; */
}

img {
  transform: scale(0.5);
  transform-origin: 0;
  cursor: pointer;
}

nav ul {
  display: flex;
}

nav li {
  margin: 0 8px;
}

li a {
  padding: 1rem 1.2rem;
  font-weight: 500;
}

li a:hover {
  background-color:rgb(243, 244, 246);
  border-radius: 8px 8px 8px 0;
  transition: 0.5s ease-in-out;
}

</style>