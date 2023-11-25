<template>
  <div class="index-page">
    <!-- Your page content here -->
    <footer class="footer">
      <p class="footer-text">Footer text</p>
    </footer>
  </div>
</template>

<style scoped>
.index-page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.footer {
  background-color: #f6f6f6;
  padding: 16px;
  text-align: center;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
}

.footer-text {
  color: black;
}
</style>