<template>

<div class="min-h-screen text-gray-200 mt-5">
    <h1 class="text-center text-3xl font-bold mb-3">ADMIN</h1>
    <table class="table-fixed">
        <thead>
            <tr>
                <th class="text-center text-black p-2 bg-amber-400 bg-opacity-90" colspan="2">Home Page</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="data in homeInfo" :key="data.id">
                <td class="w-2/3 text-center">
                    <div class="flex flex-col items-center justify-center text-center my-4">
                        <img alt="My pic" class="rounded-full outline-double outline-3 outline-offset-5 outline-yellow-600" src="@/assets/mypic.jpg" width="100" height="100" />
                        <nav class="flex text-sm text-gray-300 mt-3 space-x-2">
                            <p class="border-r border-gray-600 pr-2">{{data.nav1}}</p>
                            <p class="border-r border-gray-600 pr-2">{{data.nav2}}</p>
                            <p>{{data.nav3}}</p>
                        </nav>
                        
                        <h1 class="text-white text-2xl font-bold text-center mt-2">{{data.name}}</h1>
                        <p class="mt-2 text-gray-400 text-center">{{data.description}}</p>
                    </div>
                </td>
                <td class="text-center bg-neutral-800">
                    <div class="space-x-2 mt-3">
                        <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="getData(data.id)">Edit</button>
                    </div>
                    
                    <div class="flex flex-col items-center my-3 mx-5">
                        <input type="text" class="text-black border border-zinc-900 px-2 w- x" v-model="nav1">nav1</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="nav2">nav2</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="nav3">nav3</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="name">name</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="description">description</input>
                    </div> 
                    <button class="-mt-2 mb-3 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="saveData(haveID)">Update</button>
                </td>
            </tr>
        </tbody>



        <thead>
            <tr>
                <th class="text-center text-black p-2 bg-amber-400 bg-opacity-90" colspan="2">Profile Page</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="data in profileInfo" :key="data.id">
                <td>
                    <div class="flex flex-col text-yellow-500">
                        <div class="mt-2">
                            <h2 class="text-lg font-bold">{{data.head}}</h2>
                            <h3 class="text-sm mt-2 ml-3 font-semibold text-gray-300"> {{data.desc1}}</h3>
                            <h3 class="text-sm ml-3 font-semibold text-gray-300 italic"> {{data.desc2}}</h3>
                            <p class="text-sm mt-2 ml-3 font-medium text-gray-300 border-b border-gray-600 pb-3">
                                {{data.desc3}}<br>
                                {{data.desc4}}
                            </p>
                        </div>

                        <div class="mt-2">
                            <h2 class="text-lg font-bold">{{data.head2}}</h2>
                            <p class="text-sm mt-2 ml-4 font-semibold text-gray-300 border-b border-gray-600 pb-3">{{data.desc5}}</p>
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
                <td class="text-center bg-neutral-800">
                    <div class="space-x-2 mt-3">
                        <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="getData(data.id)">Edit</button>
                    </div>
                    
                    <div class="flex flex-col items-center my-3 mx-5">
                        <input type="text" class="text-black border border-zinc-900 px-2 w- x" v-model="head">head</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="desc1">desc1</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="desc2">desc2</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="desc3">desc3</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="desc4">desc4</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="head2">head2</input>
                        <input type="text" class="text-black border border-gray-500 px-2" v-model="desc5">desc5</input>
                    </div> 
                    <button class="-mt-2 mb-3 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="saveData(haveID)">Update</button>
                </td>
            </tr>
        </tbody>


        <thead>
            <tr>
                <th class="text-center text-black p-2 bg-amber-400 bg-opacity-90" colspan="2">Certificate Page</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <h2 class="text-lg text-center font-bold mt-2 text-yellow-500">🎖 My Certificates</h2>
                    <div class="flex flex-wrap max-w-full">
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/AI.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/BA.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/DA.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/ITP.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/JS1.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/OCDM.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/OCI.png"/>
                    <img alt="cert" class="m-2 w-60 h-auto" src="@/assets/SQL.png"/>
                    </div>
                </td>
                <td class="text-center bg-neutral-800">
                    <button class="mr-2 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Edit</button>
                    <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out">Delete</button>
                </td>
            </tr>
        </tbody>
    </table>
</div>
</template>

<script>
    export default{
        data(){
            return{
                //pic: '',
                nav1: '',
                nav2: '',
                nav3: '',
                name: '',
                description: '',
                haveID: null,
                
                homeInfo: [
                    {
                    id: 1,
                    //pic: '<img alt="My pic" class="rounded-full outline-double outline-3 outline-offset-5 outline-yellow-600" src="@/assets/mypic.jpg" width="100" height="100" />',
                    nav1: 'Home',
                    nav2: 'Profile',
                    nav3: 'Certificate',
                    name: 'Angelica Manliguez',
                    description: 'Aspiring Front-End Developer'
                    },
                ],
                
                profileInfo: [
                    {
                    id: 2,
                    head: '📚 Education',
                    desc1: 'Bachelor of Science in Computer Science',
                    desc2: 'New Era University (2021 - 2014)',
                    desc3: "🏅 Consistent President's Lister",
                    desc4: '🏅 Tagis Lakas 2024 Womens Badminton Champion',
                    head2: '👩🏻 Know Me',
                    desc5: 'Aspiring Front-End Developer with a passion for creating intuitive user experiences. With a strong academic background and hands-on experience in software development, I am consistently recognized as a top-performing student. I am eager to apply my technical skills and creativity to help organizations build impactful and user-friendly digital solutions.',
    
                    },
                ]
            }
        },
        methods: {
            getData(id) {
                this.haveID = id;
                if (id === 1) {
                    var data = this.homeInfo.filter((data) => data.id === id);
                    this.nav1 = data[0].nav1;
                    this.nav2 = data[0].nav2;
                    this.nav3 = data[0].nav3;
                    this.name = data[0].name;
                    this.description = data[0].description;
                } else if (id === 2) {
                    var data = this.profileInfo.filter((data) => data.id === id);
                    this.head = data[0].head;
                    this.desc1 = data[0].desc1;
                    this.desc2 = data[0].desc2;
                    this.desc3 = data[0].desc3;
                    this.desc4 = data[0].desc4;
                    this.head2 = data[0].head2;
                    this.desc5 = data[0].desc5;
                }
            },
            saveData(haveID) {
                if (haveID === 1) {
                    var data = this.homeInfo.filter((data) => data.id === haveID);
                    data[0].nav1 = this.nav1;
                    data[0].nav2 = this.nav2;
                    data[0].nav3 = this.nav3;
                    data[0].name = this.name;
                    data[0].description = this.description;
                } else if (haveID === 2) {
                    var data = this.profileInfo.filter((data) => data.id === haveID);
                    data[0].head = this.head;
                    data[0].desc1 = this.desc1;
                    data[0].desc2 = this.desc2;
                    data[0].desc3 = this.desc3;
                    data[0].desc4 = this.desc4;
                    data[0].head2= this.head2;
                    data[0].desc5 = this.desc5;
                }
                    }
        }
    }
</script>