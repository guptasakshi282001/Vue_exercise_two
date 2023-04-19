<template>
<div>
    <div class="fixed overflow-x-hidden overflow-y-auto inset-0 flex justify-center items-center z-50" v-if="showModal">
        <div class="absolute inset-0 bg-black opacity-25" @click.self="closeModal"></div>
        <div class="relative mx-auto w-auto max-w-2xl">
            <div class="bg-white rounded shadow-xl w-96 h-56 flex flex-col">
                <div class="text-sky-500 text-2xl font-bold px-4 py-6" v-bind:class="{'text-red-500': theme === 'sale'}">{{ modalTitle }}</div>
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
    name: "MyFirstModal",
    props: {
        modalTitle: {
            type: String,
            required: true
        },
        modalContent: {
            type: String,
            required: true
        },
        showModal: {
            type: Boolean,
            required: true,
            default: false
        },
        theme: {
            type:String,
            default : "",
        },
    },
    methods: {
        closeModal() {
            this.$emit('updateShowModal', false);
        }
    }
};
</script>
