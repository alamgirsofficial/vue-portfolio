<template>
    <section class="relative py-20 overflow-hidden" id="contact">
        <div class="relative z-10 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16"
            data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                Get In <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">
                    Touch</span>
            </h2>
            <p class="text-blue-200 text-lg">
                Let's work together on your next project.
            </p>
            </div>
            <div class="grid lg:grid-cols-2 gap-12">
                <!-- Conatct info  -->
                 <div data-aos="fade-right">
                    <h3 class="text-2xl font-bold text-white mb-6">
                        Contact Information
                    </h3>  
                <div class="space-y-6">
                    <div class="flex items-center gap-4">
                        <EnvelopeIcon class="w-6 h-6 text-cyan-400"/>
                    <div>
                        <p class="text-white font-semibold"> Email </p>
                        <p class="text-blue-200"> Alamgir@example.com </p>                        
                    </div>                    
                    </div>
                    <div class="flex items-center gap-4">
                        <PhoneIcon class="w-6 h-6 text-cyan-400"/>
                    <div>
                        <p class="text-white font-semibold"> Phone </p>
                        <p class="text-blue-200"> 0123456798 </p>                        
                    </div>                    
                    </div>
                    <div class="flex items-center gap-4">
                        <MapPinIcon class="w-6 h-6 text-cyan-400"/>
                    <div>
                        <p class="text-white font-semibold"> Location </p>
                        <p class="text-blue-200"> Chittagong </p>                        
                    </div>                    
                    </div>

                </div>
                <!-- Social Links  -->
                 <div class="mt-8">
                    <h4 class="text-lg font-bold text-white mb-4"> 
                        Follow Me
                    </h4>
                    <div class="flex gap-4">
                        <a href="#" class="p-3 bg-blue-500/20 border border-blue-400/30 rounded-xl text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <ChatBubbleLeftRightIcon class="size-5"/>
                        </a>
                        <a href="#" class="p-3 bg-cyan-500/20 border border-blue-400/30 rounded-xl text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <UserGroupIcon class="size-5"/>
                        </a>
                        <a href="#" class="p-3 bg-pink-500/20 border border-blue-400/30 rounded-xl text-blue-400
                        hover:bg-blue-500/30 transition-all">
                        <ShareIcon class="size-5"/>
                        </a>
                    </div>
                 </div>
                 </div>
                 
                 <!-- Conatct Form -->
                 <div data-aos="fade-left">
                     <form class="space-y-6">
                        <div class="grid sm:grid-cols-1 gap-2">

                            <div>
                                <label class="text-white text-sm font-extrabold mb-2 block">
                                    Name
                                </label>
                                <input type="text" class="w-full bg-gray-800/50 border
                                border-blue-500/30 rounded-xl px-4 py-3 focus:border-n=blue-400
                                focus:outline-none transition-all placeholder:text-blue-400 "
                                placeholder=" Name Here">
                            </div>
                            <div>
                                <label class="text-white text-sm font-medium mb-2 block">
                                    Email
                                </label>
                                <input type="email" class="w-full bg-gray-800/50 border
                                border-blue-500/30 rounded-xl px-4 py-3 focus:border-n=blue-400
                                focus:outline-none transition-all placeholder:text-blue-400 "
                                placeholder=" Email Here">
                            </div>
                            <div>
                                <label class="text-white text-sm font-medium mb-2 block">
                                    Subject
                                </label>
                                <input type="text" class="w-full bg-gray-800/50 border
                                border-blue-500/30 rounded-xl px-4 py-3 focus:border-n=blue-400
                                focus:outline-none transition-all placeholder:text-blue-400 " 
                                placeholder=" Subject Here">
                            </div>
                            <div>
                                <label class="text-white text-sm font-medium mb-2 block">
                                    Message
                                </label>
                                <textarea rows="6" class="w-full bg-gray-800/50 border
                                border-blue-500/30 rounded-xl px-4 py-3 focus:border-n=blue-400
                                focus:outline-none transition-all placeholder:text-blue-400 "
                                placeholder=" Write Message"></textarea>
                            </div>

                        </div>
                        <div>
                            <button type="submit" class="w-full bg-linear-to-r from-blue-500 to-cyan-500
                            text-white font-semibold py-3 rounded-xl hover:shadow-lg hover:shadow-blue-500/25
                             transition-all duration-300">
                             Send Message
                            </button>
                            
                        </div>
                        </form>

                 </div>

            </div>

        </div>

    </section>
</template>
<script setup>
import { 
    EnvelopeIcon,
    PhoneIcon,
    MapPinIcon, 
    ChatBubbleLeftRightIcon,
    UserGroupIcon,
    ShareIcon
} from '@heroicons/vue/16/solid';


</script>
