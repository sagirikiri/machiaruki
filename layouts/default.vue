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
          value="maps"
        >
          <span>さがす</span>
          <v-icon>maps</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="write"
        >
          <span>のこす</span>
          <v-icon>create</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="recent"
        >
          <span>みかえす</span>
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
      bottomNav: 'maps'
    }
  }
}
</script>
