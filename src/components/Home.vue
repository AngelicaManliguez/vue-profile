<script setup>
</script>

<template>
  <div class="flex flex-col items-center justify-center h-screen text-center">
            <a href="#"><img alt="My pic" class="rounded-full outline-double outline-4 outline-offset-8 outline-yellow-600" src="@/assets/mypic.jpg" width="300" height="300" /></a>
            <nav class="text-gray-300 mt-5 space-x-2">
                <RouterLink to="/" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out border-r border-gray-600 pr-2" active-class="text-yellow-600">Home</RouterLink>
                <RouterLink to="/profile" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out border-r border-gray-600 pr-2">Profile</RouterLink>
                <RouterLink to="/certificate" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out">Certificate</RouterLink>
            </nav>
            
            <h1 class="text-white text-4xl font-bold text-center mt-4">Angelica Manliguez</h1>
            <p class="mt-2 text-gray-400 text-center">Aspiring Front-End Developer</p>
    </div> 
</template>
