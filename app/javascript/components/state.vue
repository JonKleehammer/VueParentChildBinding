<template>
    <div id="state">
        state: <input :value="value"
                      @input="$emit('input', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "state",
        props: ['value']
    }
</script>

<style scoped>
    #state {
        background-color: lightblue;
        width: 300px;
        margin: 10px;
        padding: 10px;
    }
</style>