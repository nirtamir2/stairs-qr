<template>
  <v-tabs id="mobile-tabs-3" grow light>
    <v-tabs-bar slot="activators">
      <v-tabs-slider></v-tabs-slider>
      <v-tabs-item
        v-for="header in headers"
        :key="header"
        :href="'#' + header"
      >
        header
      </v-tabs-item>
    </v-tabs-bar>
    <v-tabs-content
      v-for="header in headers"
      :key="header"
      :id=" '#'+ header"
    >
      <v-card flat>
        <v-card-text>{{ text }}</v-card-text>
      </v-card>
    </v-tabs-content>
  </v-tabs>
</template>

<script>
  export default {
    data () {
      return {
        headers: ['About', 'My Score', 'High Scores'],
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
      }
    }
  }
</script>
