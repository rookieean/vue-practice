<template>
    <div>
        <app-header></app-header>
        <div class="container">

            // parents *slots
            <com-brand>
                <ul>
                    <li v-for="(brand, index) in brands" key="index">{{ brand }}</li>
                </ul>



                // *named slots
                <template v-slot:brands>
                    <ul>
                        <li v-for="(brand, index) in brands" :key="index">{{ brand }}</li>
                    </ul>
                </template>

                <template v-slot:other>
                    <h3>Other Slots</h3>
                </template>

                <strong>default</strong>
            </com-brand>
            </div>
        <app-footer></app-footer>
   
   </div>
</template>

// gimana cara agar components anak bisa nerima dari parentsnya?
// jadi ada namanya slots

<script>

import comBrand from './components/brand.vue'


export default {
    components: {
        comBrand
    },

    data() {
        return {
            brands: ['Honda', 'Toyota', 'Ford'], // tetep di parents
            cars: [
                {model: 'Jazz', brand: 'Honda'},
                {model: 'Yaria', brand: 'Toyota'},
                {model: 'Airew', brand: 'Mulling'},
            ]
        }
    },
}

provide() {
    
}

</script>


// klo mau rubah si li taruh disini
<style>
    .container {
        margin-top: 20px;
    }

    li {
        color: red;
    }
</style>

// jika text components berada di file a, maka taruh semua data, style dll ya di file a




// *slots adalah cara components anak nerima data dari parentsnya
// *named slots adalah cara components anak nerima data dari parentsnya dengan nama tertentu, krblh pakai slots sesuai kebutuhan kita