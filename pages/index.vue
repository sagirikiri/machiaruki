<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <v-card
        v-for="item in items"
        v-bind:key="item.id"
      >
        <v-card-title class="headline">{{ item.title }}</v-card-title>
        <v-card-text>
          <p> {{ item.content }}</p>
          <img src= '' alt="横浜">
        </v-card-text>
        <v-card-actions>
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
          title: 'ストーリー投稿のタイトルが表示される',
          content: 'ストーリー投稿の最初のコンテンツの内容がここに表示される',
          image: '~/static/macchanrio.png'
        },
        {
          title: '横浜',
          content: '',
          image: '',
          isPR: 'false'
        },
        {
          title: '東京で丸一日遊ぶならこのコースがおすすめ',
          content: '',
          image: '',
          isPR: 'false'
        },
        {
          title: '東京で丸一日遊ぶならこのコースがおすすめ',
          content: '',
          image: '',
          isPR: 'false'
        },
        {
          title: 'もやさまで訪れたまち〜吉祥寺編〜',
          content: '2019年もやもやさまぁ〜ずで訪問したお店を紹介します',
          image: '',
          isPR: 'true'
        }
      ],
    }
  },
}

</script>
