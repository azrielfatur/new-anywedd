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
                    content: 'https://drive.google.com/uc?id=1g_9U1c6gO3UT6Hh03EMnO4gWYvNkMnB5'
                },
                {
                    hid: 'og:image',
                    name: 'og:image',
                    content: 'https://drive.google.com/uc?id=1g_9U1c6gO3UT6Hh03EMnO4gWYvNkMnB5'
                }
            ]
        }
    },
  components: { VianEva },
}
</script>