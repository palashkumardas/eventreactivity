<script setup>
import { ref,reactive } from 'vue'
const accordions=reactive([
    false,false,false,false
]);

function toggle(index){
    accordions[index]=!accordions[index]
}
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events & Reactivity in Vue.js</h1>
    
        <div class="p-10 bg-gradient-to-br from-pink-50 to-indigo-100 grid place-items-center">
          <div class="w-6/12 mx-auto rounded border">
            <div class="bg-white p-10 shadow-sm">
              <h3 class="text-lg font-medium text-gray-800">Several Windows stacked on each other</h3>
              <p class="text-sm font-light text-gray-600 my-3">
                The accordion is a graphical control element comprising a vertically stacked list of items such as labels or thumbnails
              </p>
    
              <div class="h-1 w-full mx-auto border-b my-5"></div>
    
              <!-- What is term -->
              <div class="transition hover:bg-indigo-50">
                <!-- header -->
                <div class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16" @click="toggle(0)">
                  <i class="fas fa-plus"></i>
                  <h3>Item one</h3>
                </div>
                <!-- Content -->
                <div class="px-5 pt-0 text-left pb-5" v-show="accordions[0]">
                  <p class="leading-6 font-light pl-9 ">
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sequi dolor dolorum odio, saepe quibusdam iusto possimus nesciunt dolores assumenda quae totam, doloremque odit. Itaque cum animi, labore debitis deserunt iusto!
                  </p>
                </div>
              </div>
    
              <!-- When to use Accordion Components -->
              <div class="transition hover:bg-indigo-50">
                <!-- header -->
                <div class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16" @click="toggle(1)">
                  <i class="fas fa-plus"></i>
                  <h3>Item two</h3>
                </div>
                <!-- Content -->
                <div class="accordion-content px-5 pt-0 text-left pb-5" v-show="accordions[1]">
                  <p class="leading-6 font-light pl-9 ">
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ut suscipit itaque, sequi incidunt ab sit optio debitis dignissimos doloribus ratione nobis id mollitia maiores eveniet necessitatibus dolorum praesentium! Corrupti, at.
                  </p>
                </div>
              </div>
    
              <!-- Accordion Wrapper -->
              <div class="transition hover:bg-indigo-50">
                <!-- header -->
                <div class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16" @click="toggle(2)">
                  <i class="fas fa-plus"></i>
                  <h3>Item three</h3>
                </div>
                <!-- Content -->
                <div class="accordion-content px-5 pt-0 text-left pb-5" v-show="accordions[2]">
                  <p class="leading-6 font-light pl-9">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima facilis labore voluptates provident nam, delectus suscipit nihil optio voluptate quae porro fugiat magni excepturi doloribus.
                  </p>
                </div>
              </div>
    
              <!-- Accordion Wrapper -->
              <div class="transition hover:bg-indigo-50">
                <!-- header -->
                <div class="accordion-header cursor-pointer transition flex space-x-5 px-5 items-center h-16" @click="toggle(3)">
                  <i class="fas fa-plus"></i>
                  <h3>Item four</h3>
                </div>
                <!-- Content -->
                <div class="accordion-content px-5 pt-0 text-left pb-5" v-show="accordions[3]">
                  <p class="leading-6 font-light pl-9">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ullam minima maiores magni dolore qui architecto pariatur incidunt repellat quos hic? Eius, eveniet accusantium! Quisquam, quo. Vitae ipsum ad veritatis commodi quasi expedita!
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>

<style scoped>

</style>
