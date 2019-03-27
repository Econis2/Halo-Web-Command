<template>
    <div id="myServers" class="container-fluid">
        <server :serverprops="serverprops"></server>
    </div>
</template>

<script>

import serverPanel from '../panel/server/main.vue'

export default {
    name: 'myServers',
    components: {
        server: serverPanel
    },
    methods:{
        getServerData(){},
        getAssociatedServers(){}
    },
    data: function() {

        // Lookup user and find servers associated
        // Collect Data and Return ServerObjects[]
        

        return {
            serverprops: {
                auth:{
                    token: "somerandomstringofcharacters"
                }
            }
        }
    }

}



// set timer for 10 sec refresh of data


</script>