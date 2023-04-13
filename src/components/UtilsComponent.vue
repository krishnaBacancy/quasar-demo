<template>
  <div id="utils">
    <span>Hello From Utils Component</span>
  </div>
</template>

<script>
import { ref, onMounted } from "vue";

import { dom, format, is } from "quasar";
const { capitalize } = format;
const { offset } = dom;

export default {
  setup() {
    console.log(capitalize("some text"));
    // const obj = 5;
    // console.log(is.object(obj));
  },
  mounted() {
    console.log(offset(document.getElementById("utils")));
  },
};
</script>
