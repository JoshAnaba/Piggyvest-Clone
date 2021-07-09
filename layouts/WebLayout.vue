<template>
  <div class="web-ctn-wrapper">
    <NoAuthHeader/>
    <Nuxt class="page-container"/>
  </div>
</template>

<style scoped>
.web-ctn-wrapper {
  width: 100%;
  min-height: 100vh;
}

.page-container {
  margin-top: 80px;
}
</style>