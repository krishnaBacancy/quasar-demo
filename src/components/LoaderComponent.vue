<!-- <template>
  <div class="q-pa-md flex flex-center">
    <q-circular-progress
      show-value
      font-size="12px"
      :value="value"
      size="50px"
      :thickness="0.22"
      color="teal"
      track-color="grey-3"
      class="q-ma-md"
    >
      {{ value }}%
    </q-circular-progress>
  </div>
</template>

<script>
export default {
  setup() {
    return {
      value: 56,
    };
  },
};
</script> -->
<template>
  <div class="q-pa-md">
    <q-btn color="purple" @click="showLoading" label="Show Loading" />
  </div>
</template>

<script>
import useQuasar from "quasar/src/composables/use-quasar.js";
import { onBeforeUnmount } from "vue";

export default {
  setup() {
    const $q = useQuasar();
    let timer;

    onBeforeUnmount(() => {
      if (timer !== void 0) {
        clearTimeout(timer);
        $q.loading.hide();
      }
    });

    return {
      showLoading() {
        $q.loading.show();

        // hiding in 2s
        timer = setTimeout(() => {
          $q.loading.hide();
          timer = void 0;
        }, 2000);
      },
    };
  },
};
</script>
