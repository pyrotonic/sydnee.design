<template>
  <component :is="component" class="typography">
    <slot />
  </component>
</template>

<script lang="ts">
  import Vue from 'vue'
  import Component from 'vue-class-component'
  import { Prop } from 'vue-property-decorator'

  @Component
  export default class Typography extends Vue {
    @Prop({ type: String, default: 'span' }) component!: string
  }
</script>

<style>
  .typography {
    font-size: calc(1rem);
  }

  h1.typography {
    font-size: calc(3rem);
  }
  h2.typography {
    font-size: calc(2.25rem);
  }
  h3.typography {
    font-size: calc(1.5rem);
  }
  h4.typography {
    font-size: calc(1.25rem);
  }
  h5.typography {
    font-size: calc(1rem);
  }
  h6.typography {
    font-size: calc(0.875rem);
  }
</style>
