<template>
  <div class="squid-game-page">
    <section class="banner">
      <div class="header">
        <div
          class="toggle"
          :class="active ? 'active' : ''"
          @click="toggle()"
        ></div>
        <a href="#" class="logo">
          <img src="../../../assets/images/squid-game/logo.png" alt="logo" />
        </a>
      </div>
      <div class="content">
        <img
          src="../../../assets/images/squid-game/text.png"
          alt="text"
          class="textimg"
        />
        <p>
          Hundreds of cash-strapped players accept a strange invitation to
          compete in children's games. Inside, a tempting prize awaits - with
          deadly high stakes.
        </p>
        <a href="#" class="btn">
          <v-icon class="mr-1">mdi-play-circle-outline</v-icon>
          Watch Trailer
        </a>
      </div>
      <div class="clip">
        <div class="clipBox">
          <img src="../../../assets/images/squid-game/img1.jpg" alt="img1" />
          <v-icon x-large class="mr-1">mdi-play-circle-outline</v-icon>
        </div>
        <div class="clipBox">
          <img src="../../../assets/images/squid-game/img2.jpg" alt="img2" />
          <v-icon x-large class="mr-1">mdi-play-circle-outline</v-icon>
        </div>
      </div>
      <ul class="socialIcon">
        <li>
          <a href="#">
            <v-icon>mdi-facebook</v-icon>
          </a>
        </li>
        <li>
          <a href="#">
            <v-icon>mdi-instagram</v-icon>
          </a>
        </li>
        <li>
          <a href="#">
            <v-icon>mdi-twitter</v-icon>
          </a>
        </li>
      </ul>
    </section>
    <ul class="navigation" :class="active ? 'active' : ''">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Cast</a></li>
      <li><a href="#">Shop</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'SquidGame',
  data() {
    return {
      active: false,
    }
  },
  methods: {
    toggle() {
      this.active = !this.active
    },
  },
}
</script>

<style lang="css" scoped>
.squid-game-page {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.banner {
  min-height: 100vh;
  background: #120e0f url('../../../assets/images/squid-game/bg.jpg');
  background-position: center;
  background-size: cover;
  padding: 40px 100px;
  display: flex;
  align-items: center;
}

.banner .header {
  position: absolute;
  top: 40px;
  display: flex;
  align-items: center;
}
.logo {
  max-width: 120px;
}
.banner .header .toggle {
  position: relative;
  width: 50px;
  height: 50px;
  background: #fff;
  margin-right: 20px;
  cursor: pointer;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}

.banner .header .toggle::before {
  content: '';
  position: absolute;
  width: 28px;
  height: 3px;
  background: #120e0f;
  transform: translateY(-6px);
  transition: 0.5s;
}

.banner .header .toggle.active::before {
  transform: translateY(0) rotate(45deg);
}

.banner .header .toggle::after {
  content: '';
  position: absolute;
  width: 28px;
  height: 3px;
  background: #120e0f;
  transform: translateY(6px);
  transition: 0.5s;
}

.banner .header .toggle.active::after {
  transform: translateY(0) rotate(-45deg);
}

.navigation {
  position: fixed;
  z-index: 9;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #120e0f url('../../../assets/images/squid-game/menuBg.jpg');
  background-position: right;
  background-size: cover;
  display: none;
  padding-right: 100px;
}

.navigation.active {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  flex-direction: column;
}

.navigation li {
  list-style: none;
  margin: 4px 0;
}

.navigation li a {
  color: #fff;
  font-size: 2em;
  letter-spacing: 0.05em;
  text-decoration: none;
  font-weight: 600;
  text-transform: uppercase;
}

.navigation li a:hover {
  color: #e83c80;
}

.content {
  position: relative;
  max-width: 700px;
}

.content .textimg {
  max-width: 600px;
  width: 100%;
}

.content p {
  color: #fff;
  font-size: 1.2em;
  line-height: 1.75em;
  font-weight: 300;
}

.content .btn {
  position: relative;
  background: #e83c80;
  color: #fff;
  padding: 10px 18px;
  display: inline-flex;
  align-items: center;
  margin-top: 20px;
  font-size: 1.1em;
  font-weight: 400;
  text-decoration: none;
}

.content .btn:hover {
  background: #d43071;
}
.clip {
  position: absolute;
  right: 100px;
  bottom: 40px;
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
}

.clip .clipBox {
  position: relative;
  width: 340px;
  height: 220px;
  border: 8px solid #fff;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.clip .clipBox img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  cursor: pointer;
}

.socialIcon {
  position: absolute;
  bottom: 40px;
  left: 100px;
  display: flex;
  align-items: center;
  gap: 40px;
}

.socialIcon li {
  list-style: none;
}

.socialIcon li a {
  font-size: 2em;
  color: #fff;
  text-decoration: none;
}

.socialIcon li a:hover {
  color: #e83c80;
}

@media only screen and (max-width: 1100px) {
  .banner {
    padding: 40px;
    flex-direction: column;
    align-items: flex-start;
  }
  .content {
    margin-top: 150px;
  }
  .clip {
    position: relative;
    right: initial;
    bottom: initial;
  }
  .socialIcon {
    position: relative;
    bottom: initial;
    left: initial;
  }
  .navigation {
    padding-right: 40px;
  }
}
</style>
