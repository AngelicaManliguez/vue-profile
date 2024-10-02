<template>

<div class="min-h-screen text-gray-200 mt-5">
    <h1 class="text-center text-3xl font-bold mb-3">ADMIN</h1>
    <table class="table-fixed border border-collapse border-yellow-700 w-full">
        <thead>
            <tr>
                <th class="text-center border border-yellow-700" colspan="2">Home Page</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="border border-yellow-700 text-center">
                    <div class="flex flex-col items-center justify-center text-center mt-2 mb-2">
                        <img alt="My pic" class="rounded-full outline-double outline-3 outline-offset-5 outline-yellow-600" src="@/assets/mypic.jpg" width="100" height="100" />
                        <nav class="flex text-sm text-gray-300 mt-3 space-x-2">
                            <p class="border-r border-gray-600 pr-2">Home</p>
                            <p class="border-r border-gray-600 pr-2">Profile</p>
                            <p>Certificate</p>
                        </nav>
                        
                        <h1 class="text-white text-2xl font-bold text-center mt-2">Angelica Manliguez</h1>
                        <p class="mt-2 text-gray-400 text-center">Aspiring Front-End Developer</p>
                    </div>
                </td>
                <td class="border border-yellow-700 text-center">
                    <button class="mr-2 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Edit</button>
                    <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Delete</button>
                </td>
            </tr>
        </tbody>



        <thead>
            <tr>
                <th class="text-center border-b border-yellow-700" colspan="2">Profile Page</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="border border-yellow-700">
                    <div class="flex flex-col text-yellow-500">
                        <div class="mt-2">
                            <h2 class="text-lg font-bold">📚 Education</h2>
                            <h3 class="text-sm mt-2 ml-3 font-semibold text-gray-300"> Bachelor of Science in Computer Science</h3>
                            <h3 class="text-sm ml-3 font-semibold text-gray-300 italic"> New Era University (2021 - 2014)</h3>
                            <p class="text-sm mt-2 ml-3 font-medium text-gray-300 border-b border-gray-600 pb-3">
                                🏅 Consistent President's Lister <br>
                                🏅 Tagis Lakas 2024 Womens Badminton Champion
                            </p>
                        </div>

                        <div class="mt-2">
                            <h2 class="text-lg font-bold">👩🏻 Know Me</h2>
                            <p class="text-sm mt-2 ml-4 font-semibold text-gray-300 border-b border-gray-600 pb-3">Aspiring Front-End Developer with a passion for creating intuitive user experiences. With a strong academic background and hands-on experience in software development, I am consistently recognized as a top-performing student. I am eager to apply my technical skills and creativity to help organizations build impactful and user-friendly digital solutions.</p>
                        </div>

                        <div class="mt-2">
                            <h2 class="text-lg font-bold mb-3">🔨 Languages and Tools</h2>
                            <div class="flex flex-wrap max-w-full ml-4 space-x-1 border-b border-gray-500 pb-3">
                                <img src="@/assets/vue.png" class="w-14 h-14"/>
                                <img src="@/assets/tail.png" class="w-14 h-14"/>
                                <img src="@/assets/php.png" class="w-14 h-14"/>
                                <img src="@/assets/js.png" class="w-14 h-14" />
                                <img src="@/assets/html.png" class="w-14 h-14"/>
                                <img src="@/assets/bootstrap.png" class="w-14 h-14"/>
                            </div>
                        </div>

                        <div class="mt-5">
                            <h2 class="text-lg font-bold">🖇️ Resume</h2>
                            <div class="flex flex-col mt-2">
                                <img class="w-2/6 h-auto ml-4" src="@/assets/resume.png"/>
                                <p class="text-sm mt-2 ml-4 font-semibold text-gray-300 pb-5">Check my resume for more info about me! </p>
                            </div>
                        </div>
                    </div>
                </td>
                <td class="border border-yellow-700 text-center">
                    <button class="mr-2 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Edit</button>
                    <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Delete</button>
                </td>
            </tr>
        </tbody>


        <thead>
            <tr>
                <th class="text-center border border-yellow-700" colspan="2">Certificate Page</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="border border-yellow-700">
                    <h2 class="text-lg font-bold mt-2 text-yellow-500">🎖 My Certificates</h2>
                    <div class="flex flex-wrap max-w-full mt-3">
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/AI.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/BA.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/DA.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/ITP.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/JS1.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/OCDM.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/OCI.png"/>
                    <img alt="cert" class="p-2 m-2 w-60 h-auto" src="@/assets/SQL.png"/>
                    </div>
                </td>
                <td class="border border-yellow-700 text-center">
                    <button class="mr-2 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Edit</button>
                    <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Delete</button>
                </td>
            </tr>
        </tbody>
    </table>
</div>
</template>
