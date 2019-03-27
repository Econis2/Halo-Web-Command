<template>
    <div class="panel-heading">
        <div class="row">
            <div class="col-xs-10 col-sm-10 col-md-10 col-lg-10">
            <h4 class="panel-title">{{ title }}</h4>
            </div>
            <div class="col-xs-2 col-sm-2 col-md-2 col-lg-2">
                <chev :href="'#' + chevhref" :name="chevhref + 'Chev'"></chev>
            </div>
        </div>
    </div>
</template>

<script>

import menuChev from './menuChev.vue'

export default {
    name: 'panelHeader',
    props: {
        'title': {
            type: String,
            default: "Default Header"
        },
        'chevhref': {
            type: String,
            default: ''
        }
    },
    components:{
        chev: menuChev
    }

}

</script>

<style>


</style>