<template>
    <div>
        Lifecycle Hook
    </div>
</template>

<script>
    export default {
        data() {
            return {

            }
        },
        beforeCreate() {
            console.log('beforeCreate hook called');
        },
        created() {
            console.log('2-created')
        },
        beforeMount() {
            console.log('3-beforeCreate')
        },
        mounted() {
            console.log('4-mounted')
        },
        beforeUpdate() {
            console.log('U1-beforeUpdate')
        },
        updated() {
            console.log('U2-updated')
        },
        beforeUnmount() {
            console.log('D1-beforeUnmount');
        },
        unmounted() {
            console.log('D2-unmounted');
        }
    }

</script>