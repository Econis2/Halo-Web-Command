<template>

    <base-panel :id="sname + 'Details'" title="Details">
        <form>
            <div class="form-group row">
                <label class="col-form-label col-xs-2 col-sm-2 col-md-2 col-lg-2">Name</label>
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <input type="text" :value="sname" class="form-control" readonly>
                </div>
                <label class="col-form-label col-xs-3 col-sm-3 col-md-3 col-lg-3">Max Players</label>
                <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
                    <input type="number" min="1" max="16" class="form-control" :value="8" :disabled="true">
                </div>
            </div>
        </form>
    </base-panel>

    

</template>
<script>

import panelBase from '../panelComponents/panelBase.vue'

export default {
    name: "serverDetails",
    props: {
        sname: {
            type: String
        }
    },
    components:{
        'base-panel': panelBase
    }
}


</script>