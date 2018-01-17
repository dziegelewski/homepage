<template>
  <main>
    <Section
      v-for="section in sections"
      :key="section.id"
      :title="section.title"
      :children="section.children"
    />
  </main>
</template>

<script>

import Section from './Section.vue';
import sections from './sections';

export default {
  name: 'Main',
  components: {
    Section
  },
  data() {
    return {
      sections
    }
  }
}
</script>

<style lang="scss">
    main {
      max-width: 500px;
      margin: 1em auto;
      font-size: 1.4em;
      padding: 0 1em;
    }
</style>
