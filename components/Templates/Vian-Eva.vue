<template>
    <div class="font-poppins">
        <guest-modal v-show="SpecialInvited" v-bind="GuestInvited"/>
        
        <!-- Music Button -->
        <div class="fixed z-50 bottom-5 right-5">
            <button class="py-2 px-4 bg-gray-100" unelevated :icon="PlayingAudio ? 'music_off' : 'music_note'" @click.prevent="PlayingAudio ? pauseMusic(FileAudio) : playMusic(FileAudio) "></button>
        </div>

        <!-- Headline Section -->
        <div class="relative">
            <img src="~/assets/img/16436960169351.webp" class="w-full hidden md:block h-screen object-cover" alt="Vian & Eva">
            <img src="~/assets/img/cover-mobile.webp" class="w-full block md:hidden h-screen object-cover" alt="Vian & Eva">
            <div class="absolute mt-10 md:mt-0 top-36 md:top-72 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-white text-center">
                <div class="text-lg font-light">The Wedding Of</div>
                <div class="font-qwigley text-8xl lg:text-8xl">Eva <br> & <br> Vian</div>
                <div class="text-lg font-light">27 . 03 . 2022</div>
            </div>
        </div>

        <!-- Magic Words -->
        <div class="px-5 lg:px-48 py-10 lg:py-24">
            <div class="flex text-center">
                <div class="w-36 lg:w-40">
                    <img src="~/assets/img/Left-Flower.png">
                </div>
                <p class="text-xs lg:text-base mt-5 font-light italic px-3">TUHAN Allah berfirman: "Tidak baik, kalau manusia itu seorang diri saja. Aku akan menjadikan penolong baginya, yang sepadan dengan dia."</p>
                <div class="w-40 lg:w-52">
                    <img src="~/assets/img/Right-Flower.png">
                </div>
            </div>
            <div class="text-center lg:mt-0">
                <p>Kejadian 2:18</p>
            </div>
        </div>

        <!-- Bride & Groom -->
        <div class="flex px-5 lg:px-60 py-5">
            <div class="w-full lg:flex justify-between lg:justify-around flex-row space-y-10 lg:space-y-0">
            <div data-aos="fade-right" data-aos-duration="1500" class="flex flex-col w-full lg:w-52 space-y-5">
                <img src="~/assets/img/Bride.png" alt="Bride" class="w-32 lg:w-full mx-auto ">
                <div class="text-center space-y-2">
                <p class="font-medium">Eva Oktaviana</p>
                <p class="text-xs lg:text-sm font-light">Putri Kedua Bapak Nasirudin & Ibu Rusmina Simbolon</p>
                </div>
            </div>

            <div data-aos="fade-left" data-aos-duration="1500" class="flex flex-col w-full md:w-52 space-y-5">
                <img src="~/assets/img/Groom.png" alt="Groom" class="w-32 lg:w-full mx-auto">
                <div class="text-center space-y-2">
                <p class="font-medium">Charisma Vian Geslianto </p>
                <p class="text-xs lg:text-sm font-light">Putra Pertama Alm Bapak Paidi & Ibu Yutini Soleka</p>
                </div>
            </div>

            </div>
        </div>

        <!-- Save The Dates -->
        <div class="relative text-white py-10 lg:py-20">
            <img src="~/assets/img/Awan.png" alt="Awan" class="lg:w-full hidden h-96 object-cover">
            <img src="~/assets/img/Awan2.png" alt="Awan" class="w-full h-96 lg:hidden">
            <div class="absolute top-60 lg:top-60 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-center">
                <div class="font-light text-sm">SAVE THE DAY</div>
                <div class="text-4xl lg:text-7xl font-qwigley">27 Maret 2022</div>
                    <!-- <vue-countdown :time="TheDate" :interval="100" v-slot="{ days, hours, minutes, seconds }">
                        <div class="grid grid-cols-2 lg:grid-cols-4 gap-10 lg:space-x-5 mt-5 lg:mt-10">

                            <div class="flex flex-col text-center">
                                <div class="text-4xl lg:text-6xl">{{ days }}</div>
                                <div class="text-xs font-light">Hari</div>
                            </div>
                            <div class="flex flex-col text-center">
                                <div class="text-4xl lg:text-6xl">{{hours}}</div>
                                <div class="text-xs font-light">Jam</div>
                            </div>
                            <div class="flex flex-col text-center">
                                <div class="text-4xl lg:text-6xl">{{minutes}}</div>
                                <div class="text-xs font-light">Menit</div>
                            </div>
                            <div class="flex flex-col text-center">
                                <div class="text-4xl lg:text-6xl">{{seconds}}</div>
                                <div class="text-xs font-light">Detik</div>
                            </div>
                        </div>
                    </vue-countdown> -->
            </div>
        </div>

        <!-- Event -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-x-0 gap-y-10 lg:gap-0 lg:gap-x-20 px-5 lg:px-60 py-10">
            <div class="h-max flex flex-col px-4 lg:px-6 py-4 lg:py-6 border text-center rounded-lg">
                <p class="font-qwigley text-5xl">Pemberkatan</p>
                <div class="mt-7 space-y-3 text-base">
                    <p>-- 27 Maret 2022 --</p>
                    <p>Pukul 09:00 - 11.00</p>
                </div>
                <div class="mt-10 space-y-2">
                    <p class="font-semibold font-ubuntu text-base">Gereja Masehi Advent Hari Ketujuh Jemaat Salatiga</p>
                    <p class="font-light text-sm">Jl. Hasanudin No.100, Dukuh, Kec. Sidomukti, Kota Salatiga, Jawa Tengah 50724</p>
                </div>
                <div class="flex justify-center mt-20">
                    <a href="https://maps.app.goo.gl/RKjWjSjrwMzW5dYn6">
                        <div class="w-max px-5 py-2 rounded-md bg-black text-white">Buka Lokasi</div>
                    </a>
                </div>
            </div>

            <div class="flex flex-col px-4 py-4 lg:px-6 lg:py-6 border text-center rounded-lg">
            <p class="font-qwigley text-5xl">Resepsi</p>
            <div class="mt-7 space-y-3 text-base">
                <p>-- 27 Maret 2022 --</p>
                <p class="font-semibold">Sesi 1</p>
                <p>Pukul 12:00 - 13.00</p>
                <p class="font-semibold">Sesi 2</p>
                <p>Pukul 13:00 - 14.00</p>
            </div>
            <div class="mt-10 space-y-2">
                <p class="font-semibold font-ubuntu text-base">Joglo Ki Penjawi</p>
                <p class="font-light text-sm">Jl. Ki Penjawi No.14, Sidorejo Lor, Kec. Sidorejo, Kota Salatiga, Jawa Tengah 50714</p>
            </div>
            <div class="flex justify-center mt-20">
                <a href="https://maps.app.goo.gl/quqSdroLEcsq8Gax5">
                    <div class="w-max px-5 py-2 rounded-md bg-black text-white">Buka Lokasi</div>
                </a>
            </div>
            </div>

        </div>

        <!-- Stories -->
        <div class="px-5 lg:px-52 py-10 lg:py-20">
            <div class="text-center px-5 lg:px-10 space-y-3">
                <p class="font-qwigley text-5xl lg:text-7xl">Cerita Kita</p>
                <p class="text-xs lg:text-sm font-light">Banyak cerita yang kami lalui sehingga akhirnya kami bisa bersatu, cerita yang akan kami kenang selalu, dan cerita itu kami bagi untuk anda.</p>
            </div>

            <div class="mt-14 lg:mt-28">
                <ol class="relative border-l border-gray-200 dark:border-gray-700">                  
                    <li class="mb-10 ml-4">
                        <div class="absolute w-3 h-3 bg-green-200 rounded-full -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"></div>
                        <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">15 Februari 2019</time>
                        <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Pertama Kali Berjumpa</h3>
                        <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">Bak cerita-cerita sinetron. Kami berjumpa di depan Lift Apartemen, saat itu lah cinta pada pandangan pertama terjadi. Siapa yang menduga cerita dongeng seperti itu bisa menjadi awal kisah cinta kami.</p>
                    </li>
                    <li class="mb-10 ml-4">
                        <div class="absolute w-3 h-3 bg-green-200 rounded-full -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"></div>
                        <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">26 Desember 2021</time>
                        <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Pertunangan Kami</h3>
                        <p class="text-base font-normal text-gray-500 dark:text-gray-400">Setelah 2 tahun menjalani masa pendekatan dan saling mengenal. Kami memutuskan sudah waktunya kita melanjutkan ke jenjang yang lebih serius</p>
                    </li>
                    <li class="ml-4">
                        <div class="absolute w-3 h-3 bg-green-200 rounded-full -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"></div>
                        <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">27 Maret 2022</time>
                        <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Pernikahan Kami</h3>
                        <p class="text-base font-normal text-gray-500 dark:text-gray-400">The world is full of lonely people afraid to make the first move. Its my first move and she said YES. Fuck yeah! We're getting married!</p>
                    </li>
                </ol>
            </div>
        </div>

        <!-- Video -->
        <!-- <div class="relative py-10">
            <img src="~/assets/img/Bg-Vidio.png" alt="" class="hidden lg:block">
            <img src="~/assets/img/Bg-Vidio2.png" alt="" class="block lg:hidden">
            <div class="absolute top-40 lg:top-80 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
            <p class="text-6xl lg:text-8xl font-qwigley text-white text-center">Video Kami</p>
                <div class="hidden lg:block">
                    <iframe src="https://drive.google.com/file/d/1FKIsVpla-pBHOVIMQk59xW1biQJWyjDc/preview" width="600" height="315" allow="autoplay"></iframe>
                </div>
                <div class="block lg:hidden">
                    <iframe src="https://drive.google.com/file/d/1FKIsVpla-pBHOVIMQk59xW1biQJWyjDc/preview" width="260" height="150" allow="autoplay"></iframe>
                </div>
            </div>
        </div> -->

        <!-- Gallery -->
        <div class="px-5 lg:px-32 py-10 text-center">
            <p class="font-qwigley text-5xl lg:text-7xl">Gallery Foto</p>
            <div class="grid lg:grid-cols-4 gap-5 mt-10">
            <div v-for="x in Gallery" :key="x.Path" :class="x.Class">
                <img :src="'https://drive.google.com/uc?id='+x.Path" alt="" class="md:h-full rounded-lg">
            </div>
            </div>
        </div>

        <!-- Gift -->
        <div class="px-5 lg:px-32 text-center my-20">
            <p class="font-qwigley text-5xl lg:text-7xl">Berikan Hadiah</p>
            <div class="px-8 py-8 border">
                <img src="~/assets/img/qr_code_bca.jpeg" class="w-72 mx-auto">
                <div class="text-xl mt-8">BCA - 4770202863</div>
            </div>
        </div>

        <!-- Presences -->
        <div class="px-5 lg:px-32 py-10 lg:py-20">
            <p class="font-qwigley text-5xl lg:text-7xl">Konfirmasi Kehadiran</p>
            <p class="text-xs lg:text-sm font-light">Merupakan suatu kehormatan dan kebahagiaan bagi kami sekeluarga apabila Bapak/Ibu/Saudara/i berkenan hadir untuk memberikan doa restu kepada kedua mempelai. Atas kehadiran serta doa restu, kami ucapkan terima kasih.</p>
            <div class="px-8 py-8 lg:px-16 lg:py-12 border mt-10 rounded-lg">
                <form class="full space-y-5">
                    
                    <div class="flex flex-col lg:flex-row flex-wrap -mx-3 space-x-0 space-y-5 lg:space-y-0 lg:space-x-5">
                        <div class="flex-1">
                            <label class="block tracking-wide text-gray-700 text-xs font-bold mb-2">Nama</label>
                            <input v-model="NamePresence" type="text" placeholder="Masukan Nama" class="w-full bg-gray-100 py-4 px-5 text-xs" />
                        </div>
                        <div class="flex-1">
                            <label class="block tracking-wide text-gray-700 text-xs font-bold mb-2">Jumlah Orang</label>
                            <select v-model="TotalPresence" type="text" placeholder="Jumlah Orang" class="w-full bg-gray-100 py-4 px-5 text-xs">
                                <option value="">- Pilih Jumlah -</option>
                                <option value="1">1 Orang</option>
                                <option value="2">2 Orang</option>
                            </select>
                        </div>
                    </div>

                    <div class="flex -mx-3">
                        <div class="w-full">
                            <label class="block tracking-wide text-gray-700 text-xs font-bold mb-2">Pesan</label>
                            <textarea v-model="MessagePresence" type="textarea" placeholder="Pesan" class="w-full bg-gray-100 py-4 px-5 text-xs"></textarea>
                        </div>
                    </div>

                    <div class="flex flex-col -mx-3">
                        <label class="block tracking-wide text-gray-700 text-sm font-bold mb-2">Konfirmasi Kehadiran</label>
                        <div class="space-y-3 text-sm">
                            <div class="flex gap-2"><input id="option1" type="radio" name="ConfirmPresence" v-model="ConfirmPresence" value="Hadir resepsi sesi 1"><label for="option1">Hadir resepsi sesi 1</label></div>
                            <div class="flex gap-2"><input id="option2" type="radio" name="ConfirmPresence" v-model="ConfirmPresence" value="Hadir resepsi sesi 2"><label for="option2">Hadir resepsi sesi 2</label></div>
                            <div class="flex gap-2"><input id="option3" type="radio" name="ConfirmPresence" v-model="ConfirmPresence" value="Saya tidak yakin"><label for="option3">Saya tidak yakin</label></div>
                            <div class="flex gap-2"><input id="option4" type="radio" name="ConfirmPresence" v-model="ConfirmPresence" value="Maaf, saya tidak bisa hadir"><label for="option4">Maaf, saya tidak bisa hadir</label></div>
                        </div>
                    </div>

                    <div>
                        <button v-if="LoadingPresence" class="w-full flex justify-center transition ease-in-out duration-150 cursor-not-allowed py-2 text-sm rounded text-white bg-gray-600" @click.stop="savePresence">
                            <svg class="animate-spin -ml-1 mr-3 h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                                <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                                <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                            </svg>
                            Processing
                        </button>
                        <button v-else class="w-full py-2 text-sm rounded text-white bg-gray-600" @click.stop="savePresence">
                            Kirim
                        </button>
                        <p v-show="SuccessPresence">Berhasil terkirim...</p>
                    </div>
                </form>
            </div>
        </div>

        <!-- Outgiving -->
        <div class="px-5 lg:px-32 py-10">
            <p class="font-qwigley text-7xl text-center lg:text-left">Katakan Sesuatu</p>
            <div class="px-8 py-8 lg:px-16 lg:py-12 border mt-10 rounded-lg">
            <form class="full space-y-6">
                <div class="flex flex-row space-x-5">
                    <div class="flex-1 space-y-8">
                        <div>
                            <label class="block tracking-wide text-gray-700 text-xs font-bold mb-2">Name</label>
                            <input v-model="NameOutgiving" type="text" placeholder="Name" class="w-full bg-gray-100 py-4 px-5 text-xs" />
                        </div>
                        <div>
                            <label class="block tracking-wide text-gray-700 text-xs font-bold mb-2">Ucapan</label>
                            <textarea rows="6" v-model="MessageOutgiving" type="textarea" placeholder="Ucapan" class="w-full bg-gray-100 py-4 px-5 text-xs"></textarea>
                        </div>
                        <div>
                            <button v-if="LoadingOutgiving" class="w-full flex justify-center transition ease-in-out duration-150 cursor-not-allowed py-2 text-sm rounded text-white bg-gray-600" @click.stop="savePresence">
                                <svg class="animate-spin -ml-1 mr-3 h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                                    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                                    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                                </svg>
                                Processing
                            </button>
                            <button v-else class="w-full px-16 py-2 text-sm rounded text-white bg-gray-600" @click="saveOutGiving">Kirim</button>
                            <p v-show="SuccessOutgiving">Berhasil terkirim...</p>
                        </div>
                    </div>
                    <div class="hidden lg:block flex-1">
                        <img src="~/assets/img/1643649327582.webp" alt="" class="mt-7">
                    </div>
                </div>
            </form>

            </div>
            <div v-if="OutGivings.length > 0">
                <div class="h-96 mt-10 pb-2 overflow-hidden overflow-y-scroll">
                    <div v-for="og in OutGivings" :key="og.id" class="flex flex-row items-center px-5 py-2 gap-5">
                        <div><img src="~/assets/img/avatar.webp" class="w-16"></div>
                        <div class="w-full px-3 lg:px-7 text-xs lg:text-sm py-3 bg-gray-100 space-y-3 rounded-lg">
                            <p class="font-semibold">{{ og.name }}</p>
                            <div class="text-xs font-light">{{ og.message }} </div>
                        </div>
                    </div>
                </div>
            </div>

            <div v-else>
                <!-- Kalo gak ada data -->
            </div>
        </div>

        <div class="bg-gray-600 text-white mt-60 py-5 font-light text-center">
            © 2022 anywedd. All Rights Reserved
        </div>
    </div>
</template>

<script>
import GuestModal from '../Utils/GuestModal.vue'

const Gallery = [
    {
        Path: '15VFXUptuJQ_PQqqX6ftQIQd5MtJdw_zJ',
        Class: 'col-span-2'
    },
    {
        Path: '1-y5FJkRglrsMnXZpbhdL6KTifnsqiIkX',
        Class: ''
    },
    {
        Path: '1EoewdKNNLPKOPGkD6582gneuTyMGvEvW',
        Class: ''
    },
    {
        Path: '10xeiL7TZmraGNRiRYEx9lUWg_q7kiCT8',
        Class: 'col-span-2'
    },
    {
        Path: '1hwwf6wXc1SB9799G7UUq5GuRBSyGzHnK',
        Class: 'col-span-2'
    },
    {
        Path: '15tS6zb3u8yzpRPNZtUfa6EN8EcWrejbv',
        Class: ''
    },
    {
        Path: '1D5K82Pjc-zMVmMCM6IwpdPgutopfGLcF',
        Class: ''
    },
    {
        Path: '1SnPs3xk1xo1Pchd5qCMCZoVY6D38UxWn',
        Class: 'col-span-2'
    }
]

export default {
    name: "Vian-Eva",
    components: {
        GuestModal,
    },
    data() {
        return {
            GuestInvited: '',
            SpecialInvited: false,
            PlayingAudio: false,

            // Dates
            NowDate: new Date(),
            MarriageDate: new Date("2022-03-27"),
            TheDate: this.MarriageDate - this.NowDate,


            Gallery,

            NamePresence: '',
            TotalPresence: '',
            MessagePresence: '',
            ConfirmPresence: '',
            LoadingPresence: false,
            SuccessPresence: false,

            NameOutgiving: '',
            MessageOutgiving: '',
            LoadingOutgiving: false,
            SuccessOutgiving: false,

            OutGivings: []
        }
    },
    mounted() {
        this.getGuestInvited()
        this.getOutGiving()
    },
    methods: {
        getGuestInvited() {
            let param = this.$route.query.to

            if (param) {
                let split = param.split("-").join(" ")
                this.GuestInvited = split
                this.SpecialInvited = true
            }
        },
        
        playMusic() {
            this.PlayingAudio = true
            this.FileAudio.play()
        },
        
        pauseMusic() {
            this.PlayingAudio = false
            this.FileAudio.pause()
        },

        getOutGiving() {
            this.$axios.get('/outgivings').then((ress) => {
                this.OutGivings = ress.data
            })
        },

        savePresence(e) {
            e.preventDefault()
            this.LoadingPresence = true

            let data = {
                "name": this.NamePresence,
                "num_of_people": this.TotalPresence,
                "confirmation": this.MessagePresence,
                "message": this.ConfirmPresence
            }

            this.$axios.post('/presences', data).then((ress) => {
                if(ress.status == 201) {
                    this.NamePresence = ''
                    this.TotalPresence = ''
                    this.MessagePresence = ''
                    this.ConfirmPresence = ''

                    this.LoadingPresence = false
                    this.SuccessPresence = true

                    setInterval(() => {
                        this.SuccessPresence = false
                    }, 1000);
                } else {
                    this.NamePresence = ''
                    this.TotalPresence = ''
                    this.MessagePresence = ''
                    this.ConfirmPresence = ''

                    this.LoadingPresence = false
                }
            })
        },
        saveOutGiving(e) {
            e.preventDefault()
            this.LoadingOutgiving = true

            let data = {
                "name": this.NameOutgiving,
                "message": this.MessageOutgiving
            }

            this.$axios.post('/outgivings', data).then((ress) => {
                if(ress.status == 201) {
                    // this.successNotify()
                    this.NameOutgiving = ''
                    this.MessageOutgiving = ''

                    this.LoadingOutgiving = false
                    this.SuccessOutgiving = true

                    setInterval(() => {
                        this.SuccessOutgiving = false
                    }, 1000);
                } else {
                    // this.failedNofity()
                    this.NameOutgiving = ''
                    this.MessageOutgiving = ''

                    this.LoadingOutgiving = false
                }
            })
        }
    }
}
</script>