<template>

    <base-panel :id="sname + 'PlayerSettings'" title="Player Settings">
        <ban-list :sname="sname"></ban-list>
        <team-kills :sname="sname"></team-kills>
    </base-panel>




</template>
<script>

import panelBase from '../../panelComponents/panelBase.vue'
import banList from './banList.vue'
import teamKills from './teamKills.vue'

export default {
    name: "playerSettings",
    props:{
        sname: {
            type: String
        }
    },
    components:{
        'ban-list': banList,
        'base-panel': panelBase,
        'team-kills': teamKills
    }
}




</script>