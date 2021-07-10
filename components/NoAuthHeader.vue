<template>
  <div class="header-ctn-wrapper">
    <img src="@/assets/images/piggyvest-logo-1.png" alt="">
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
  max-width: 1280px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 1.5rem;
  position: absolute;
  top: 0;
  background: #fff;
  z-index: 20;
  transition: 0.5s ease-in-out;
  margin-left: auto;
  margin-right: auto;
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
  margin-left: 16px;
}

li a {
  padding: 1rem 1.2rem;
  height: 190px;
  font-weight: 500;
  font-size: 16px;
  white-space: nowrap;
}

li a:hover {
  background-color:rgb(243, 244, 246);
  border-radius: 8px 8px 8px 0;
  transition: 0.5s ease-in-out;
}

@media (max-width: 1024px) {
 
}

@media (max-width: 920px) {
  .header-ctn-wrapper {
    /* padding: 0 4rem; */
  }
   .header-ctn-wrapper nav {
    display: none;
  }

}

</style>