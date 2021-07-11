<template>
  <div class="header-ctn-wrapper">
    <img src="@/assets/images/piggyvest-logo.png" class="piggyvest-logo main-logo" alt="" @click="$router.push('/')">
    <nav>
      <ul class="header-links">
        <li>
          <nuxt-link to="/save">Save</nuxt-link>
          <ul class="header-link-links">
            <li>
              <nuxt-link to="/save/piggybank">
                <img src="@/assets/images/piggybank-icon.svg" alt="">
                <div class="inner-link">
                  <span>Piggybank</span>
                  <span>Strict Savings Automtically. Weekly, Daily Or Monthly</span>
                </div>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/save/safelock">
                <img src="@/assets/images/safelock-icon.svg" alt="">
                <div class="inner-link">
                  <span>Safelock</span>
                  <span>Lock Funds to Avoid Temptations. Upfront Interest</span>
                </div>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/save/targets">
                <img src="@/assets/images/target-savings-icon.svg" alt="">
                <div class="inner-link">
                  <span>Target Savings</span>
                  <span>Reach Your Unique Individual Saving Goals</span>
                </div>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/save/flex-naira">
                <img src="@/assets/images/flex-icon.svg" alt="">
                <div class="inner-link">
                  <span>Flex Naira</span>
                  <span>Flexible Savings For Emergency Free Transfers, Withdrawals Etc</span>
                </div>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/save/flex-dollar">
                <img src="@/assets/images/flex-dollar-icon.svg" alt="">
                <div class="inner-link">
                  <span>Flex Dollar</span>
                  <span>Save & Grow Your Wealth In Foreign Currencies</span>
                </div>
              </nuxt-link>
            </li>
          </ul>
        </li>
        <li>
          <nuxt-link to="/invest">Invest</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/stories">Stories</nuxt-link>
        </li>
        <li>
          <nuxt-link to="dashboard/login">Login</nuxt-link>
        </li>
        <li>
          <nuxt-link to="dahsboard/register" class="register">Create A Free Account</nuxt-link>
        </li>
      </ul>
    </nav>
    <div class="smaller-header">
      <img src="@/assets/images/piggyvest-logo.png" class="piggyvest-logo sec-logo" alt="" @click="$router.push('/')">
      <button class="header-menu" @click="showMenu = !showMenu">
        <span v-if="!showMenu" class="material-icons">
          menu
        </span>
        <span v-else class="material-icons">
          close
        </span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      showMenu: false
    }
  },
  watch: {
    showMenu:{
      handler() {
      this.$emit('menu-active', this.showMenu)
      }
    }
  }
}
</script>

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

.piggyvest-logo {
  transform: scale(0.5);
  transform-origin: 0;
  cursor: pointer;
}

nav .header-links {
  display: flex;
}

nav .header-links>li {
  margin-left: 16px;
  position: relative;
}

.header-links > li > a {
  padding: 1rem 1.2rem;
  height: 60px;
  font-weight: 500;
  font-size: 16px;
}

.header-links > li > a {
  white-space: nowrap;
}

li a:hover {
  background-color:rgb(243, 244, 246);
  border-radius: 8px 8px 8px 0;
  transition: 0.5s ease-in-out;
}

.header-links>li>a:hover+.header-link-links {
  display: flex;
}

.header-link-links {
  background: #fff;
  box-shadow: -1px 5px 15px 1px rgba(18, 94, 164, 0.08);
  position: absolute;
  top: 35px;
  width: 550px;
  display: none;
  /* display: flex; */
  flex-wrap: wrap;
  align-items: flex-start;
  border-radius: 8px 8px 8px 0;
}

.header-link-links:hover {
  display: flex;
}

.header-link-links li a {
  display: flex;
  /* width: 100% */
}

.header-link-links li a div {
  display: flex;
  flex-direction: column;
}

.header-link-links li {
  width: 50%;
  height: 80px;
}

.header-link-links li a {
  width: 100%;
  height: 100%;
  padding: 10px;
}

.header-link-links img {
  transform: scale(0.5);
  transform-origin: 0 0;
  position: relative;
  left: 10px;
}

.header-link-links li span:nth-of-type(1) {
  font-weight: 600;
  font-size: 15px;
  margin-bottom: 4px;
}

.header-link-links li span:nth-of-type(2) {
  font-size: 11px;
  line-height: 15px;
}

.smaller-header button {
  background: transparent;
  width: 33px;
  height: 38px;
  border-radius: 3px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  border: none
}

.smaller-header button:focus {
  border: 2px solid #000;
}

.smaller-header button span {
  transform: scale(1.4);
  color: rgb(8, 62, 158);
  font-weight: 700;
  /* width: 100%; */
}

@media (min-width: 1024px) {
  .smaller-header {
    display: none;
  }
}

@media (max-width: 1024px) {
  .header-ctn-wrapper {
    padding: 0 5rem;
    height: 50px;
  }

  .piggyvest-logo {
    transform: scale(0.3);
  }
  .header-ctn-wrapper nav,
  .piggyvest-logo.main-logo {
    display: none;
  }

  .header-ctn-wrapper {
    justify-content: center;
  }

  .smaller-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }
}

</style>