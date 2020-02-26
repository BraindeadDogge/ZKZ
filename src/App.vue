<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      color="yellow lighten-5"
    >
      <v-list dense>
        <v-list-item link @click="$vuetify.goTo('#main')">
          <v-list-item-action>
            <v-icon>mdi-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Главная</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link @click="$vuetify.goTo('#info')">
          <v-list-item-action>
            <v-icon>mdi-alpha-i-circle-outline</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Информация</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link @click="$vuetify.goTo('#contact')"> 
          <v-list-item-action>
            <v-icon>mdi-contact-mail</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Контакты</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      color="yellow lighten-4"
      light
      right
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer></v-spacer>
      <v-toolbar-title style="white-space: nowrap"><strong>Инженерное Бюро Крахмалопродукты</strong></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <Carouselka id="main"></Carouselka>
      <v-container
        fluid
        style="padding-bottom: 0px;"
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col class="text-center">
            <Carto4ka id="info" style="margin-top: -55px; margin-bottom: 25px"/>
            <Paralax1 style="min-height: 100vh; padding-left: 10vw; padding-right: 10vw; margin-left: -13px; margin-right: -13px; display: flex; align-items: center"><Carta1/></Paralax1>
            <Paralax2 style="min-height: 100vh; padding-left: 10vw; padding-right: 10vw; margin-left: -13px; margin-right: -13px; display: flex; align-items: center"><Carta2/></Paralax2>
          </v-col>
        </v-row>
      </v-container>

      <v-footer
        dark
        padless
        id="contact"
        style="margin-top: -13px;"
      >
        <v-card
          flat
          tile
          class="grey darken-4 white--text text-center"
        >

          <v-card-text class="white--text pt-0" style="width: 100vw">
          <br>
          +7 (916) 900-91-19 <br>
          +7 (916) 231-28-70 <br>
          KRAHMALPRODUCT@GMAIL.COM <br>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            <span >2019 — <strong>Инженерное Бюро "Крахмалопродукты"</strong></span>
            <AGtag style="margin: 13px 0 2px 0"/>
          </v-card-text>
        </v-card>
      </v-footer>

    </v-content>
  </v-app>
</template>

<script>
  import Carouselka from '@/components/Carouselka.vue'
  import Carto4ka from '@/components/Carto4ka.vue'
  import Carta1 from '@/components/Carta1.vue'
  import Carta2 from '@/components/Carta2.vue'
  import Paralax1 from '@/components/Paralax1.vue'
  import Paralax2 from '@/components/Paralax2.vue'
  import AGtag from '@/components/AGtag.vue'

  export default {
    components: {
      Carouselka,
      Carto4ka,
      Carta1,
      Carta2,
      Paralax1,
      Paralax2,
      AGtag
    },
    props: {
      source: String,
    },
    data: () => ({
      drawer: false,
    }),
  }
</script>