<script setup>
</script>

<template>
    <header>
        <div class="flex flex-col items-center justify-center text-center mt-6">
            <a href="#"><img alt="My pic" class="rounded-full outline-double outline-4 outline-offset-8 outline-yellow-600" src="@/assets/mypic.jpg" width="200" height="200" /></a>
            <nav class="text-gray-300 mt-5 space-x-2">
                <RouterLink to="/" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out border-r border-gray-600 pr-2">Home</RouterLink>
                <RouterLink to="/profile" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out border-r border-gray-600 pr-2" exact-active-class="text-yellow-600">Profile</RouterLink>
                <RouterLink to="/certificate" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out border-r border-gray-600 pr-2" exact-active-class="text-yellow-600">Certificate</RouterLink>
                <RouterLink to="/admin" class="hover:text-yellow-600 transition-colors duration-200 ease-in-out" exact-active-class="text-yellow-600">Admin</RouterLink>
            </nav>

            <h1 class="text-white text-4xl font-bold text-center mt-4">Angelica Manliguez</h1>
            <p class="mt-2 text-gray-400 text-center">Aspiring Front-End Developer</p>
        </div> 
    </header>
</template>