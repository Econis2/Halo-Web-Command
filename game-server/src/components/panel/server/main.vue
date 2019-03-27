<template>
    <div class="panel-group">
        <div class="panel panel-default">
            <main-server-header :headerprops="headerInfo"></main-server-header>
        </div>
        <div class="panel-collapse collapse" :id="headerInfo.serverName + 'Main'">
            <div class="panel-body">
                <basic-info :tickerinfo="headerInfo"></basic-info>
                <server-details :sname="headerInfo.serverName"></server-details>
                <player-settings :sname="headerInfo.serverName"></player-settings>
                <map-settings :sname="headerInfo.serverName"></map-settings>
            </div>
        </div>
    </div>
</template>

<script>

import panelHeader from './mainHeader.vue'
import basicInfo from './basicInfo.vue'
import serverDetails from './details.vue'
import playerSettings from './playerSettings/main.vue'
import mapSettings from './maps.vue'

export default {
    name: "server",
    props:{
        serverprops: {
            type: Object
        }
    },
    mounted: function (){
        
        window.setInterval(()=> {
            this.updateHeader()
        },1000)
    },
    data: function(){
        return {
            headerInfo: {
                serverName: "testServer1",
                currentUpTime: (new Date()),
                currentMap: "BloodGultch",
                currentGameType: "Slayer"
            }
        }
    },
    components:{
        'main-server-header': panelHeader,
        'basic-info': basicInfo,
        'server-details': serverDetails,
        'player-settings': playerSettings,
        'map-settings': mapSettings
    },
    methods: {
        updateHeader(){
            // get some data and update header
            this.headerInfo.currentUpTime = (new Date())

        }
    }
}





</script>