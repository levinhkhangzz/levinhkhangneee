<!-- 404/+layout.svelte -->
<script context="module">
  // Nếu bạn cố gắng xuất `default` từ đây, hãy đổi thành tên khác
  // Ví dụ: export { Layout as CustomLayout };
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
