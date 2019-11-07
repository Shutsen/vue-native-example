<template>
  <nb-header>
    <nb-left>
      <nb-button :onPress="toggleSidebar" transparent>
        <nb-icon name="menu" />
      </nb-button>
    </nb-left>
    <nb-body>
      <nb-title>{{ title }}</nb-title>
    </nb-body>
    <nb-right />
  </nb-header>
</template>

<script>
export default {
  props: ['title'],
  methods: {
    toggleSidebar() {
      this.$emit('toggle')
    }
  }
}
</script>