<template>
  <div>
    <v-btn class="mt-10 mb-5" color="default" nuxt to="/timeline">
      Go to Timeline
    </v-btn>
    <v-spacer />

    <div class="display-3 text-center mt-5 mb-5">Pre-render fetch example</div>

    <v-card
      class="mx-auto mb-5"
      outlined
      v-for="item in posts.slice(1, 10)"
      :key="item.title"
    >
      <v-list-item three-line>
        <v-list-item-content>
          <div class="overline mb-4">Post</div>
          <v-list-item-title class="headline mb-1">{{
            item.title
          }}</v-list-item-title>
          <v-list-item-subtitle>{{ item.body }}</v-list-item-subtitle>
        </v-list-item-content>

        <!-- <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar> -->
      </v-list-item>

      <v-card-actions>
        <v-btn text>Like</v-btn>
        <v-btn text>Comment</v-btn>
      </v-card-actions>
    </v-card>

    <v-card class="mx-auto mb-5" outlined loading>
      <v-list-item three-line>
        <v-list-item-content>
          <div class="overline mb-4">OVERLINE</div>
          <v-list-item-title class="headline mb-1"
            >Headline 5</v-list-item-title
          >
          <v-list-item-subtitle
            >Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle
          >
        </v-list-item-content>

        <v-list-item-avatar tile size="80" color="grey"></v-list-item-avatar>
      </v-list-item>

      <v-card-actions>
        <v-btn text>Button</v-btn>
        <v-btn text>Button</v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>


<script>
export default {
  data() {
    return {
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
        },
        {
          name: 'Eclair',
          calories: 262,
        },
        {
          name: 'Cupcake',
          calories: 305,
        },
        {
          name: 'Gingerbread',
          calories: 356,
        },
        {
          name: 'Jelly bean',
          calories: 375,
        },
        {
          name: 'Lollipop',
          calories: 392,
        },
        {
          name: 'Honeycomb',
          calories: 408,
        },
        {
          name: 'Donut',
          calories: 452,
        },
        {
          name: 'KitKat',
          calories: 518,
        },
      ],
      posts: [],
    }
  },
  activated() {
    // Call fetch again if last fetch more than 30 sec ago
    if (this.$fetchState.timestamp <= Date.now() - 30000) {
      this.$fetch()
    }
  },
  async fetch() {
    this.posts = await fetch(
      'https://jsonplaceholder.typicode.com/posts'
    ).then((res) => res.json())
  },

  // call fetch only on client-side
  fetchOnServer: false,
}
</script>