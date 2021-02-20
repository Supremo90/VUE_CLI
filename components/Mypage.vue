<template>
    <div style="text-align:center">
        <h1>Primo comando</h1>
        <p>{{ a }}</p>
        <button @click="a = 'Rosso'">CAMBIA COLORE</button>
    </div>
</template>

<script>
export default {
    name: 'Mypage',
    data: () => ({
    a: 'Bianco'
  }),
}
</script>


<style scoped> /*scoped serve solo localmente lo stile e non lo applica a tutta la pagina*/
div{border: 1px solid blue;}
</style>