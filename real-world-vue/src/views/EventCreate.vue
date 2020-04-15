<template>
  <div>
    <h1>Create and Event, {{ user.name }}</h1>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength
    },
    ...mapGetters(['getEventById']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style lang="scss" scoped></style>
