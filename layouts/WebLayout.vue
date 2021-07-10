<template>
  <div class="web-ctn-wrapper">
    <NoAuthHeader/>
    <Nuxt class="page-container"/>
  </div>
</template>

<script>
export default {
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

@media (max-width: 920px) {
  .page-container {
    padding: 0 4rem;
  }
}



</style>