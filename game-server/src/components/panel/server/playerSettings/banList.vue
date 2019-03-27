<template>

    <base-panel :id="sname + 'BanList'" title="Ban List" :sname="sname">
        <p> Some Ban List Players will populate here </p>
    </base-panel>

</template>
<script>

import panelBase from '../../panelComponents/panelBase.vue'

export default {
    name: 'banList',
    props:{
        sname: {
            tpye: String
        }
    },
    components:{
        'base-panel': panelBase
    }
}




</script>