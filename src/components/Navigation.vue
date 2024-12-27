<template>
    <div>
    <div class="wrapper">
        <div class="wrapper_left bg-[#1A1C33] w-[70px] h-[100vh] flex items-center flex-col p-2 absolute left-0 z-10">
            <img class="mb-[80px]" src="https://www.bootstrapget.com/demos/themeforest/unipro-admin-template/demos/02-design-dark/img/logo.svg" alt="">
            <div class=" wrap_icons flex flex-col items-start w-full" v-for="icon in icons" :key="icon.id">
                <i @click="activeClass = { [icon.id]: true }" class="fa-solid cursor-pointer py-5 transition-all duration-200 rounded-full hover:text-white w-full flex justify-center items-center" :class="icon.class + ' ' + (activeClass[icon.id] ? 'active' : '')"></i>
            </div>
        </div>
    </div>
    <div class="warpper_right w-[250px] h-[100vh] bg-[#1E203A] absolute left-[4.4rem]">
        <h1 class="p-4 my-[20px] text-[#B0B6D2] text-2xl">Pages</h1>
        <div class="flex items-start flex-col" v-for="item in items" :key="item.id">
            <a href="#" class="px-4 py-3 hover:bg-gray-600 inline-block w-full hover:text-white">{{ item.label }}</a>
        </div>
    </div> 
</div>
</template>

<script setup>
import { ref } from 'vue';

const activeClass = ref({})

const items = ref([
    {
        id: 1,
        label: 'Tasks'
    },
    {
        id: 2,
        label: 'Chat'
    },
    {
        id: 3,
        label: 'Create'
    },
    {
        id: 4,
        label: "View Invoice"        
    },
    {
        id: 5,
        label: 'Documents'
    },
    {
        id: 6,
        label: 'Faqs'
    },
    {
        id: 7,
        label: 'Pricing'
    },
    {
        id: 8,
        label: "Gallery"
    },
    {
        id: 9,
        label: "Icons"
    }
])

const icons = ref([
    {
        id: 1,
        class: 'fa-house'
    },
    {
        id: 2,
        class: 'fa-layer-group'
    },
    {
        id: 3,
        class: 'fa-book-open'
    },
    {
        id: 4,
        class: 'fa-pen-to-square'
    },
    {
        id: 5,
        class: 'fa-clone    '
    },
    {
        id: 6,
        class: 'fa-chart-pie'
    },
    {
        id: 7,
        class: 'fa-lock'
    }
])

</script>

<style scoped>

a {
    color: #79809A;
    transition: 0.4s ease-in-out;
    font-size: 14px;
}
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
i {
    color: #687CA2;
}
.active {
    background-color: #0ea5e9;
    color: white;
}
</style>