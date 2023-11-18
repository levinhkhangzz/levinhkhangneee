<!-- 404.svelte -->
<script>
  export let error;
</script>

<main>
  <h1>Trang không tồn tại</h1>
  <p>{error.message}</p>
</main>

<style>
  main {
    text-align: center;
    padding: 2em;
  }
</style>
