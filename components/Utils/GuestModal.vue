<template>
    <div>
        <div class="flex fixed justify-center bg-black opacity-60 top-0 bottom-0 right-0 left-0 z-10"> 
        </div>
        <div class="flex fixed justify-center items-center top-0 bottom-0 right-0 left-0 z-10">
                <div class="flex items-center bg-white w-96 h-48 rounded-md mx-5" style="background-image: url('img/SpecialInvited.png'); background-size: 100% 100%;">
                <div class="text-center py-5 mx-auto">
                    <p class="text-sm">Kepada Yth.</p>
                    <h6 class="text-2xl font-medium py-2">Testing Name</h6>
                    <p class="text-sm">Ditempat</p>
                    <button class="bg-gray-700 text-white rounded-md py-2 px-5 mt-5">Buka Undangan</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            GuestInvited: '',
        }
    }
}
</script>