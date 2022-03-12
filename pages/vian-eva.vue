<template>
    <vian-eva />
</template>

<script>
import VianEva from '~/components/Templates/Vian-Eva.vue'
export default {
head: {
    title: 'Pernikahan Vian & Eva',
    meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
            hid: 'description',
            name: 'description',
            content: 'Undangan Pernikahan Vian & Eva'
        }
    ]
},
  components: { VianEva },
}
</script>