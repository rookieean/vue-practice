<template>
    <div>
        <h3>
            Grape Component 2
        </h3>

        <teleport to="body">
            <comp-modal></comp-modal>
        </teleport>
    </div>
</template> 

<script>

import compModal from '../utils/modal.vue';

export default {
    Components: {
        compModal
    },
    name: 'grape-comp',
    unmounted() {
        console.log('grape unmounted')
    }
}

// teleport -> digunakan untuk memindahkan element ke tempat lain di DOM

</script>