<template>
    <div class="box has-text-weight-bold" :style="estilos">
        <slot></slot>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: 'Box-Tracker',
    data () {
        return {
            estilos: {
                background: '#FAF0CA'
            }
        }
    }

})
</script>

