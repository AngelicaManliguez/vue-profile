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
                            <img src="@/assets/mypic.jpg" alt="My pic" class="rounded-full outline-double outline-3 outline-offset-5 outline-yellow-600" width="100" height="100" />
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
                        <div class="flex flex-col items-center my-3 mx-5">
                            <input type="text" id="nav1" class="text-black border border-zinc-900 px-2 my-1 w-80 rounded" v-model="nav1" placeholder="nav1"/>
                            <input type="text" id="nav2" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="nav2" placeholder="nav2"/>
                            <input type="text" id="nav3" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="nav3" placeholder="nav3"/>
                            <input type="text" id="name" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="name" placeholder="name"/>
                            <input type="text" id="description" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="description" placeholder="description"/>
                        </div> 

                        <div class="space-x-2 mt-3">
                            <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="getData(data.id, 'home')">Edit</button>
                            <button class="-mt-2 mb-3 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="saveData('home')">Update</button>
                        </div>
                        
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
                                <h2 class="text-lg font-bold mb-3">{{data.head3}}</h2>
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
                                <h2 class="text-lg font-bold">{{data.head4}}</h2>
                                <div class="flex flex-col mt-2">
                                    <img class="w-2/6 h-auto ml-4" src="@/assets/resume.png"/>
                                    <p class="text-sm mt-2 ml-4 font-semibold text-gray-300 pb-5">{{data.desc6}}</p>
                                </div>
                            </div>
                        </div>
                    </td>
                    <td class="text-center bg-neutral-800">
                        <div class="flex flex-col items-center my-3 mx-5">
                            <input type="text" class="text-black border border-zinc-900 px-2 my-1 w-80 rounded" v-model="head" placeholder="head">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc1" placeholder="desc1">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc2" placeholder="desc2">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc3" placeholder="desc3">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc4" placeholder="desc4">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="head2" placeholder="head2">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc5" placeholder="desc5">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="head3" placeholder="head3">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="head4" placeholder="head4">
                            <input type="text" class="text-black border border-gray-500 px-2 my-1 w-80 rounded" v-model="desc6" placeholder="desc6">
                        </div> 
                        <div class="space-x-2 mt-3">
                            <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="getData(data.id, 'profile')">Edit</button>
                            <button class="-mt-2 mb-3 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="saveData('profile')">Update</button>
                        </div>
                    </td>
                </tr>
            </tbody>

            <thead>
                <tr>
                    <th class="text-center text-black p-2 bg-amber-400 bg-opacity-90" colspan="2">Certificate Page</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="data in certificateInfo" :key="data.id">
                    <td>
                        <h2 class="text-lg text-center font-bold mt-2 text-yellow-500">{{data.head5}}</h2>
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
                        <div class="flex flex-col items-center my-3 mx-5">
                            <input type="text" class="text-black border border-zinc-900 px-2 my-1 w-80 rounded" v-model="head5" placeholder="head5">
                        </div> 
                        <div class="space-x-2 mt-3">
                            <button class="bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="getData(data.id, 'certificate')">Edit</button>
                            <button class="-mt-2 mb-3 bg-yellow-600 rounded-xl px-6 py-2 hover:bg-yellow-800 duration-200 ease-in-out" @click="saveData('certificate')">Update</button>
                        </div>
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
                homeID: null,
                
                homeInfo: [
                    {
                        id: 1,
                        //pic: '<img alt="My pic" class="rounded-full outline-double outline-3 outline-offset-5 outline-yellow-600" src="@/assets/mypic.jpg" width="100" height="100" />',
                        nav1: 'Home',
                        nav2: 'Profile',
                        nav3: 'Certificate',
                        name: 'Angelica Manliguez',
                        description: 'Aspiring Front-End Developer'
                    }
                ],
                
                head: '',
                desc1: '',
                desc2: '',
                desc3: '',
                desc4: '',
                head2: '',
                desc5: '',
                head3: '',
                head4: '',
                desc6: '',
                profileID: null,

                profileInfo: [
                    {
                        id: 1,
                        head: '📚 Education',
                        desc1: 'Bachelor of Science in Computer Science',
                        desc2: 'New Era University (2021 - 2014)',
                        desc3: "🏅 Consistent President's Lister",
                        desc4: '🏅 Tagis Lakas 2024 Womens Badminton Champion',
                        head2: '👩🏻 Know Me',
                        desc5: 'Aspiring Front-End Developer with a passion for creating intuitive user experiences. With a strong academic background and hands-on experience in software development, I am consistently recognized as a top-performing student. I am eager to apply my technical skills and creativity to help organizations build impactful and user-friendly digital solutions.',
                        head3: '🔨 Languages and Tools',
                        head4: '🖇️ Resume',
                        desc6: 'Check my resume for more info about me! 🎖 My Certificates'
                    }
                ],

                head: '',
                certificateInfo: [
                    {
                        id: 1,
                        head5: '🎖 My Certificates'
                    }
                ]
            };
        },
        methods: {
            getData(id, type) {
                if (type === 'home') {
                    this.homeID = id;
                    const data = this.homeInfo.find(item => item.id === id);
                    if (data) {
                        this.nav1 = data.nav1;
                        this.nav2 = data.nav2;
                        this.nav3 = data.nav3;
                        this.name = data.name;
                        this.description = data.description;
                    }
                    
                } else if (type === 'profile') {
                    this.profileID = id;
                    const data = this.profileInfo.find(item => item.id === id);
                    if (data) {
                        this.head = data.head;
                        this.desc1 = data.desc1;
                        this.desc2 = data.desc2;
                        this.desc3 = data.desc3;
                        this.desc4 = data.desc4;
                        this.head2 = data.head2;
                        this.desc5 = data.desc5;
                        this.head3 = data.head3;
                        this.head4 = data.head4;
                        this.desc6 = data.desc6;
                    }
                }else if (type === 'certificate') {
                    this.certificateID = id;
                    const data = this.certificateInfo.find(item => item.id === id);
                    if (data) {
                        this.head5 = data.head5;
                    }
                    
                }
            },
            saveData(type) 
            {
                if (type === 'home' && this.homeID !== null) {
                    const index = this.homeInfo.findIndex(item => item.id === this.homeID);
                    if (index !== -1) {
                        this.homeInfo[index] = {
                            id: this.homeID,
                            nav1: this.nav1,
                            nav2: this.nav2,
                            nav3: this.nav3,
                            name: this.name,
                            description: this.description
                        };
                    }
                }else if (type === 'profile' && this.profileID !== null) {
                    const index = this.profileInfo.findIndex(item => item.id === this.profileID);
                    if (index !== -1) {
                        this.profileInfo[index] = {
                            id: this.profileID,
                            head: this.head,
                            desc1: this.desc1,
                            desc2: this.desc2,
                            desc3: this.desc3,
                            desc4: this.desc4,
                            head2: this.head2,
                            desc5: this.desc5,
                            head3: this.head3,
                            head4: this.head4,
                            desc6: this.desc6
                        };
                    }
                }else if (type === 'certificate' && this.certificateID !== null) {
                    const index = this.certificateInfo.findIndex(item => item.id === this.certificateID);
                    if (index !== -1) {
                        this.certificateInfo[index] = {
                            id: this.certificateID,
                            head5: this.head5
                        };
                    }
                }
            }
        }
    }
</script>