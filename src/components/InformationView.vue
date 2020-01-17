<template>
  <div id="content">
    <v-row class="my-3">
      <v-col v-for="(card, index) in cards" :key="index" md-cols="4" cols="12">
        <div
          :style="
            `background: url(https://www.ordr.cz/Content/Img/Sprites/draws.png) ${
              card.width
            };width: ${
              card.width == '-2px -498px' ? '225px' : '128px'
            };height: 118px;margin: 0px auto;`
          "
        ></div>

        <v-card-title primary-title>
          <div>
            <h3 class="headline text-center mb-0">{{ card.title }}</h3>
            <div class="text-center">{{ card.content }}</div>
          </div>
        </v-card-title>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Fast & Easy',
          content: 'Get your meal easier and faster with ZeroFOOD ❤️',
          width: '-2px -498px'
        },
        {
          title: 'All Safe',
          content: 'Safe & secure payment methods 🔐',
          width: '-2px -107px'
        },
        {
          title: 'Few Clicks',
          content:
            'Just a few clicks on the web or in the mobile app and every thing is ready 😉!',
          width: '-2px -374px'
        }
      ]
    }
  }
}
</script>

<style></style>
