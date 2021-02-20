<template>
    <div class="card" style="width:200px">
    <div class="card-body">
      <h4 class="card-title">{{title}}--{{title.length}}</h4>
      <slot name="A"></slot> <!---Lo slot rappresenta il child di react all'interno dei componenti dichiarati altrove-->
      <slot name="B"></slot>
      <p class="card-text">{{description}}----<b>{{ colore }}</b></p>
      <button @click="card_button" class="btn btn-primary">See Profile</button>
    </div>
    <img class="card-img-bottom" src="https://www.w3schools.com/bootstrap4/img_avatar6.png" alt="Card image" style="width:100%">
  <br/>
  </div>
</template>

<script>
export default {
    name: 'Cards',
    data: () => ({
    //
  }),
  props:['title','description'],
  methods:{
      card_button: () =>{
          alert("this.title,3");
      }
  }
}
</script>


<style scoped> /*scoped serve solo localmente lo stile e non lo applica a tutta la pagina*/

</style>