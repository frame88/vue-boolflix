<template>
  <header>
    <div class="container-fluid d-flex justify-content-between">
      <img src="../assets/logo.png" class="logo" alt="">
      <div class="ricerca">
        <input class="myinput" type="text" v-model="textSearch" @keyup.enter="sendSearch()" placeholder="Cerca film o serie tv">
        <button @click="sendSearch()" class="btn btn-outline-light">Cerca</button>
      </div>
  </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    data(){
        return{
            textSearch:'',
        };
    },
    methods: {
        sendSearch(){
            console.log(this.textSearch);
            this.$emit('emitSearch', this.textSearch);
        },
    },
}
</script>

<style lang="scss">
  header{
    padding: 20px;
    background-color: black;
    .logo{
      margin-left: 60px;
      width: 150px;
    }
    .myinput{
      height: 40px;
      align-self: center;
      border: none;
      padding-left: 15px;
      padding-top: 0;
      background-color: #141414;
      color: grey;
    }
    .ricerca{
      display: flex;
      margin-right: 60px;
      align-items: center;
    }
  }
</style>