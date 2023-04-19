<template>
<input :value="text" ref="myInput" />
<button @click="focusOnInput">Focus</button>
<button class="text-white rounded bg-pink-500 px-6 py-4 font-sans font-semibold shadow-lg hover:bg-pink-400 outline-none active:outline-none mt-5" @click="showModal = true">Open Modal</button>

<my-first-modal modalTitle="Sign Up for the GiveAway" modalContent="Grab Your ninja swag for half price" theme="sale" :show-modal="showModal" @updateShowModal="showModal = $event">
  <template v-slot:links>
        <a href="#" class="text-white rounded bg-green-500 px-4 py-2 font-sans font-semibold shadow-lg hover:bg-green-400 outline-none active:outline-none">Green Button</a>
        <a href="#" class="text-white rounded bg-red-500 px-4 py-2 font-sans font-semibold shadow-lg hover:bg-red-400 outline-none active:outline-none">Red Button</a>
    </template>
</my-first-modal>
</template>

  

<script>
import MyFirstModal from './components/MyFirstModal.vue';

export default {
    components: {
        MyFirstModal
    },
    methods: {
        focusOnInput() {
            this.$refs.myInput.focus();
        }
    },
    data() {
        return {
            showModal: false
        }
    }
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

input {
    border: 1px solid grey;
    margin-top: 1%;
}

button {
    border: 1px solid grey;

}
</style>
