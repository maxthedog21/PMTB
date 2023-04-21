<template>
  <div>
    <v-row class="header" style="margin: 0">
      <v-col cols="1" align-self="center" class="title">
        <img src="../assets/images/logo.png" alt="Title" class="title-image" />
      </v-col>
    </v-row>
  </div>
</template>

<script setup>
const props = defineProps(["title", "version"]);
</script>

<script>
export default {
  name: "Header",
};
</script>
<style scoped>
.header {
  background-image: linear-gradient(
    to right,
    #212121 20%,
    #212121 70%,
    #212121 80%,
    #212121 100%
  );
  /* box-shadow: 0px 6px 8px #00000040; */
}
.title {
  background-color: #212121;
  text-align: center;
  color: white !important;
  padding: 10px 10px 5px 10px;
}
.title .title-image {
  width: 170px; /* set the width of the image */
}
</style>
