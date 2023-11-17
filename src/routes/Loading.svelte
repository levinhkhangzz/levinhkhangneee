<!-- Loading.svelte -->
<style>
  /* CSS cho phần loading */
  .loading {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7); /* Màu nền của phần loading */
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999; /* Để hiển thị trên tất cả các phần tử khác */
  }

  .spinner {
    border: 4px solid rgba(255, 255, 255, 0.3); /* Màu của vòng tròn loading */
    border-top: 4px solid #ffffff; /* Màu của vòng tròn loading */
    border-radius: 50%;
    width: 50px;
    height: 50px;
    animation: spin 2s linear infinite; /* Tạo hiệu ứng quay vòng tròn */
  }

  @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }
</style>

<div class="loading">
  <div class="spinner"></div>
</div>
