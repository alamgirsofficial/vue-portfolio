<template>
    <section class="relative py-20 overflow-hidden" id="testimonial">
        <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- testimonial header  -->
            <div class="text-center mb-16"
            data-aos="fade-up" >
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4"
            data-aos="fade-up">
                Client <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">
                    Testimonial</span>
            </h2>
            <p class="text-blue-200 text-lg"> What People Say About Work with Me</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div v-for="(testimonial, index) in testimonials" :key="testimonial.id"
                class="bg-linear-to-br from-gray-800/50 to-blue-900/30
                rounded-2xl p-6 border border-blue-500/20 backdrop-blur-sm
                hover:border-blue-400 transition-all duration-300"
                data-aos="fade-up" data-aos-delay="index*100">
                <!-- Rating -->
                 <div class="flex gap-1 mb-4">
                    <StarIcon v-for="n in 5" :key="n" class="w-6 h-6 text-yellow-400" />
                 </div>
                 <!-- Testimonial text  -->
                  <p class="text-blue-100 text-sm leading-relaxed mb-6">
                    {{ testimonial.text }}
                  </p>

                  <!-- Client Info  -->
                  <div class="flex items-center  gap-4 ">
                    <div class="w-12 h-12 rounded-full overflow-hidden border-2 border-blue-400/50">
                        <img :src="testimonial.avatar" :alt="testimonial.name"
                        class="w-full h-full object-cover transition-transform duration-300 hover:scale-110">
                    </div>
                    <div>
                        <h4 class="text-lg font-semibold text-white mb-1">
                            {{ testimonial.name }}
                        </h4>
                        <p class="text-blue-200 text-sm">
                            {{ testimonial.position }}
                        </p>
                    </div>
                </div>


            </div>


        </div>
        </div>

    </section>
</template>
<script setup>

import { StarIcon } from '@heroicons/vue/16/solid';

import client1 from '../assets/testimonial/client1.png';
import client2 from '../assets/testimonial/client2.png';
import client3 from '../assets/testimonial/client3.png';
import client4 from '../assets/testimonial/client4.png';


const testimonials=[
    {
        id:1,
        text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, distinctio?",
        name:"John Doe",
        position:"CEO, TechCorp",
        avatar:client4
    },
    {
        id:2,
        text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, distinctio?",
        name:"Abraham Doe",
        position:"CEO, BMIT",
        avatar:client2
    },
    {
        id:3,
        text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, distinctio?",
        name:"Kilton Doe",
        position:"CEO, SME",
        avatar:client3
    },
    {
        id:4,
        text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi, distinctio?",
        name:"Suresh Doe",
        position:"CEO, ABC",
        avatar:client4
    }
]

</script>
