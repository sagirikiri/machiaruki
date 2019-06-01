<template>
  <v-app>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-bottom-nav
        :active.sync="bottomNav"
        :value="true"
        fixed
        >
        <v-btn
          color="blue"
          flat
          value="search"
          to="/"
        >
          <v-icon>search</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="favorite"
          to="/favorite"
        >
          <v-icon>favorite</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="write"
          to="/create"
        >
          <v-icon>create</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="recent"
          to="/history"
        >
          <v-icon>history</v-icon>
        </v-btn>
    </v-bottom-nav>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: true,
      title: 'まちあるき',
      bottomNav: 'search'
    }
  }
}
</script>
