<template>
  <v-layout
    column
    justify-center
    align-center
  >
  <v-autocomplete
            v-model="model"
            :items="items"
            :loading="isLoading"
            :search-input.sync="search"
            color="white"
            item-text="Description"
            item-value=this.data.
            cache-items
            hide-no-data
            hide-selected
            placeholder="遊びプランを探す"
            prepend-icon="mdi-database-search"
            return-object>
  </v-autocomplete>
    <v-flex
    >
      <v-card
        v-for="item in items"
        v-bind:key="item.id"
      >
      <v-img
            src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
            aspect-ratio="2.75"
      ></v-img>
        <v-card-title class="headline">{{ item.title }}</v-card-title>
        <v-card-text>
          <p> {{ item.content }}</p>
        </v-card-text>
        <v-card-actions>
            <v-chip>{{ item.isPR ? 'PR' : 'テスト'}}</v-chip>
          <v-spacer />
          <v-btn
            color="primary"
            flat
            nuxt
            to="/create"
          >もっとみる(ストーリー投稿の内容が表示される。)</v-btn>
        </v-card-actions>
       <hr class="my-3">
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  methods: {

  },
  data() {
    return {
      items: [
        {
          id: 1,
          title: 'ストーリー投稿のタイトルが表示される',
          content: 'ストーリー投稿の最初のコンテンツの内容がここに表示される',
          image: '~/static/macchanrio.png',
          isPR: false
        },
        {
          id: 2,
          title: '横浜',
          content: '',
          image: '',
          isPR: false
        },
        {
          id: 3,
          title: '東京で丸一日遊ぶならこのコースがおすすめ',
          content: '',
          image: '',
          isPR: false
        },
        {
          id: 4,
          title: '京都で丸一日遊ぶならこのコースがおすすめ',
          content: '',
          image: '',
          isPR: false
        },
        {
          id: 5,          
          title: 'もやさまで訪れたまち〜吉祥寺編〜',
          content: '2019年もやもやさまぁ〜ずで訪問したお店を紹介します',
          image: '',
          isPR: true
        }
      ],
    }
  },
}

</script>
