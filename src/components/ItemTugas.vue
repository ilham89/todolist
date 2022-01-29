<template>
  <div>
    <input type="checkbox" :checked="tugasSaya.selesai" />

    <label
      class="form-check-label label"
      v-bind:class="{ 'item-completed': tugasSaya.selesai }"
      for="flexCheckDefault"
    >
      {{ tugasSaya.nama }}
    </label>
  </div>
</template>

<script>
export default {
  name: "ItemTugas",
  props: ["tugasSaya"],
};
</script>

<style scoped>
.input {
  width: 300px;
}
</style>
