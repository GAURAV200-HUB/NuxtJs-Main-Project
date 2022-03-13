<template>
  <div class="html-and-css-page">
    <v-container>
      <v-row align="center" justify="center">
        <v-col
          v-for="(web, index) in webDesigns"
          :key="index"
          cols="12"
          sm="12"
          md="4"
          lg="4"
        >
          <v-card>
            <v-card-title>
              <div class="card-header">{{ web.header }}</div>
            </v-card-title>
            <v-divider />
            <v-card-text>
              <div class="card-body">
                {{ web.body }}
              </div>
            </v-card-text>
            <v-divider />
            <v-card-actions class="card-footer">
              <v-btn color="primary" :to="web.to">View</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12">
          <h1>Parallax Designs</h1>
          <a href="../../designs/halloween-parallax/index.html" target="_blank">Go</a>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'HtmlAndCss',
  data() {
    return {}
  },
  computed: {
    webDesigns() {
      return this.$store.state.htmlcssjs.webDesigns
    },
  },
}
</script>

<style lang="css" scoped>
.html-and-css-page .card-footer {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
