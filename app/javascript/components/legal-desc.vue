<template>
    <div id="legal-desc">
        <h3>legal-desc component</h3>
        legal: {{legal}}<br>
        <state :state.sync="legal.state"></state>
        <county :county.sync="legal.county" :state="legal.state"></county>
    </div>
</template>

<script>
    import state from './state'
    import county from './county'

    export default {
        name: "legal-desc",
        props: ['legal'],
        components: {
            state,
            county
        }
    }
</script>

<style scoped>
    #legal-desc {
        margin: 20px;
        padding: 20px;
        display: inline-block;
        background-color: lightgoldenrodyellow;
    }
</style>