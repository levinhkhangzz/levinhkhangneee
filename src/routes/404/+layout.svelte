<!-- 404/+layout.svelte -->
<script context="module">
  export { default } from '$layout';
</script>

<main>
  <slot></slot>
</main>

<style>
  main {
    text-align: center;
    padding: 2em;
  }
</style>
