<template>
    <div id="property-desc">
        <h3>property-desc component</h3>
        legals:
        <p style="white-space: pre">{{JSON.stringify(legals, null, 4)}}</p>

        <button id="add-legal-button" @click="addLegal">Add Legal</button>
        <legal-description v-for="legal in legals" :legal.sync="legal"/>
    </div>
</template>

<script>
    import legalDescription from './legal-desc'

    export default {
        name: "property-desc",
        props: ['legals'],
        components: {
            legalDescription
        },
        methods: {
            addLegal: function() {
                console.log('test')
                this.legals.push({})
            }
        }
    }
</script>

<style scoped>
    #property-desc {
        margin: 20px;
        padding: 20px;
        background-color: paleturquoise;
        display: inline-flex;
        flex-direction: column;
    }
    #add-legal-button {
        width: 100px;
        margin: 10px;
    }
</style>