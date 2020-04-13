<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/serfer.jpg')"
          class="my-3"
          contain
          height="1000"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to HolyWheelin'
        </h1>

        <p class="subheading font-weight-regular">
          由来：ボブディランの~~
          <br>please join our team
          <a
            href="https://www.asahi.com/"
            target="_blank"
          >Discord Community</a>
        </p>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          What's next?
        </h2>

        <v-row justify="center">
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          SNS
        </h2>

        <v-row justify="center">
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      importantLinks: [
        {
          text: 'twitter',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'facebook',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'instagram',
          href: 'https://madewithvuejs.com/vuetify',
        }
      ],
      whatsNext: [
        {
          text: '開催場所',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: '実績',
          href: 'https://vuetifyjs.com/layout/pre-defined',
        },
        {
          text: '次回予定',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>
