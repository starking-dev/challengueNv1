<template class="" >

    <div id="" class="w-full max-h-full bg-teal-200 content-between flex flex-col">

       <Navbar/>

    <!-- Sección de Inicio -->
    <section id="inicio" class="flex-grow flex items-center justify-center p-8 bg-sky-800 text-white shadow-lg rounded-b-xl mb-8">
      <div class="text-center max-w-2xl">
        <h1 class="text-5xl md:text-6xl font-extrabold mb-4 animate-fadeIn">Bienvenido al inicio</h1>
        <p class="text-lg md:text-xl pt-2.5 opacity-80 animate-fadeIn delay-200">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui sapiente porro sint! Ducimus vero cum repudiandae, amet distinctio dicta nobis provident, ea deserunt voluptatem in, facilis minus consequatur ut ipsum.
        </p>
      </div>
    </section> 
    <br><br><br>
    
    <!-- Sección de Contacto -->
    <section id="contacto" class="w-full mx-auto p-8 my-8 bg-sky-800 shadow-lg rounded-xl mb-8">
      <h2 class="text-3xl font-bold text-white text-center mb-6">Contáctenos</h2>
      <p class="text-center text-white mb-8">
        Envíanos un mensaje y ponte en contacto.
      </p>
      <form class="max-w-md mx-auto space-y-4">
        <div>
          <label for="name" class="block text-sm font-medium text-white">Nombre Completo</label>
          <input type="text" id="name" name="name" class="text-black bg-teal-200 mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 p-2">
        </div>
        <div>
          <label for="email" class="block text-sm font-medium text-white">Correo Electrónico</label>
          <input type="email" id="email" name="email" class="text-black bg-teal-200 mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 p-2">
        </div>
        <div>
          <label for="message" class="block text-sm font-medium text-white">Mensaje</label>
          <textarea id="message" name="message" rows="4" class="text-black bg-teal-200 mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500 p-2"></textarea>
        </div>
        <div class="text-center pt-3 ">
          <button type="submit" class="w-full inline-flex justify-center py-2 px-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-black bg-teal-200 hover:bg-teal-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 transition-colors duration-300">
            Enviar
          </button>
        </div>
      </form>
    </section>  
    
    <AddElements/>    

    <!-- Pie de página -->
    <footer class="bg-gray-800 text-white text-center p-4 mt-auto -xl">
      <p class="text-sm opacity-70">
        © {{ new Date().getFullYear() }} Prueba De Nivelación 
      </p>
    </footer>

    </div>

</template>

<script>
import Navbar from "./components/Navbar.vue"
import AddElements from "./components/AddElements.vue"


export default {
  name: "App",
  components: {
    Navbar, AddElements,
  },
};

</script>

<style>

</style>