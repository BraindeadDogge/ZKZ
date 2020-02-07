<template>
  <div>
    <v-carousel show-arrows-on-hover cycle height="95vh">
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>
    <v-card-title class="text-center justify-center py-6" style="transform: translateY(-60vh); height: 0px">
      <h1 class="font-weight-thin display-4" style="text-shadow: 0.5px 0.5px 1px rgba(0,0,0,1); color: #FBE9E7">Инженерное Бюро <br/> "КрахмалоПродукты"</h1>
    </v-card-title>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: '1.png',
          },
          {
            src: '2.jpg',
          },
          {
            src: '3.jpg',
          },
          {
            src: '4.jpg',
          },
        ],
      }
    },
  }
</script>