<!-- Trang Svelte -->
<script>
  import { onMount } from 'svelte';

  let isLoaded = false;

  // Sử dụng onMount để thực hiện việc xác định khi trang đã tải
  onMount(() => {
    isLoaded = true;
  });
</script>

<style>
  /* Định dạng ban đầu với opacity: 0 và transition */
  .fade-in {
    opacity: 0;
    transition: opacity 1s ease-in-out;
  }

  /* Khi hiển thị, thay đổi opacity thành 1 */
  .fade-in.show {
    opacity: 1;
  }
</style>

<!-- Sử dụng lớp fade-in và điều kiện isLoaded để áp dụng hiệu ứng fade-in -->
<img
  src="/lars.jpg"
  alt="Le Vinh Khang"
  width="100"
  height="100"
  class="mask-squircle mx-auto block mb-18 {isLoaded ? 'fade-in show' : 'fade-in'}"
/>

<h1 class="font-semibold text-2xl mb-1 text-slate-900 {isLoaded ? 'fade-in show' : 'fade-in'}">Le Vinh Khang</h1>
<h2 class="font-medium text-slate-500 mb-8 {isLoaded ? 'fade-in show' : 'fade-in'}">Web Developer</h2>

<p class="font-medium mb-10 text-slate-800 text-lg {isLoaded ? 'fade-in show' : 'fade-in'}">
  I help companies build performant and scalable solutions for customer facing web apps.
</p>

<ul class="flex font-medium text-slate-500 justify-center gap-6 {isLoaded ? 'fade-in show' : 'fade-in'}">
  <li>
    <a href="https://twitter.com/aedotris" class="hover:underline underline-offset-4">X</a>
  </li>
  <li>
    <a href="https://www.facebook.com/profile.php?id=199717642" class="hover:underline underline-offset-4">Facebook</a>
  </li>
  <li>
    <a href="https://instagram.com/williamcachamwri" class="hover:underline underline-offset-4">Instagram</a>
  </li>
  <li>
    <a href="https://github.com/levinhkhangzz" class="hover:underline underline-offset-4">Github</a>
  </li>
</ul>
