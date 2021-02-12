<template>
  <v-card flat color="transparent" max-width="350px">
    <v-card-title>
      <v-layout>
        <v-flex>
          <v-card
            elevation="5"
            class="rounded-xl pa-2"
            width="100px"
            height="100px"
          >
            <v-img :src="logo(data.logo)" />
          </v-card>
        </v-flex>
        <v-flex xs7 align-self-center>
          <div>{{ data.name }}</div>
        </v-flex>
      </v-layout>
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default: function() {
        return {};
      },
    },
  },
  methods: {
    logo(name) {
      return require("../assets/" + name);
    },
  },
};
</script>
