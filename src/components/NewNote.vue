<template>
  <div class="new-note">
    <label>Title</label>
   <input v-model="note.title" type="text">
   <label>Description</label>
  <textarea v-model="note.descr"></textarea>
  <button class="btn btnPrimary" @click="addNote">New Note</button>
        </div>
</template>

<script>
export default {
  props: {
    note: {
      type:Object,
      required:true
    }
  },
  methods: {
    addNote () {
      this.$emit("addNote",this.note)
    }
  }
}
</script>

<style lans="scss ">
.new-note {
  text-align: center;
}
.btn {
  margin-top: 30px;
}

</style>