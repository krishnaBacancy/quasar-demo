<template>
  <q-page class="flex flex-center">
    <!-- <Loader /> -->
    <!-- <ChatMessage /> -->
    <!-- <Editor /> -->
    <!-- <Storage /> -->
    <Utils />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import Loader from "../components/LoaderComponent.vue";
import ChatMessage from "../components/ChatMessages.vue";
import Editor from "../components/EditorComponent.vue";
import Storage from "../components/StorageComponent.vue";
import Utils from "../components/UtilsComponent.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    // Loader,
    // ChatMessage,
    // Editor,
    // Storage,
    Utils,
  },
});
</script>
