<template>
  <button class="btn btn-danger align-self-center mb-4" @click="addNote()">
    Add a New Note
  </button>
  <div class="board d-flex justify-content-center flex-row flex-wrap">
    <div class="note d-flex flex-column" v-for="note in notes" :key="note">
      <button
        class="btn-sm btn-danger remove align-self-end"
        @click="removeNote(index)"
      >
        x
      </button>
      <textarea
        class="bg-transparent align-self-center"
        cols="30"
        rows="10"
      ></textarea>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notes: ["note"],
    };
  },
  methods: {
    removeNote(index) {
      console.log("silindi");
      this.notes.splice(index, 1);
    },
    addNote() {
      this.notes.push("note");
      console.log("eklendi");
    },

  },
};
</script>
