<template>
    <div id="county">
        <h3>county component</h3>
        state: {{state}}<br>
        county: {{county}}<br>
        county: <input :value="county"
                      @input="$emit('update:county', $event.target.value)"  />
    </div>
</template>

<script>
    export default {
        name: "county",
        props: ['county', 'state'],
    }
</script>

<style scoped>
    #county {
        background-color: lightgreen;
        display: inline-block;
        margin: 10px;
        padding: 10px;
    }
</style>