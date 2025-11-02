<template>
    <div>
        <app-header></app-header>
        <com-brand></com-brand>
            <div class="container">
                <ul>
                    <li>Honda</li>
                    <li>Toyota</li>
                    <li>Ford</li>
                </ul>
            </div>
        <app-footer></app-footer>
    </div>
</template>



<script>

import comBrand from './components/brand.vue'


export default {
    components: {
        comBrand
    },

    data() {
        return {
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