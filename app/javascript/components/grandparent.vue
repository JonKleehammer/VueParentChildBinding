<template>
    <div id="grandparent">
        <h3>grandparent component</h3>
        legals: {{legals}}
        <legal-description v-for="legal in legals" :legal.sync="legal"/>
    </div>
</template>

<script>
    import legalDescription from './legal-desc'

    export default {
        name: "grandparent",
        props: {
            legals: {default: () => [{}, {}] }
        },
        components: {
            legalDescription
        }
    }
</script>

<style scoped>
    #grandparent {
        margin: 20px;
        padding: 20px;
        /*display: inline-block;*/
        background-color: lightcoral;
        display: inline-flex;
        flex-direction: column;
    }
</style>