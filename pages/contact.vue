<template>
  <v-layout>
    <v-flex class="text-center">
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :href="item.href"
          :target="item.target"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-twitter',
          title: 'twitter',
          href: 'https://twitter.com/ochibaapps',
          target: '_blank'
        }
      ]
    }
  }
}
</script>
