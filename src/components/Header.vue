<template>
<div>
    <v-row class="header" justify="center">
        <v-col cols="2.5" align-self="center" class="title">
            <h2> {{ props.title }}</h2>
        </v-col>
        <v-col cols="4" offset="4" align-self="center" class="title">
            <h2> {{ props.version }}</h2>
        </v-col>
    </v-row>
</div>
</template>

<script setup>
const props = defineProps(['title', 'version']);

</script>

<script>
export default{
    name: "Header",
}
</script>
<style scoped>
.header{
    background-color: #8da9db !important;
    height: 105px;
}
.title{
    background-color: #2f5496;
    text-align: center;
    color: white !important;
    padding: 40px;
}
</style>