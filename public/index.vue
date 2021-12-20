<template>
  <v-container fluid>
    <!-- <div class="intro mt-5 mb-8">
      <h1 class="text-h1">Automation Blog</h1>
      <h2 class="text mt-2">Automate boring stuff</h2>
    </div> -->

    <v-row class="posts-container mt-5">
      <v-col cols="12">
        <div class="filter">
          <v-select
            v-model="category"
            style="width: 200px"
            outlined
            dense
            hide-details="auto"
            :items="['all', 'investing', 'crypto', 'automation']"
          />
        </div>
      </v-col>

      <v-col v-for="post in 4" :key="post" cols="12" md="6">
        <v-card elevation="0">
          <v-card-title>My First Blog Post</v-card-title>
          <v-card-text
            >Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus
            id, vero ratione provident amet odit sed molestias cupiditate
            praesentium inventore eum obcaecati harum dolore est eveniet quo
            nisi iure sit?
          </v-card-text>
          <v-card-action>
            <v-btn text to="/1">Read More</v-btn>
          </v-card-action>
        </v-card>
      </v-col>
    </v-row>
    <v-row class="post-pagination">
      <v-col class="text-right" cols="12">
        <v-btn>
          <v-icon small> mdi-arrow-left</v-icon>
        </v-btn>
        <v-btn>
          <v-icon small> mdi-arrow-right</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HomePage',
  layout: 'DefaultLayout',
  data: () => ({
    category: 'all',
  }),
}
</script>

<style>
</style> 
