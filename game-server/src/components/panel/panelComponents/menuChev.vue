<template>
    <button @click="toggleChev" class="endChev btn fas fa-angle-double-down" data-toggle="collapse"></button>
</template>

<script>

export default {
    name: 'headChev',
    props: {},
    methods:{
        toggleChev(event){
                $("button[name="+ event.target.name + "]").toggleClass('fa-angle-double-up')
                $("button[name="+ event.target.name + "]").toggleClass('fa-angle-double-down')
        }
    }
}

</script>

<style></style>