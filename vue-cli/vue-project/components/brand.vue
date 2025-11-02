<template>
    <div>
        <h1> Brand View </h1>

        // child yang akan nerima dari parents
       <slot></slot> 
        
        
        <slot name="brands"></slot>
        <slot name="other"></slot>
    </div>
</template>

<script>

// data disini gak bisa, karena data harus tetep di parents
export default {
    data() {
        return {
           //  brands: ['Honda', 'Toyota', 'Ford'],
        }
    }
}

</script>



// klo pakai scope gak bakal global
<style scoped>
    li {
        color: blue;
    }
</style>