<template>
  <div class="web-ctn-wrapper">
    <NoAuthHeader/>
    <Nuxt class="page-container"/>
  </div>
</template>

<style scoped>
.web-ctn-wrapper {
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.page-container {
  margin-top: 80px;
  overflow: auto;
}
</style>