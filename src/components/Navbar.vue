<template>
    <div class="bg-gray-800 text-gray-100 py-3.5 px-6 shadow md:flex justify-between items-center ">
        <div class="flex items-center cursor-pointer">
            <span class="text-emerald-50 text-xl">
                <i class="bi bi-1-circle-fill "></i>                
            </span>

            <h1 class="text-xl pl-1.5">Desafío nivel 1</h1>

        </div>

        <span @click="MenuOpen()" class="absolute md:hidden right-10 top-10 cursor-pointer text-4xl z-40" >
            <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']" ></i>

        </span>

        <ul class="md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute bg-gray-800 md:w-auto w-full top-8 duration-700 ease-in pt-5" :class="[open ? 'left-0' : 'left-[-100%]']" >
            <li class="pl-1.5 md:mx-4 md:my-0 my-6" v-for="link in links">
                <a :href="link.link" @click="scrollToSection(link.link.substring(1))" class="text-xl" >{{link.name}}</a>
            </li>

            <!-- <Button>Get started</Button> -->
        </ul>
    </div>
</template>

<script>
import { ref, registerRuntimeCompiler } from "vue"
import Button from "./Button.vue"

export default{
    components:{
        Button
    },

    setup(){
        let open = ref()
        let links = [
            {name : "Inicio", link : "#inicio"},
            {name : "Contacto", link : "#contacto"},
        ]

        function MenuOpen(){
            open.value = !open.value
        }

        return {links, open, MenuOpen}
    }
}

const scrollToSection = (id) => {
  const section = document.getElementById(id);
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' });
  }
};

</script>