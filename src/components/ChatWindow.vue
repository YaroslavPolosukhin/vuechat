<template>
  <div class="chat-window">
    <div class="chat-messages">
      <div class="scroll-wrapper">
        <slot></slot>
      </div>
    </div>
    <div class="chat-send-panel">
      <input type="text" placeholder="Ваш никнейм..." class="chat-send-name-field" />
      <input type="text" placeholder="Сообщение..." class="chat-send-message-field"/>
      <button>
        <img src="/img/send.png"  alt="send"/>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChatWindow'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .chat-window {
    width: 100%;
    height: 100vh;
  }
  .chat-messages {
    width: 100%;
    background-color: #e9f3fa;
    background-image: url("/img/blue-snow.png");
    overflow: auto;
    height: calc(100vh - 60px);
    box-sizing: border-box;
  }
  .chat-messages .scroll-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-end;
    padding: 20px;
    min-height: calc(100vh - 60px);
    box-sizing: border-box;
  }
  .chat-send-panel {
    width: 100%;
    height: 60px;
    box-sizing: border-box;
    background-color: #dfe9f0;
    display: flex;
    padding: 5px;
    justify-content: space-between;
    align-items: center;
  }
  .chat-send-panel input,
  .chat-send-panel button {
    border-radius: 50px;
    color: #3a4158;
    font-size: 14px;
    border: 0;
  }
  .chat-send-panel input {
    border: 2px solid #bbb;
    padding: 10px 20px;
  }
  .chat-send-message-field {
    flex-grow: 1;
  }
  .chat-send-name-field {
    width: 100px;
    flex-grow: 0;
  }
  .chat-send-panel button {
    background-color: transparent;
    padding: 10px;
    cursor: pointer;
    transition: 0.2s;
  }
  .chat-send-panel button:active {
    transform: scale(0.9);
  }
  .chat-send-panel button img {
    width: 100%;
  }
</style>