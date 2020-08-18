<template>
    <div id="legal-desc">
        <h2>Inputs in child components</h2>
        <state v-model="legal.state"></state>
        <county :county.sync="legal.county" :state="legal.state"></county>
    </div>
</template>

<script>
    import state from './state'
    import county from './county'

    export default {
        name: "legal-desc",
        props: {
            legal: { default: {state: null, county: null} }
        },
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
        width: 600px;
        background-color: lightgoldenrodyellow;
    }
</style>