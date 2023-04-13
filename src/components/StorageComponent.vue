<template>
  <q-btn
    color="purple"
    @click="setLocalStorageData('number', [1, 2])"
    label="Set LocalStorage"
  />
</template>

<script>
import { useQuasar } from "quasar";
export default {
  setup() {
    const $q = useQuasar();

    // $q.sessionStorage.set(key, value);
    // const otherValue = $q.sessionStorage.getItem(key);

    return {
      setLocalStorageData(key, val) {
        $q.localStorage.set(key, val);
        const value = $q.localStorage.getItem(key);

        window.localStorage.setItem("number1", 1);
        let val1 = window.localStorage.getItem("number1");

        console.log("value from local storage", val1, typeof val1);
        console.log(
          "value from local storage using quasar",
          value,
          typeof value
        );
      },
    };
  },
};
</script>
