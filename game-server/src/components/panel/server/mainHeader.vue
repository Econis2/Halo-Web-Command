<template>
    <div class="panel-heading">
        <div class="row">
            <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                <h4 class="panel-title">{{ headerprops.serverName }}</h4>
            </div>
            <div class="col-xs-5 col-sm-5 col-md-5 col-lg-5">
                <marquee behavior="scroll" direction="left" class="form-control">{{ "[UPTIME] " + headerprops.currentUpTime + " [MAP] " + headerprops.currentMap + " [GAMETYPE] " + headerprops.currentGameType }}</marquee>
            </div>
            <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                <div class="row">
                    <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                        <button class="btn fas fa-step-backward"></button>
                    </div>
                    <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                        <button class="btn fas fa-stop"></button>
                    </div>
                    <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                        <button class="btn fas fa-play"></button>
                    </div>
                    <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                        <button class="btn fas fa-step-forward"></button>
                    </div>
                </div>                        
            </div>
            <div class="col-xs-1 col-sm-1 col-md-2 col-lg-1">
                <chev :href="'#' + headerprops.serverName + 'Main'" :name="headerprops.serverName + 'MainChev'"></chev>
            </div>
        </div>
    </div>
</template>

<script>

import chev from '../panelComponents/menuChev.vue'

export default {
    name: 'panelHeader',
    props: {
        'headerprops': {
            type: Object
        }
    },
    components:{
        chev: chev
    }
}

</script>

<style>


</style>