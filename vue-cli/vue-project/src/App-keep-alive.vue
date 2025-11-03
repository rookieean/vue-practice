<template>
    <div>
        <app-header></app-header>
        <div class="container">

            <button @click="this.activeComp = 'comp-orange'">Show Orange</button>
            <button @click="this.activeComp = 'comp-grape'">Show Grape</button>


            <comp-orange v-if="activeComp === 'comp-orange'"></comp-orange>
            <comp-grape v-if="activeComp === 'comp-grape'"></comp-grape>


            // panggil si orange dan grape
            <comp-orange></comp-orange>
            <comp-grape></comp-grape>


            // dynamic component
            <component :is="activeComp"></component>


            // keep alive
            <keep-alive include="comp-orange">
                <component :is="activeComp"></component>
            </keep-alive>

        </div>
        <app-footer></app-footer>
    </div>
</template>


<script>
import compOrange from './components/orange.vue'
import compGrape from './components/grape.vue'

    export default {
        components: {
            compOrange,
            compGrape

        },
        data() {
            return {
                activeComp: 'comp-orange'
            }
        },
    }

</script>


// keep alive -> biar state component tetap terjaga walaupun di hide
// misal user isi form di component orange, terus pindah ke grape, terus balik lagi ke orange
// nah formnya tetep keisi, gak ilang





<style>
.container {
    padding: 20px;
}

</style>