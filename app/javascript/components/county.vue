<template>
    <div id="county">
        <h1>county component</h1>
        county: <input :value="countyProp"
                      @input="$emit('updateCountyProp', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "county",
        props: ['countyProp'],
        model: {
            prop: 'countyProp',
            event: 'updateCountyProp'
        }
    }
</script>

<style scoped>
    #county {
        background-color: lightgreen;
        width: 300px;
        margin: 10px;
        padding: 10px;
    }
</style>