<template>
    <Box>
        <div class="column is-7">
            {{ tarefa.descricao || 'Tarefa sem descrição!' }}
        </div>
        <div class="column">
           <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>     
        </div>
    </Box>
</template>

<script lang="ts">

import { defineComponent, PropType } from 'vue';

import Cronometro from './Cronometro.vue';
import ITarefa from '@/interfaces/ITarefa';
import Box from './Box.vue';

export default defineComponent({
    name: 'Tarefa-Track',
    components: {
        Cronometro,
        Box
    },
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
                required: true 
        }
    }
})
</script>
