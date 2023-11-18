<!-- layout.svelte -->
<script>
  export let error;
</script>

<script>
  import '../app.css';
</script>

<svelte:head>
  <title>Le Vinh Khang – Web Developer</title>
  <meta
    name="description"
    content="In the quiet realm of a coder's life, the symphony of keystrokes orchestrates a world of innovation and endless possibilities."
  />
</svelte:head>

<main>
  {#if error}
    <404 {error} />
  {:else}
    <div class="w-full pt-[20vh] pb-16">
      <div class="w-full px-4 max-w-md mx-auto text-center">
        <slot></slot>
      </div>
    </div>
  {/if}
</main>

<style>
  main {
    text-align: center;
    padding: 2em;
  }
</style>
