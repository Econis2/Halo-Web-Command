<template>

    <base-panel :id="sname + 'TeamKills'" title="Team Kills">
        <form>
            <!-- Limit -->
            <div class="form-group row">
                <label class="col-form-label col-xs-4 col-sm-4 col-md-4 col-lg-4">Limit</label> 
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <input type="number" min="0" class="form-control">
                </div>
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <select class="form-control">
                        <option>sec</option>
                        <option>min</option>
                        <option>hour</option>
                        <option>days</option>
                    </select>
                </div>
            </div>
            <!-- Grace -->
            <div class="form-group row">
                <label class="col-form-label col-xs-4 col-sm-4 col-md-4 col-lg-4">Grace</label> 
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <input type="number" min="0" class="form-control">
                </div>
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <select class="form-control">
                        <option>sec</option>
                        <option>min</option>
                        <option>hour</option>
                        <option>days</option>
                    </select>
                </div>
            </div>
            <!-- Cool Down-->
            <div class="form-group row">
                <label class="col-form-label col-xs-4 col-sm-4 col-md-4 col-lg-4">Cool Down</label> 
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <input type="number" min="0" class="form-control">
                </div>
                <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                    <select id="tkTypeCoolDown" class="form-control">
                        <option>sec</option>
                        <option>min</option>
                        <option>hour</option>
                        <option>days</option>
                    </select>
                </div>
            </div>
        </form>
    </base-panel>



</template>
<script>

import basePanel from '../../panelComponents/panelBase.vue'

export default {
    name: "teamKills",
    props:{
        sname: {
            type: String
        }
    },
    components:{
        "base-panel": basePanel
    }

}



</script>