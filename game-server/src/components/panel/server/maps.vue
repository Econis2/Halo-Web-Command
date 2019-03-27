<template>
    <base-panel :id="sname + 'Maps'" title="Maps">
        <p> Reserved for Map Content </p>
    </base-panel>
</template>
<script>

import basePanel from '../panelComponents/panelBase.vue'

export default {
    name: "Maps",
    props:{
        sname:{
            type: String
        }   
    },
    components:{
        'base-panel': basePanel
    }
}


</script>