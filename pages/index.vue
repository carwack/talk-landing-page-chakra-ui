<template>
  <c-flex
    v-bind="mainStyles[colorMode]"
    h="100vh"
    w="100vw"
    p="0 10%"
    flex-direction="column"
    justify-content="space-between"
    :bg-image="`url('/images/${bgs[colorMode].src}')`"
    bg-pos="center"
    bg-repeat="no-repeat"
    bg-size="cover"
    box-shadow="inset 0 0 0 2000px rgba(255, 255, 255, 0.4)"
    class="container"
    :class="colorMode"
  >
    <c-flex as="nav" justify-content="space-between">
      <c-heading as="h1" size="2xl" text-transform="uppercase">
        Bel-Vue
      </c-heading>

      <c-icon-button
        m="auto 0"
        bg="transparent"
        :icon="colorMode === 'light' ? 'moon' : 'sun'"
        :aria-label="`Switch to ${
          colorMode === 'light' ? 'dark' : 'light'
        } mode`"
        @click="toggleColorMode"
      />
    </c-flex>
    <c-box>
      <c-heading as="h1" size="xl" text-transform="uppercase" color="brand.1">
        Bel-Vue
      </c-heading>
      <c-heading
        as="h2"
        size="xl"
        text-transform="uppercase"
        font-weight="500"
      >
        The best Vue/View in Belgium.
      </c-heading>
      <c-text mt="20px">
        We're your local Vue.js User Group for Belgium, great to have you here 🙌 <br>
        We usually schedule meetups every quarter, with topics on anything related to Vue.js. <br>
        For more information checkout our
        <c-link
          href="https://www.meetup.com/vue-antwerp"
          color="brand.1"
          is-external
        >
          Meetup.com
        </c-link>
        page!
      </c-text>
    </c-box>
    <c-box as="footer">
      <c-text font-weight="light">
        Build by Sybren W. Powered by Chakra UI Vue.
      </c-text>
    </c-box>
  </c-flex>
</template>

<script lang="js">

export default {
  name: 'App',
  inject: ['$chakraColorMode', '$toggleColorMode'],
  data () {
    return {
      mainStyles: {
        dark: {
          bg: 'gray.700',
          color: 'whiteAlpha.900'
        },
        light: {
          bg: 'white',
          color: 'gray.900'
        }
      },
      bgs: {
        light: {
          src: 'zoe-gayah-jonker-IIs0z8QZO-s-unsplash.jpg',
          by: {
            name: 'Zoë Gayah Jonker',
            src: 'https://unsplash.com/@zoegayah?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText'
          },
          unsplash: 'https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText'
        },
        dark: {
          src: 'joran-quinten-_4SKRpyDLMI-unsplash.jpg',
          by: {
            name: 'Joran Quinten',
            src: 'https://unsplash.com/@joranquinten?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText'
          },
          unsplash: 'https://unsplash.com/photos/qlxnpyFmTS0?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText'
        }
      }
    }
  },
  computed: {
    colorMode () {
      return this.$chakraColorMode()
    },
    toggleColorMode () {
      return this.$toggleColorMode
    }
  }
}
</script>

<style scoped>
.container.dark {
  box-shadow:inset 0 0 0 2000px rgba(23, 25, 35, 0.4);
}
.container.light {
  box-shadow:inset 0 0 0 2000px rgba(255, 255, 255, 0.4);
}
a:hover {
  text-decoration: none;
}
</style>
