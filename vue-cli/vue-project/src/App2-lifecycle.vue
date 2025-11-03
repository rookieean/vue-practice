<template>
    <div>
        <app-header></app-header>
        <div class="container">
            <comp-life></comp-life>
        </div>
        <app-footer></app-footer>
    </div>
</template>


<script>

    import compLife from './components/index.vue'

    export default {
        components: {
            compLife
        },
        data() {
            return {
                showIt: true
            }
        },
        mounted() {
            setTimeout(() => {
                this.showIt = false;
            }, 2000);
        }
    }
</script>

<style>
.container {
    padding: 20px;
}

</style>