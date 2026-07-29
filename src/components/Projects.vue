<template>
    <section class="relative py-20 overflow-hidden" id="projects">
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Section Header  -->
             <div class="text-center mb-16 "
             data-aos="fade-up">
             <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                My <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400"> 
                    Projects</span>
             </h2>
             <p class="text-blue-200 text-lg max-w-2xl mx-auto">
                 A Collection of my recent work and Creative Solutions
             </p>
             </div>
             <!-- Section Header End  -->
              <!-- Project Grid  -->
               <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

                <div v-for="(project,index) in projects" :key="project.id"
                    class="group relative bg-linear-to-br from-gray-800/50 to-blue-900/30
                    rounded-3xl overflow-hidden border backdrop-blur-sm border-blue-400/40 
                    transition-all duration-300 hover:transform hover:-translate-y-2"
                    :class="project.bordColor"
                    data-aos="fade-up"
                    :data-aos-delay="(index+1)*100">
                    <div class="relative overflow-hidden">
                        <img :src="project.image" :alt="project.title"
                        class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500"> 
                        <div class="absolute inset-0 bg-linear-to-t from-gray-900/90 via-transparent to-transparent">
                            </div>
                            <div class="absolute top-4 right-4">
                                <span class="px-3 py-1 text-white text-xs rounded-full font-semibold"
                                :class="project.bordColor">
                                {{ project.category }}
                                </span>
                            </div>
                    </div>
                    <!-- project content  -->
                    <div class="p-6">
                        <h3 class="text-lg font-bold text-white mb-2 group-hover:text-blue-400
                        transition-colors duration-300">
                            {{ project.title }}
                        </h3>
                        <p class="text-blue-100 text-sm leading-relaxed mb-4">
                            {{ project.desc }}
                        </p>
                        <!-- technology -->
                         <div class="flex flex-wrap gap-2 mb-4">
                            <span v-for="tech in project.technology" :key="tech"
                            class="px-2 py-1 border rounded text-xs"
                            :class="tech.class">
                            {{ tech.name}}
                            </span>
                         </div>
                         <!-- technology end  -->
                          <!-- Project links  -->
                           <div class="flex gap-3">
                            <a v-for="link in project.links" :key="link.name"
                            :href="link.url"
                            :class="link.class"
                            class="flex items-center gap-2 transition-colors duration-300
                             text-sm font-medium">
                            <component :is="link.icon" class="w-5 h-5" /> {{ link.name }}</a>
                           </div>
                           <!-- Project links end  -->                           
                    </div>                    
                </div>
                </div>
                <!-- CTA section  -->
                 <div class="text-center mt-16" data-aos="fade-up">
                    <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
                        <button type="button" class="px-8 py-4 rounded-xl bg-linear-to-r from-blue-500 to-cyan-500
                        text-white font-semibold hover:shadow-lg hover:shadow-blue-500/25 transition-all
                        duration-300 hover:scale-105 flex items-center">
                        View All Projects 
                        <ArrowRightIcon class="w-6 h-6 ml-2"/>
                        </button>
                        <button type="button" class="px-8 py-4 rounded-xl border border-blue-400
                        text-white font-semibold hover:shadow-lg hover:shadow-blue-500/25 transition-all
                        duration-300 hover:scale-105 flex items-center">
                        Discuss Project
                        <ChatBubbleLeftRightIcon class="w-6 h-6 ml-2"/>
                        </button>

                    </div>

                 </div>

        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';

import image1 from '../assets/project/project1.png';
import image2 from '../assets/project/project2.png';
import image3 from '../assets/project/project3.png';
import image4 from '../assets/project/project4.png';
import image5 from '../assets/project/project5.png';
import image6 from '../assets/project/project6.png';

import { 
    EyeIcon,
    CodeBracketIcon,
    ArrowRightIcon,
    ChatBubbleLeftRightIcon
 } from '@heroicons/vue/16/solid';


const projects = ref([
    {
        id:1,
        title:'Project 1',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image1,
        category:'Category 1',
        bordColor:'border-blue-500/20',
        technology:[
            {
                name:'Vue JS',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Laravel',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
            {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    },
    {
        id:2,
        title:'Project 2',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image2,
        category:'Category 2',
        bordColor:'border-cyan-500/20',
        technology:[
            {
                name:'Technology 1',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Technology 2',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
           {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    },
    {
        id:3,
        title:'Project 3',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image3,
        category:'Category 3',
        bordColor:'border-blue-500/20',
        technology:[
            {
                name:'Technology 1',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Technology 2',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
            {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    },
    {
        id:4,
        title:'Project 4',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image4,
        category:'Category 4',
        bordColor:'border-cyan-500/20',
        technology:[
            {
                name:'Technology 1',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Technology 2',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
            {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },            
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    },
    {
        id:5,
        title:'Project 5',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image5,
        category:'Category 5',
        bordColor:'border-blue-500/20',
        technology:[
            {
                name:'Technology 1',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Technology 2',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
            {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    },
    {
        id:6,
        title:'Project 6',
        desc:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, quos.',
        image:image6,
        category:'Category 6',
        bordColor:'border-cyan-500/20',
        technology:[
            {
                name:'Technology 1',
                class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
            },
            {
                name:'Technology 2',
                class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
            }
        ],
        links:[ 
            {
                name:'Live Demo',
                url:'#',
                icon:EyeIcon,
                class:'text-blue-400 hover:text-blue-500',                
            },
            {
                name:'Code',
                url:'#',
                icon:CodeBracketIcon,
                class:'text-cyan-400 hover:text-cyan-500',
            }
        ]
    }
                            
]);

</script>
<style>
    
</style>