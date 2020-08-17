<template>
    <div id="county">
        county: <input :value="value"
                      @input="$emit('input', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "county",
        props: ['value']
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