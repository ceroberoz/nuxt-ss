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
        <!-- Your content here -->
        <MonacoEditor lang="typescript" :options="{ minimap: {enabled: false}, lineNumbers: 'off'}" />
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Hack:wght@400;700&display=swap');

.mac-window {
  width: 80vw;
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
  justify-content: flex-start;
  /* Add any necessary styles for the content inside mac-window */
}
</style>