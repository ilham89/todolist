<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>Apa yang saya lakukan hari ini?</h2>
        </div>
      </div>

      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div
              v-for="tugasSaya in tugas"
              v-bind:key="tugasSaya.id"
              class="tugas mb-3 text-left"
            >
              <ItemTugas v-bind:tugasSaya="tugasSaya" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css";
import ItemTugas from "./components/ItemTugas.vue";
export default {
  name: "app",
  data: () => {
    return {
      tugas: [
        {
          id: 1,
          nama: "Menonton windah bocil kematian wikwika",
          selesai: true,
        },
        {
          id: 2,
          nama: "Belajar vue js",
          selesai: false,
        },
        {
          id: 3,
          nama: "Menjadi badutnya ~",
          selesai: false,
        },
      ],
    };
  },
  components: {
    ItemTugas,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.header {
  background: #1abc9c;
}
.label {
  margin-left: 16px;
}

.item-completed {
  color: #1abc9c;
}
</style>
