<template>
    <div>
        <app-header></app-header>
        <div class="container">

        // panggil directive disni
        <comp-directive></comp-directive>

        </div>
        <app-footer></app-footer>
    </div>
</template>


<script>

    import compDirective from './directive/index2.vue'

    export default {
        components: {

        },
        
        data() {
            return {
      
            }
        },
    }

</script>


// ada dua cara pakai directive 
// global dan lokal
// 



<style>
.container {
    padding: 20px;
}

</style>