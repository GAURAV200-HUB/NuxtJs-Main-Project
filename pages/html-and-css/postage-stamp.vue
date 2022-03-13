<template>
  <div class="postage-stamp center">
    <v-container>
      <v-row align="center" justify="center">
        <v-col
          v-for="(post, index) in postageStamp"
          :key="index"
          cols="12"
          sm="12"
          md="4"
          lg="4"
        >
          <div :class="post.class"></div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'PostageStamp',
  data() {
    return {
      postageStamp: [
        {
          class: 'postage-stamp1',
        },
        {
          class: 'postage-stamp2',
        },
        {
          class: 'postage-stamp3',
        },
      ],
    }
  },
}
</script>

<style lang="css" scoped>
.postage-stamp2 {
  position: relative;
  width: 380px;
  height: 320px;
  background: #fff radial-gradient(#4fb6ff 0px, #4fb6ff 7px, transparent 7px);
  background-size: 20px 20px;
  background-position: -10px;
}
.postage-stamp2::before {
  content: '';
  position: absolute;
  inset: 20px;
  background: url('~/assets/images/postage-stamp/postage-stamp2.jpg');
  box-shadow: 0 0 0 10px #fff;
  background-size: cover;
  background-position: center center;
}
.postage-stamp3 {
  position: relative;
  width: 380px;
  height: 320px;
  background: #fff radial-gradient(#4fb6ff 0px, #4fb6ff 7px, transparent 7px);
  background-size: 20px 20px;
  background-position: -10px;
}
.postage-stamp3::before {
  content: '';
  position: absolute;
  inset: 20px;
  background: url('~/assets/images/postage-stamp/postage-stamp3.jpg');
  box-shadow: 0 0 0 10px #fff;
  background-size: cover;
  background-position: center center;
}
</style>
