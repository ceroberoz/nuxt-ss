<template>
  <div class="text-input-section">
    <div class="mac-window">
      <div class="mac-title-bar">
        <div class="mac-buttons">
          <button class="mac-button close-button"></button>
          <button class="mac-button minimize-button"></button>
          <button class="mac-button maximize-button"></button>
        </div>
        <!-- Your title bar content here -->
      </div>
      <div class="mac-content">
        <textarea class="mac-textarea" ref="textarea" @input="adjustTextareaSize"></textarea>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    adjustTextareaSize() {
      this.$nextTick(() => {
        const textarea = this.$refs.textarea;
        textarea.style.width = 'auto'; // Reset the width first
        textarea.style.height = 'auto'; // Reset the height first
        textarea.style.width = `${textarea.scrollWidth}px`; // Set the width based on content
        textarea.style.height = `${textarea.scrollHeight}px`; // Set the height based on content
      });
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hack:wght@400;700&display=swap');

.mac-window {
  width: 800px;
  background-color: #f6f6f6;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
  border-radius: 8px;
  margin: 0 auto; /* Center horizontally */
  
}

.mac-title-bar {
  background-color: #f0f0f0;
  padding: 8px;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
  grid-column: 1 / span 3; /* Span across all 3 columns */
  display: flex;
  align-items: center;
}

.mac-buttons {
  display: flex;
  gap: 4px;
}

.mac-button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.close-button {
  background-color: #ff5f56;
}

.minimize-button {
  background-color: #ffbd2e;
}

.maximize-button {
  background-color: #28c940;
}

.mac-content {
  padding: 16px;
  display: flex;
  justify-content: flex-start; /* Left-align content */
}

.mac-textarea {
  width: 100%;
  padding: 8px;
  border: none;
  resize: none;
  font-family: 'Hack', monospace;
  font-size: 14px;
  background-color: transparent;
  color: #333333;

  min-height: 10em;
}
</style>