<template>

    <form>
        <div class="form-group row">
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                <input type="text" class="form-control" :placeholder="tickerinfo.currentUpTime" readonly>
            </div>
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                <input type="text" class="form-control" :placeholder="tickerinfo.currentMap" readonly>
            </div>
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
                <input type="text" class="form-control" :placeholder="tickerinfo.currentGameType" readonly>
            </div>
        </div>
    </form>

</template>

<script>

export default {
    name: "basicServerInfo",
    props: {
        tickerinfo: {
            type: Object
        }
    }
}


</script>