<template>
<div>
    <button class="text-white rounded bg-pink-500 px-6 py-4 font-sans font-semibold shadow-lg hover:bg-pink-400 outline-none active:outline-none mt-5" @click="toggleModal = true">Open Modal</button>
    <div class="fixed overflow-x-hidden overflow-y-auto inset-0 flex justify-center items-center z-50" v-if="toggleModal">
        <div class="absolute inset-0 bg-black opacity-25" @click.self="toggleModal = false"></div>
        <div class="relative mx-auto w-auto max-w-2xl">
            <div class="bg-white rounded shadow-xl w-96 h-56 flex flex-col">
                <div class="text-sky-500 text-2xl font-bold px-4 py-6">{{ modalTitle }}</div>
                <span>{{ modalContent }}</span>
                <div class="mt-4">
                    <slot name="links">
                    </slot>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

    
<script>
export default {
    name: "MyfirstModal",
    props: {
        modalTitle: {
            type: String,
            required: true
        },
        modalContent: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            toggleModal: false
        };
    }
};
</script>
