<template>
    <vian-eva />
</template>

<script>
import VianEva from '~/components/Templates/Vian-Eva.vue'
export default {
    head() {
        return {
            title: 'Pernikahan Vian & Eva',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Undangan Pernikahan Vian & Eva'
                },
                {
                    hid: 'og:description',
                    name: 'og:description',
                    content: 'Undangan Pernikahan Vian & Eva'
                },
                {
                    hid: 'image',
                    name: 'image',
                    content: '_nuxt/img/thumbnail.png'
                },
                {
                    hid: 'og:image',
                    name: 'og:image',
                    content: '_nuxt/img/thumbnail.png'
                }
            ]
        }
    },
  components: { VianEva },
}
</script>