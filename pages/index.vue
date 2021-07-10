<template>
  <div class="main-ctn">
    <section class="overview">
      <div class="overview-ctn">
        <div class="overview-text">
          <h1>The Better Way <br>to Save & Invest</h1>
          <p>PiggyVest helps over 2 million customers achieve their financial goals by helping them save and invest with ease.</p>
          <span>Earn 5% - 15% interests on savings and over 25% return on investments.</span>
          <nuxt-link to="/register" class="register">Create A Free Account</nuxt-link>
          <div class="store">
            <img src="@/assets/images/appstore.svg" alt="">
            <img src="@/assets/images/playstore.png" alt="">
          </div>
        </div>
        <div class="overview-img">
          <!-- <img src="@/assets/images/piggy-hero-cover-photo.jpg" class="piggy-hero-cover-photo" alt=""> -->
        </div>
      </div>
    </section>
    <section class="security">
      <h2>Security Comes First</h2>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'WebLayout',
  head(){
    return {
      title: "The Better Way To Save and Invest Online - Piggyvest"
    }
  },
}
</script>

<style scoped>
.main-ctn>* {
  /* display: flex; */
  /* justify-content:stretch; */
  /* margin: 50px; */
  /* width: calc(100%-50px); */
}

/* overview */
.overview {
 height: 100vh;
 margin-top: 160px;
}

.overview-ctn {
  display: flex;
  justify-content: space-around;
  background: #dff3fc;
  border-radius: 20px 20px 20px 0;
  height: 400px;
  /* height: 100%; */
}

.overview-text {
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 20px;
}

.overview-text h1 {
  line-height: 3.75rem;
  color: rgb(8, 62, 158);
  font-size: 3rem;
  font-weight: 700;
  letter-spacing: -1.5px;
}

.overview-text p:first-of-type {
  line-height: 21px;
  letter-spacing: 0.8px;
  font-size: 15px;
}

.overview-text span {
  color:rgb(16, 185, 129);
  background-color:rgb(209, 250, 229);
  padding: 0 10px;
  border-radius: 10px;
  font-size: 13px;
  margin: 15px 0 30px 0;
}

.overview-text a {
  transform: scale(1.1);
  margin-left: 10px;
}

.store {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding: 5px 0;
}

.store img:nth-of-type(1) {
  transform: scale(1.3);
  transform-origin: 0;
  cursor: pointer;
}

.store img:nth-of-type(2) {
  transform: scale(0.6);
  cursor: pointer;
}

.overview-img {
  width: 40%;
  max-width: 400px;
  height: 130%;
  background-image: url('@/assets/images/piggy-hero-cover-photo.jpg');
  background-size: cover;
  border-radius: 20px 20px 20px 0;
  position: relative;
  bottom: 45px;
}

.piggy-hero-cover-photo {
  border-radius: 20px 20px 20px 0;
  height: 100%;
  width: 90%;
  position: relative;
  bottom: 45px;
}

@media(max-width: 1024px) {
  .overview-img {
    margin-left: auto;
  }
}

@media (max-width: 920px) {
   .overview-img {
     display: none;
   }

   .overview-text {
     align-items: center;
   }

   .store {
     justify-content: center;
   }

   section>div {
     /* width: 740px; */
   }
}

/* security */

.security {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
