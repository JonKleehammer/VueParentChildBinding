<template>
    <div id="legal-desc">
        <h1>legal-desc component</h1>
        <h3>Data on the parent (legal-desc)</h3>
        <h4>
            state: {{state}}<br>
            county: {{county}}
        </h4>

        <h3>Inputs on parent for manipulating data</h3>
        state parent input: <input v-model="state"><br>
        county parent input: <input v-model="county">

        <h2>Inputs in child components</h2>
<!--        v-model on a vue component creates 2 things-->
        <state v-model="state"></state>
        <county v-model="county"></county>
    </div>
</template>

<script>
    import state from './state'
    import county from './county'

    export default {
        name: "legal-desc",
        components: {
            state: state,
            county: county
        },
        data() {
            return {
                state: 'Texas',
                county: 'Andrews'
            }
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