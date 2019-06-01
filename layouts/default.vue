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
          value="nearby"
        >
          <span>さがす</span>
          <v-icon>maps</v-icon>
        </v-btn>
        <v-btn
          color="blue"
          flat
          value="favorites"
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
      fixed: false,
      items: [
        {
          icon: 'maps',
          title: 'みつける',
          to: '/'
        },
        {
          icon: 'create',
          title: 'のこす',
          to: '/create'
        },
        {
          icon: 'list_alt',
          title: 'みかえす',
          to: '/history'
        }

      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'まちあるき'
    }
  }
}
</script>
