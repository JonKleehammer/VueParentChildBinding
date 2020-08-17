<template>
    <div id="legal-desc">
        <h2>Data on the parent (legal-desc)</h2>
        <h4>
            state: {{state}}<br>
            county: {{county}}
        </h4>

        <h2>Inputs on parent for manipulating data</h2>
        <input v-model="state"><br>
        <input v-model="county">

        <h2>Inputs in child components</h2>
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