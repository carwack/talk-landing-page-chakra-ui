<template>
  <c-flex
    h="100vh"
    w="100vw"
    p="0 10%"
    flex-direction="column"
    justify-content="space-between"
  >
    <c-flex as="nav" justify-content="space-between">
      <c-heading as="h1" size="2xl" text-transform="uppercase">
        Bel-Vue
      </c-heading>
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
  name: 'App'
}
</script>
