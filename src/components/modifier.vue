import { reactive } from 'vue';
<script setup>
import {ref,reactive} from 'vue';
const message=ref("Hello Vue 3");
const space=ref(0);

function spacePressed(){
    space.value++
    message.value="Space pressed " + space.value + " times"
}
function whatPressed(event){
    message.value="You pressed " + event.key 
}
function clickButton(){
    message.value="You Clicked The Button" 
}
function ctrlRightClick(){
    message.value = "Ctrl+Right Click"
}
function divClick(){
    message.value ="Div click"
}
function buttonClick(){
    message.value ="Button click"
}
</script>

<template>
     <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events &amp; Reactivity in Vue.js</h1>
        <h2 class="mt-10">{{ message }}</h2>
        <form @submit.prevent=""  action="https://google.com/search">
            <div class="container mx-auto flex space-x-5 justify-center m-5"><input @keyup.space="spacePressed()" name="q" type="text" class="border border-gray-500 bg-white p-5" placeholder="Press Space"></div>
            <div class="container mx-auto flex space-x-5 justify-center m-5"><input @keyup="whatPressed($event)" name="text" type="text" class="border border-gray-500 bg-white p-5" placeholder="Type Something"></div>
            <button @click.prevent="clickButton()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"> Button </button>
            <button @click.ctrl="ctrlRightClick()" class="bg-blue-500 ml-5 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"> Ctrol + Right Click </button>
        </form>
        <div @click="divClick()" class="bg-gray-200 w-[500px] h-80 mt-5 flex items-center justify-center">
            <button @click.stop="buttonClick()" class="bg-orange-500 hover:bg-orange-700 text-white font-bold py-2 px-4 rounded"> Button </button></div>
    </section>
</template>


<style scoped>

</style>