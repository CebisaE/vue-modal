<template>
<h1>{{title}}</h1>
<p>have a look at our promotion</p>
<teleport to='.modals' v-if="showModal">
<modal theme="promotion" @close="toggleModal">
  <template v-slot:links>
    <a href="#">register</a>
    <a href="#">find out more</a></template>
<h1>emihle cebisa</h1>
<p>come get your 50% discount now whilst stock lasts!!!</p>
</modal>
</teleport>
<teleport to=".modals" v-if="showModalTwo">
  <modal @close="toggleModalTwo">
    <h1>register for promotions</h1>
    <p>do not mis out of promotions promo codes!</p>
    </modal>
    </teleport>
<button @click="toggleModal">info</button>
&nbsp;
<button @click="toggleModalTwo">register</button>
</template>
<script>
import modal from "./components/modal.vue";

export default {
name: 'App',
components:{
  modal
},
  data() {
    return {
      title: `emihle cebisa`,
      header:'sign up to win a prize now!!!',
      text:'come get your 50% discount now whilst stock lasts!!!',
      showModal: false,
      showModalTwo:false
    }
  },
  methods:{
    toggleModal(){
      this.showModal = !this.showModal;
    },
    toggleModalTwo(){
    this.showModalTwo=!this.showModalTwo;
    }
  }
}
</script>

<style>
#App{
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialised;
  -moz-osx-font-smoothing: grayscale;
  text-align:center;
  color: #2c3e50;
  margin-top:60px;
}
</style>