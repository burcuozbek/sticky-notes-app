<template>
  <div class="container d-flex justify-content-center flex-column">
    <h3 class="d-flex justify-content-center align-items-center mt-5 mb-3">
      Sticky Notes
    </h3>

    <NoteBoard />
  </div>
</template>
<script>
import NoteBoard from "@/components/NoteBoard.vue";

export default {
  data() {
    return { notes: ["note"] };
  },
  components: {
    NoteBoard,
  },
};
</script>
