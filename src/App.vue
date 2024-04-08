<template>
  <h1>{{ title }}</h1>

<!--First Modal-->

 <teleport to=".modals" v-if="showModal">
  <modal  theme="sale" @close="toggleModal">
    <template v-slot:links>
      <a href="#">Sign up now</a>
      <a href="#">More info</a>
    </template>
    <h1>Ninja Giveaway</h1>
    <p>Grab your Ninja swag for half price </p>
  </modal>
 </teleport>

 <!--second modal-->

 <teleport  to=".modals" v-if="showModal2">
  <modal  theme="sale" @close="toggleModal2">
    <template v-slot:links>
      <a href="#">Get Coupon code</a>
      <a href="#">Buy course</a>
    </template>
    <h1>Udemy courses give away</h1>
    <p>Get your most wanted courses at give away prices</p>
  </modal>
 </teleport>

<!--End of second modal-->

 <button @click="toggleModal">open modal</button>
 <button @click="toggleModal2">open modal2</button>



 <!--practicing pull request -->

<div class="container">
  <h1>amune victor making pullrequest</h1>
</div>
</template>

<script>
import modal from './components/modal';

export default {
  name: 'App',
  components:{modal},
  data (){
    return {
      title: 'My first vue App',
     showModal: false,
     showModal2: false
    }
  },
  methods:{
    // handleclick (){
    //   console.log(this.$refs.name)
    //   this.$refs.name.classlist.add('active')
    //   this.$refs.name.focus()
    // },
    toggleModal (){
      this.showModal = !this.showModal
    },
    toggleModal2  (){
      this.showModal2 = !this.showModal2
    }
  }
}
</script>

<style>
#app, .modals{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button{
  outline: none;
  color:#333;
  border: 1px solid #333;
   margin: 10px;
   padding: 12px;
   background: none;
   border-radius:4px;
}
</style>
