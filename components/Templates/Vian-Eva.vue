<template>
    <div>
        <guest-modal v-show="SpecialInvited" v-bind="GuestInvited"/>
        <div class="fixed z-50 bottom-5 right-5">
            <button class="py-2 px-4 bg-gray-100" unelevated :icon="PlayingAudio ? 'music_off' : 'music_note'" @click.prevent="PlayingAudio ? pauseMusic(FileAudio) : playMusic(FileAudio) "></button>
        </div>
        <div class="relative">
            <img src="~/assets/img/16436960169351.webp" class="w-full hidden md:block h-screen object-cover" alt="Vian & Eva">
            <img src="~/assets/img/cover-mobile.webp" class="w-full block md:hidden h-screen object-cover" alt="Vian & Eva">
            <div class="absolute mt-10 md:mt-0 top-36 md:top-72 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-white text-center">
                <div class="text-lg font-thin">The Wedding Of</div>
                <div class="font-qwigley text-8xl lg:text-8xl">Eva <br> & <br> Vian</div>
                <div class="text-lg font-thin">27 . 03 . 2022</div>
            </div>
        </div>
    </div>
</template>

<script>
import GuestModal from '../Utils/GuestModal.vue'
export default {
  components: { GuestModal },
    name: "Vian-Eva",
    data() {
        return {
            GuestInvited: '',
            PlayingAudio: false,
            // FileAudio: new Audio('/assets/music/Paul Anka  Put Your Head on My Shoulder Cover by The Macarons Project.mp3'),

            SpecialInvited: false,
        }
    },
    mounted() {
        this.getGuestInvited()
        console.log(this.FileAudio)
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
    }
}
</script>