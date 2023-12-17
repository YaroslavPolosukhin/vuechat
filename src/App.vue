<template>
  <ContainerElement>
    <ChatWindow>
      <ChatMessage username="Ivan" datetime="21.12.2019 05:00:50">Hello, World!!</ChatMessage>
    </ChatWindow>
  </ContainerElement>
</template>

<script>
  import {defineComponent} from "vue";
  import ContainerElement from "@/components/Container.vue";
  import ChatWindow from "@/components/ChatWindow.vue";
  import ChatMessage from "@/components/ChatMessage.vue";

  export default defineComponent({
    components: {ChatMessage, ChatWindow, ContainerElement}
  })

</script>

<style>
  body {
    margin: 0;
    background-color: #f9f9fa;
  }
</style>
