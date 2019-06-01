<template>
  <v-layout
    column
    justify-center
    align-center
  >
        <v-autocomplete
          v-model="model"
          :items="prefectures"
          :label="`あそびばをさがす`"
        >
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
          >もっとみる(リンク先がストーリー投稿)</v-btn>
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
      model: null,
      items: [
        {
          id: 1,
          title: 'ストーリー投稿のタイトルを表示',
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
      prefectures: [
        '北海道',
        '青森県','岩手県','宮城県','秋田県','山形県','福島県',
        '茨城県','栃木県','群馬県','埼玉県','千葉県','東京都','神奈川県',
        '新潟県','富山県','石川県','福井県',
        '山梨県','長野県','岐阜県','静岡県','愛知県',
        '三重県','滋賀県','京都府','大阪府','兵庫県','奈良県','和歌山県',
        '鳥取県','島根県','岡山県','広島県','山口県',
        '徳島県','香川県','愛媛県','高知県',
        '福岡県','佐賀県','長崎県','熊本県','大分県','宮崎県','鹿児島県','沖縄県'
      ]
    }
  },
}
</script>
