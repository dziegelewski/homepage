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

    h2 {
      font-size: 1.2em;
      margin: 1em 0 .5em;
    }
    
    article {
      display: flex;
      flex-direction: column;
      margin-bottom: 1em;
    }

    h3 {
      margin: .5em 0;
    }

    p {
      margin: 0 0 .5em;
    }

    a {
      margin-right: .5em;
    }
</style>
