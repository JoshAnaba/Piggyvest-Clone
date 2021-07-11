<template>
  <div class="web-ctn-wrapper" :class="[fixedPosition ? 'fixed-position': '']">
    <NoAuthHeader @menu-active="menuActive"/>
    <Nuxt class="page-container"/>
  </div>
</template>

<script>
export default {
  data(){
    return {
      fixedPosition: null
    }
  },
  mounted(){
    //  const ctn = document.querySelector('.web-ctn-wrapper')
     const headerCtn = document.querySelector('.header-ctn-wrapper')
    //  const pageCtn = document.querySelector('.page-container')
      window.onscroll = () => scrollFunction()
      function scrollFunction () {
      if ((document.body.scrollTop > 80) || (document.documentElement.scrollTop > 80)) {
         headerCtn.style.position = 'fixed'
      } else {
        headerCtn.style.position = 'absolute'
      }
    }
  },
  methods: {
    menuActive(val) {
      this.fixedPosition=val
    }
  }
}
</script>

<style scoped>
.web-ctn-wrapper {
  width: 100%;
  height: 100vh;
  max-width: 1280px;
  margin: auto;
}

.page-container {
  min-height: 100vh;
  padding: 0 1.5rem;
  /* overflow: auto; */
}

@media (max-width: 1024px) {
  .page-container,
  .header-ctn-wrapper {
    padding: 0 6rem;
  }
  .fixed-position {
    overflow: hidden;
  }
}

</style>