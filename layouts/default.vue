<template>
  <div class="container">
    <c-color-mode-provider>
      <c-box font-family="body" as="main">
        <c-reset />
        <nuxt />
      </c-box>
    </c-color-mode-provider>
  </div>
</template>
<script>

export default {
  name: 'App'
}
</script>
