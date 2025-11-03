<template>
    <div>
        Orange Component 2
    </div>
</template> 

<script>
export default {
    name: 'orange-comp',
    mounted() {
        console.log('mounted')
    },
    activated() {
        console.log('orange activated')
    },
    deactivated() {
        console.log('orange deactivated')
    },
    unmounted() {
        console.log('orange unmounted')
    }
}

</script>