<template>

  <MyFirstModal modalTitle="Sign Up for the GiveAway" modalContent="Grab Your ninja swag for half price">
    <template #links>
      <a href="#" class="text-white rounded bg-green-500 px-4 py-2 font-sans font-semibold shadow-lg hover:bg-green-400 outline-none active:outline-none">Green Button</a>
      <a href="#" class="text-white rounded bg-red-500 px-4 py-2 font-sans font-semibold shadow-lg hover:bg-red-400 outline-none active:outline-none">Red Button</a>
    </template>
  </MyFirstModal>

</template>


<script>
import MyFirstModal from './components/MyFirstModal.vue';

export default {
components: {
MyFirstModal
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
</style>
