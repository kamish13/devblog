<template>
  <v-app-bar max-height="64">
    <div class="search d-flex allign-center justify-end ml-auto">
      <v-text-field
        v-model="search"
        hide-details="auto"
        dense
        placeholder="Search for a Post"
        prepend-icon="mdi-magnify"
        outlined
        :append-icon="search.length ? 'mdi-close' : ''"
        @click:append="clearField"
      >
      </v-text-field>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  name: 'TheNavigation',
  data: () => ({
    search: '',
  }),
  methods: {
    clearField() {
      this.search = ''
    },
  },
}
</script>

<style>
</style>