<template>
  <v-flex>
    <v-date-picker
      v-model="picker"
      full-width
      type="month"
      no-title
      locale="ja"
      class="v-card--outlined"
      show-current="false"
    ></v-date-picker>
  </v-flex>
</template>

<script>
export default {
  computed: {
    picker: {
      get() {
        return this.$store.getters.getCurrentMonth
      },
      set(value) {
        this.$store.commit('setCurrentMonth', value)
      }
    }
  }
}
</script>
