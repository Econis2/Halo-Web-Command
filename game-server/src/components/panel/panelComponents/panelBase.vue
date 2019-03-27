<template>


    <div class="panel-group">
        <div class="panel panel-default">
            <base-header :title="title" :chevhref="id"></base-header>
        </div>
        <div class="panel-collapse collapse" :id="id">
            <div class="panel-body">
                <slot></slot>
            </div>
        </div>
    </div>





</template>

<script>

import panelHeader from './panelHeader.vue'

export default {
    name: "panel-base",
    props:{
        'id':{
            type: String
        },
        'title': {
            type: String
        }
    },
    components:{
        'base-header': panelHeader
    }
}





</script>