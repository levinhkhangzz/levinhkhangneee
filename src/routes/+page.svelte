<!-- Trang Svelte -->
<script>
  import { onMount } from 'svelte';

  let isLoaded = false;

  // Sử dụng onMount để thực hiện việc xác định khi trang đã tải
  onMount(() => {
    isLoaded = true;
  });

  // Hàm xử lý khi hoàn thành hiệu ứng
  function onAnimationEnd() {
    // Ẩn phần tử gốc sau khi hiệu ứng hoàn thành (nếu cần)
  }
</script>

<style>
  /* Bắt đầu với opacity: 0 */
  .fade-in {
    opacity: 0;
  }
</style>

<!-- Sử dụng lớp animate__animated và animate__fadeIn để áp dụng hiệu ứng fade-in -->
<img
  src="/lars.jpg"
  alt="Le Vinh Khang"
  width="100"
  height="100"
  class="{isLoaded ? 'animate__animated animate__fadeIn fade-in' : 'fade-in'}"
  on:animationend={onAnimationEnd}
/>

<h1
  class="{isLoaded ? 'animate__animated animate__fadeIn fade-in' : 'fade-in'}"
  on:animationend={onAnimationEnd}
>
  Le Vinh Khang
</h1>
<h2
  class="{isLoaded ? 'animate__animated animate__fadeIn fade-in' : 'fade-in'}"
  on:animationend={onAnimationEnd}
>
  Web Developer
</h2>

<p
  class="{isLoaded ? 'animate__animated animate__fadeIn fade-in' : 'fade-in'}"
  on:animationend={onAnimationEnd}
>
  I help companies build performant and scalable solutions for customer facing web apps.
</p>

<!-- Sử dụng lớp fade-in và điều kiện isLoaded để áp dụng hiệu ứng fade-in -->
<ul class="flex font-medium text-slate-500 justify-center gap-6 {isLoaded ? 'animate__animated animate__fadeIn fade-in' : 'fade-in'}">
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
