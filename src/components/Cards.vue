<template>
  <div id="Cards">
    <v-card :loading="loading" class="mx-auto">
      <v-img
        height="250"
        :src="`http://172.105.75.12:8888/${item.image}`"
      ></v-img>
      <div class="my-4 subtitle-1 px-2 black--text">
        <span class="text-left title">{{ item.name }} •</span>
        <em class="text-right font-15 float-right">${{ item.price }}</em>
      </div>
      <v-card-actions>
        <v-btn depressed color="primary" @click="addToCard(item)" class="w-100"
          >Add to Card 🛒</v-btn
        >
      </v-card-actions>
    </v-card>
  </div>
</template>
<script>
import Toasted from 'vue-toasted'

export default {
  name: 'Cards',
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  data() {
    return {}
  },
  methods: {
    addToCard(item) {
      let items = JSON.parse(localStorage.getItem('items')) || []
      let oneItem = items.filter(x => x.id == item.id)
      if (oneItem.length == 0) {
        items.push({ ...item, qty: 1 })
        return localStorage.setItem('items', JSON.stringify(items))
      }
      let arr = []
      for (let i of items) {
        if (i.id == item.id) i.qty = ++i.qty
        arr.push(i)
      }
      localStorage.setItem('items', JSON.stringify(arr))
      this.$toasted.show(`${item.name} Now in your card 🛒!`).goAway(1500)
    }
  }
}
</script>
<style scoped>
.font-15 {
  font-size: 15px !important;
}
</style>
