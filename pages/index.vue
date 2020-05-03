<template>
  <v-card class="mx-auto">
    <v-card-title class="headline">
      Works
    </v-card-title>
    <v-container fluid>
      <v-row dense>
        <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
          <v-card :href="card.href" :target="card.target" link>
            <v-img
              :src="card.src"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title v-text="card.title"></v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    cards: [
      {
        title: '趣味を押し付けるまとめ',
        src: '/icon_org.png',
        flex: 12,
        href: 'https://oshitsuke.ochibaapps.com',
        target: '_blank'
      },
      {
        title: '工事中',
        src: '/icon_org.png',
        flex: 6,
        href: '',
        target: ''
      },
      {
        title: '工事中',
        src: '/icon_org.png',
        flex: 6,
        href: '',
        target: ''
      }
    ]
  })
}
</script>
