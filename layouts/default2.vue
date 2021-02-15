<template>
  <v-app>
    <v-toolbar color="cyan" dark>
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

      <v-toolbar-title>Go-DD</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-toolbar>
<!--     
    <v-navigation-drawer
      v-model="drawer"
      dark
      :permanent="drawer"
      :mini-variant.sync="mini"
      :clipped="clipped"
      :src="bg"
      :fixed="fixed"
      app
    > -->
      <v-list>
        <v-list-item two-line :class="miniVariant && 'px-0'">
          <!-- <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
            </v-list-item-avatar> -->

          <v-list-item-content>
            <v-list-item-title>Smart FM</v-list-item-title>
            <v-list-item-subtitle>FM Engine</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      sidebarMenu: true,
      clipped: false,
      drawer: true,
      fixed: true,
      background: true,
      toggleMini: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'IEQ',
          to: '/ieq',
        },
        {
          icon: 'mdi-apps',
          title: 'HVAC',
          to: '/hvac',
        },
        {
          icon: 'mdi-apps',
          title: 'LSS-IOT',
          to: '/lssiot',
        },
      ],
      miniVariant: false,
      right: false,
      rightDrawer: false,
      title: 'Dashboard.',
    }
  },
  computed: {
    mini() {
      return this.$vuetify.breakpoint.smAndDown || this.toggleMini
    },
    bg() {
      return this.background
        ? 'https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg'
        : undefined
    },
  },
}
</script>
