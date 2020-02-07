<template>
  <v-parallax
    dark
    src="4.jpg"
    height="100vh"
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col class="text-center" cols="12">
        <slot/>
      </v-col>
    </v-row>
  </v-parallax>
</template>