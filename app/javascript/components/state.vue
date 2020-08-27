<template>
    <div id="state">
        <h3>state component</h3>
        state: {{state}}<br>
        state: <input :value="state"
                      @input="$emit('update:state', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "state",
        props: ['state']
    }
</script>

<style scoped>
    #state {
        background-color: lightblue;
        display: inline-block;
        margin: 10px;
        padding: 10px;
    }
</style>