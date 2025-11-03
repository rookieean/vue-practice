<template>
    <div>
        Grape Component 2
    </div>
</template> 

<script>
export default {
    name: 'grape-comp',
    mounted() {
        console.log('mounted')
    },
    unmounted() {
        console.log('unmounted')
    }
}

</script>