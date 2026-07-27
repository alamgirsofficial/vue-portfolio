<template>
    <section class=" relative py-20 overflow-hidden" id="services">
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center m-16" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    My <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400
                    to-cyan-400"> Services
                    </span>
                </h2>
                <p class="text-blue-200 text-lg max-w-2xl mx-auto" 
                data-aos="fade-up" data-aos-delay="100">
                    These are the services I provide to my clients </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="group relative p-8 rounded-2xl bg-linear-to-br from-gray-800/50 
                to-blue-900/30 backdrop-blur-sm border border-blue-500/20 hover:border-blue-400/40
                transition-all duration-500 hover:transform hover:-translate-y-2 "
                v-for="(service, index) in services" :key="service.id"
                :data-aos="fade-up" :data-aos-delay="(index*100)+200"> 

                <div class="absolute inset-0 bg-linear-to-r from-blue-500/5
                   to-cyan-500/5 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                </div>
                <div class=" relative z-10 mb-6">
                    <div class="inline-flex items-center justify-center w-16 h-16 rounded-xl bg-linear-to-r
                    from-blue-500/20 to-cyan-500/20 border border-blue-400/30 group-hover:scale-110 
                    transition-transform duration-300">
                    <component :is="service.icon" class="w-8 h-8 text-blue-400">
                    </component>
                    </div>
                </div>
                <div class="relative z-10"> 
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-blue-400
                    transition-colors duration-300">
                        {{ service.name }}
                    </h3>
                    <p class="text-blue-100 leading-relaxed"> {{ service.desc }}</p>
                </div>
                <div class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 transform 
                translate-x-4 group-hover:translate-x-0 transition-all duration-300">

                <ArrowRightIcon class="w-6 h-6 text-blue-400"></ArrowRightIcon>
                </div>
                </div> 
            </div>
            <div class="text-center mt-16"
            data-aos="fade-up" data-aos-delay="800">
            <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
                <button type="button" class="px-8 py-4 rounded-xl border border-blue-400 text-blue-400
                font-semibold hover:bg-blue-400/10 hover:text-white transition-all duration-300 flex items-center">
                Get In Touch 
                <ChatBubbleLeftRightIcon class="w-6 h-6 ml-2"></ChatBubbleLeftRightIcon>
                </button> 
            </div>

            </div>

        </div>

    </section>
</template>
<script setup>
import {ref} from 'vue';

import { 
    ArrowRightIcon,
    ChatBubbleLeftRightIcon,
    CodeBracketIcon, 
    ComputerDesktopIcon, 
    DevicePhoneMobileIcon, 
    DocumentTextIcon, 
    EnvelopeIcon, 
    GlobeAltIcon 
} from '@heroicons/vue/24/outline';

const services= ref([
    {
        id:1,
        icon:CodeBracketIcon,
        name:'Web Development',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    },
    {
        id:2,
        icon:ComputerDesktopIcon,
        name:'Technical Writing',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    },
    {
        id:3,
        icon:DevicePhoneMobileIcon,
        name:'Mobile Development',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    },
    {
        id:4,
        icon:DocumentTextIcon,
        name:'Email Marketing',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    },
    {
        id:5,
        icon:EnvelopeIcon,
        name:'UI/UX Design',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    },
    {
        id:6,
        icon:GlobeAltIcon,
        name:'Web Design',
        desc:`Lorem ipsum dolor sit amet consectetur adipisicing elit.`
    }
]);
</script>
<style lang="">
    
</style>