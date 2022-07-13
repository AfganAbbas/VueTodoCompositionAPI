<template>
  <div>
    <input type="text" v-model="inp" @keydown.enter="emitAndClean" />
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  emits: ["addtolist"],
  setup(props, ctx) {
    const inp = ref("");

    const emitAndClean = () => {
      ctx.emit("addtolist", inp);
      inp.value = "";
    };

    return { inp, emitAndClean };
  },
};
</script>

<style></style>
