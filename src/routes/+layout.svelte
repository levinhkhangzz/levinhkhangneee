<script>
  import { onMount } from 'svelte';
  import Loading from './Loading.svelte';
  import '../app.css';

  let isLoading = true; // Bắt đầu với trạng thái loading là true

  // Hàm để tắt phần loading
  function hideLoading() {
    isLoading = false;
    console.log('Phần loading đã được tắt'); // Thêm log để kiểm tra xem hàm hideLoading có được gọi không
  }

  // Sử dụng onMount để thiết lập hẹn giờ
  onMount(() => {
    setTimeout(hideLoading, 1500); // Tắt phần loading sau 1.5 giây (1500ms)
  });
</script>

<svelte:head>
  <title>Le Vinh Khang – Web Developer</title>
  <meta
    name="description"
    content="I help companies build performant and scalable solutions for customer facing web apps"
  />
</svelte:head>

<main>
  {#if isLoading}
    <Loading /> <!-- Hiển thị phần loading khi isLoading là true -->
  {/if}

  <!-- Nội dung trang web -->
  <!-- Đây là nơi bạn đặt nội dung thực tế của trang web -->
  <div class="w-full pt-[20vh] pb-16">
    <div class="w-full px-4 max-w-md mx-auto text-center">
      <slot />
    </div>
  </div>
</main>
