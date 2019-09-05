<template>
    <div class="wrapper">
        Related News
        <RightPanelItems />
        <RightPanelItems />
        <RightPanelItems />
    </div>
</template>

<script>
    import RightPanelItems from './RightPanelItems.vue'

    export default {
        name: "RightPanel",
        components: {
            RightPanelItems
        }
    }
</script>

<style scoped>
    .wrapper {
        font-size: 18px;
        width: 100%;
        height: auto;
        margin-top: 26px;
        text-align: left;
        padding-left: 20px;
        padding-right: 20px;
    }
    @media only screen and (max-width : 992px) {
        .wrapper {
            padding: 0;
        }
    }
</style>