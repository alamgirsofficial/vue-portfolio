<template>
    <footer class="relative bg-gray-900/80 border-t border-500/20">

        <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">

                <!-- Brands  -->
                 <div class="md:col-span-2">
                    <div class=" text-2xl font-bold bg-linear-to-r from-blue-400 to-cyan-400
                     bg-clip-text text-transparent mb-4">
                     Alamgir's Dev
                    </div>
                    <p class="text-blue-200 text-sm leading-relaxed max-w-md">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur, totam.
                    </p>
                    <div class="flex gap-4 mt-6 ">
                        <a href="#" class="p-2 bg-blue-500/20 border borded-blue-400/30 rounded-lg text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <EnvelopeIcon class="w-6 h-6 text-cyan-400"/>
                    </a>
                    <a href="#" class="p-2 bg-blue-500/20 border borded-blue-400/30 rounded-lg text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <MapPinIcon class="w-5 h-5"/>
                    </a>
                    <a href="#" class="p-2 bg-blue-500/20 border borded-blue-400/30 rounded-lg text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <PhoneIcon class="w-5 h-5"/>
                    </a>
                    </div>                    
                 </div>

                 <!-- QuickLinks  -->
                  <div>
                    <h3 class="text-white font-semibold mb-4"> 
                        Quick Links
                    </h3>
                    <ul class="space-y-2 lg:text-center">
                        <li v-for="link in quickLinks" :key="link.name">
                            <a :href="link.href" 
                            class="text-blue-200 hover:text-blue-400 text-sm  transition-colors duration-300">
                                {{ link.name }}  
                                </a>  
                        </li>
                    </ul>
                  </div>

                  <!-- Services  -->
                   <div>
                    <h3 class="text-white font-bold mb-4">
                        Services
                    </h3>
                    <ul class="space-y-2">
                        <li v-for="service in services" :key="service">
                            <a href="#" 
                            class="text-blue-200 hover:text-blue-400 text-sm transition-colors"> 
                                {{ service }}
                            </a>
                        </li>
                    </ul>
                   </div>
            </div>
            <!-- Bottom Bar -->
             <div class="border-t border-blue-500/20 mt-8 pt-8 flex flex-col md:flex-row justify-between transition-colors">
                <p class="text-blue-300 text-sm">
                    @2023 Alamgir's Dev. All rights reserved
                </p>
                <div class="flex gap-6 mt-4 md:mt-0">
                    <a href="#" Class="text-blue-400 text-sm transition-colors"> Privacy Policy</a>
                    <a href="#" Class="text-blue-400 text-sm transition-colors"> Terms of Services</a>
                </div>
             </div>
        </div>
    </footer>
</template>
<script setup>
import { 
    EnvelopeIcon, 
    PhoneIcon, 
    MapPinIcon
 } from '@heroicons/vue/16/solid';

 const quickLinks =[
    {name:'Home', href:'#home'},
    {name:'About', href:'#about'},
    {name:'Skills', href:'#skills'},
    {name:'Services', href:'#services'},
    {name:'Projects', href:'#projects'},
    {name:'Contact', href:'#contact'},
    {name:'testimonials', href:'#testimonial'},
 ]

 const services =[
    "Web Development",
    "Technical Writing",
    "Content Writing",
    "Digital Marketing",
    "UI/UX Design",
    "consultation"
 ]

</script>
<style>
    
</style>