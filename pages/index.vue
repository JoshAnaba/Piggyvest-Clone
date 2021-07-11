<template>
  <div class="main-ctn">
    <section class="overview">
      <div class="overview-ctn">
        <div class="overview-text">
          <h1>The Better Way <br>to Save & Invest</h1>
          <p>PiggyVest helps over 2 million customers achieve their financial goals by helping them save and invest with ease.</p>
          <span>Earn 5% - 15% interests on savings and over 25% return on investments.</span>
          <nuxt-link to="dashboard/register" class="register">Create A Free Account</nuxt-link>
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
      <div class="security-ctn">
        <h2>Security Comes First</h2>
        <div class="security-content">
          <div>
            <img src="@/assets/images/key-icon.svg" alt="">
            <p>PiggyVest uses the highest levels of Internet Security, and it is secured by 256 bits SSL security encryption to ensure that your information is completely protected from fraud.</p>
          </div>
          <div>
            <img src="@/assets/images/shine-icon.svg" alt="">
            <p>Two-factor authentication (2FA) by default on all PiggyVest accounts, to securely protect you from unauthorised access and impersonation.</p>
          </div>
        </div>
      </div>
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
/* .main-ctn>* { */
  /* display: flex; */
  /* justify-content:stretch; */
  /* margin: 50px; */
  /* width: calc(100%-50px); */
/* } */

/* overview */
.overview {
 height: 100vh;
 margin-top: 160px;
}

.overview-ctn {
  display: flex;
  justify-content: space-between;
  padding: 20px;
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
  line-height: 52px;
  color: rgb(8, 62, 158);
  font-size: 44px;
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
  height: 145%;
  background-image: url('@/assets/images/piggy-hero-cover-photo.jpg');
  background-size: cover;
  border-radius: 20px 20px 20px 0;
  position: relative;
  bottom: 45px;
  margin-right: 20px;
}

.piggy-hero-cover-photo {
  border-radius: 20px 20px 20px 0;
  height: 100%;
  width: 90%;
  position: relative;
  bottom: 45px;
}

@media (max-width: 1024px) {

  .overview {
    margin-top: 100px;
  }
  
  .overview-img {
    display: none;
    margin-left: auto;
  }

  .overview-text {
    align-items: center;
  }
  
  .overview-ctn {
    justify-content: center;
    text-align: center;
    /* min-height: 360px; */
    /* padding: 0 10rem; */
  }

  .overview-text {
    width: 100%;
  }

  .overview-text a {
    margin-left: 0;
  }

  .overview-text h1 {
    font-size: 23px;
    line-height: 28px;
  }

  .overview-text span {
    font-size: 11px;
  }

  .store {
    display: flex;
    justify-content: center;
  }

  .store img:nth-of-type(1) {
  transform: scale(1.2);
  transform-origin: 0;
  cursor: pointer;
  position: relative;
  left: 15px;
}

.store img:nth-of-type(2) {
  transform: scale(0.6);
  cursor: pointer;
  position: relative;
  left: 15px;
}
}

/* security */

.security {
  display: flex;
  justify-content: center;
  padding: 20px 0;
}

.security h2 {
  font-size: 33px;
  line-height: 40px;
  font-weight: 700;
  text-align: center;
  margin-bottom: 30px;
}

/* .security-ctn {
  display: flex;
} */

.security-content {
  display: flex;
}

.security-content div {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px 45px;
  width: 50%;
}

.security-content p {
  font-size: 16px;
  text-align: center;
  line-height: 23px;
}

.security-content img {
  margin-bottom: 20px;
  transform: scale(1.2);
}

@media (max-width: 1024px) {
  .security-content {
    flex-direction: column;
  }

}

</style>
